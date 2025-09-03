# 工作流编排说明 (Workflow Orchestration Documentation)

**目的:** 描述 AutoGen 团队协作生成网站内容的核心工作流程、Agent 调用顺序、依赖关系和数据传递机制。

**版本:** 1.0
**创建日期:** 2025-03-27

---

## 1. 总体流程概述

本工作流旨在模拟一个从项目启动、信息收集、策略制定、设计、内容创作、优化到代码生成的完整网站建设流程。流程被划分为多个阶段，由 `ProjectManager` (或外部协调者/脚本) 驱动，并依赖于各专业 Agent 的协作。

**核心原则:**

*   **阶段化执行:** 遵循 `Template_PhasedExecutionPlan.md` 中定义的阶段进行。
*   **依赖驱动:** 后续步骤依赖于前置步骤的成功完成和产出物。
*   **模板化:** 大量使用 `template_System` 中的模板来规范输入和输出。
*   **结构化数据:** Agent 间优先传递结构化数据 (JSON) 或标准化的文档 (Markdown)。
*   **审核节点:** 在关键阶段（策略、线框图、内容）后设置审核点。

## 2. 核心工作流程 (示例: 创建一个新页面)

以下是一个创建新页面（例如产品详情页）的典型流程：

1.  **启动 (Triggered by `ProjectManager` / User):**
    *   **输入:** 页面创建请求 (信息符合 `Template_InputChecklist_BriefCreation.md`)。
    *   **动作:** `ProjectManager` 验证输入完整性，触发 `ContentStrategist`。

2.  **内容简报创建 (`ContentStrategist`):**
    *   **输入:** 页面创建请求信息、网站策略 (`4_Strategy/...`)、品牌指导 (`3_Info/...`)、关键词 (`Keyword_Researcher` 输出)、热点 (`TrendSpotterAgent` 输出)。
    *   **动作:** 使用 `Template_BriefDocument.md` 创建详细内容简报。
    *   **输出:** 内容简报文档 (`4_Strategy/Briefs/...Brief_[PageName].md`)。
    *   **下一步:** 提交简报给 `ProjectManager` 或 `ReviewerAgent` 审核。

3.  **简报审核 (`ReviewerAgent` / `User_Proxy`):**
    *   **输入:** 内容简报文档。
    *   **动作:** 使用 `Template_ReviewChecklist_Strategy.md` (或类似简报审核清单) 进行审核。
    *   **输出:** 审核意见 (`.review.md` 文件或状态更新)。
    *   **下一步:** 如果通过，`ProjectManager` 触发 `UX_Designer`；否则，返回 `ContentStrategist` 修改。

4.  **线框图设计 (`UX_Designer`):**
    *   **输入:** 已批准的内容简报、信息架构 (`5_Outline/...Architecture.md`)、视觉指南 (`3_Info/...`)。
    *   **动作:** 设计页面线框图。
    *   **输出:** 线框图文档 (`5_Outline/Sub/...Wireframe_[PageName].md`)。
    *   **下一步:** 提交线框图供审核。

5.  **线框图审核 (`ReviewerAgent` / `User_Proxy` / `ContentStrategist`):**
    *   **输入:** 线框图文档、关联简报。
    *   **动作:** 使用 `Template_ReviewChecklist_Wireframe.md` 进行审核。
    *   **输出:** 审核意见。
    *   **下一步:** 如果通过，`ProjectManager` 触发 `PromptEngineer` (如果使用) 或 `ContentWriter`；否则，返回 `UX_Designer` 修改。

6.  **Prompt 工程 (`PromptEngineer` - 可选):**
    *   **输入:** 已批准的简报、已批准的线框图、通用 Prompt 模板 (`Template_Prompt_PageWriter.md`)。
    *   **动作:** 为 `ContentWriter` 生成具体的、填充了上下文的 Prompt 文件。
    *   **输出:** 页面 Prompt 文件 (`6_Detail/Prompts/...Prompt_[PageName].md`)。
    *   **下一步:** 触发 `ContentWriter`。

7.  **内容创作 (`ContentWriter`):**
    *   **输入:** 页面 Prompt 文件 (或直接接收简报/线框图等信息)。
    *   **动作:** 根据 Prompt 指令撰写内容。
    *   **输出:** 页面内容 JSON 文件 (`6_Detail/Pages/...Content_[PageName].json`)，包含 `suggested_assets`。
    *   **下一步:** 提交内容 JSON 供审核。

8.  **内容审核 (`ReviewerAgent` / `User_Proxy` / `ContentStrategist` / `SEO_Specialist`):**
    *   **输入:** 页面内容 JSON 文件、关联简报、关联线框图。
    *   **动作:** 使用 `Template_ReviewChecklist_Content.md` 进行审核。
    *   **输出:** 审核意见。
    *   **下一步:** 如果通过，`ProjectManager` 触发 `SEO_Specialist` 和 `AssetGenerationAgent`；否则，返回 `ContentWriter` 修改。

9.  **SEO 优化 (`SEO_Specialist`):**
    *   **输入:** 已批准的页面内容 JSON、网站策略 (含关键词)。
    *   **动作:** 优化元数据，生成 Schema Markup。
    *   **输出:** SEO Schema 文件 (`7_SEO/...Schema_[PageName].jsonld`) 或更新后的内容 JSON。
    *   **下一步:** 提交 SEO 产出物。

10. **资产生成 (`AssetGenerationAgent`):**
    *   **输入:** 内容 JSON 中的 `suggested_assets`、图片生成 Prompt 模板 (`Template_Prompt_ImageGenerator.md`)、视觉指南。
    *   **动作:** 生成图片/图标等资产。
    *   **输出:** 资产文件 (存储在 `8_Assets/...`)、生成的资产路径列表。
    *   **下一步:** 触发 `AssetManagerAgent` (如果定义)。

11. **资产管理 (`AssetManagerAgent` - 可选):**
    *   **输入:** 生成的资产路径列表、内容 JSON 文件路径。
    *   **动作:** (可选) 移动资产到最终位置，更新内容 JSON 中的 `src` 路径。
    *   **输出:** 更新后的内容 JSON 文件。
    *   **下一步:** 触发 **内容翻译** 步骤 (或直接触发 `WebDeveloperAgent` 如果不需要翻译)。

12. **内容翻译 (`TranslationServer` / Manual):**
    *   **触发:** 源语言 (如 'en') 的内容 JSON 审核通过后，且资产管理步骤完成 (如果需要更新路径)。
    *   **输入:** 源语言内容 JSON 文件路径 (`6_Detail/Pages/en/...`), 目标语言列表 (e.g., ['de', 'zh-CN'])。
    *   **动作 (自动化):** 调用 `TranslationServer` 的 `translate_json_content` 工具。
    *   **动作 (手动):** 人工翻译 JSON 文件中的文本内容。
    *   **输出:** 翻译后的内容 JSON 文件，存储在对应的语言子目录下 (`6_Detail/Pages/de/...`, `6_Detail/Pages/zh-CN/...`)。
    *   **下一步:** (可选) 对翻译后的内容进行审核。然后触发 `WebDeveloperAgent` (为每种语言或使用 i18n 库)。

13. **代码生成 (`WebDeveloperAgent`):**
    *   **输入:** 最终的内容 JSON、线框图、视觉指南、SEO Schema、技术栈信息、开发者指令 (`Template_Instruction_WebDeveloper.md`)。
    *   **动作:** 生成页面代码。
    *   **输出:** 代码文件 (`9_WebsiteCode/...`)。
    *   **下一步:** (可选) 提交代码供审核或触发部署流程。

## 3. 数据传递机制

*   **文件引用:** Agent 主要通过引用文件系统中的标准化文件路径来传递信息。
*   **结构化数据:** 对于需要精确解析的数据（如页面内容、配置信息），优先使用 JSON 格式。
*   **模板变量:** Prompt 和指令模板使用 `{{variable_name}}` 形式的变量，由协调者或上游 Agent 负责填充。

## 4. 状态跟踪与错误处理

*   **状态跟踪:** 可通过文件命名中的 `[状态]` 标识 (draft, review, final) 或 `PhasedExecutionPlan.md` 中的复选框进行。
*   **错误处理:** (待细化) 当前主要依赖 Agent 在遇到问题时报告错误。未来可考虑加入更复杂的重试、回退或人工介入机制。

---

**备注:** 这是一个高层次的流程描述。具体的实现可能需要根据所选的 AutoGen 框架 (如 Autogen Studio, CrewAI, LangGraph) 进行调整和细化配置。
