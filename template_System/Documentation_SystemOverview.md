# 系统概览与外部输入汇总 (System Overview & External Inputs Summary)

**目的:** 提供 AutoGen 团队的角色构成概览，并汇总整个工作流程中需要从外部（用户或配置）获取的关键输入信息。

**版本:** 1.0
**创建日期:** 2025-03-27

---

## 1. Agent 角色概览 (Agent Role Summary)

以下是本 AutoGen 团队中定义的主要角色及其核心职责：

*   **`ProjectManager`:** (定义: `0_Planning/`) 协调整个工作流程，驱动阶段性执行，管理任务和状态。
*   **`SourceCollectorAgent`:** (定义: `1_Source/`) 根据指令收集网页、文件等源信息。
*   **`MarketAnalyst`:** (定义: `2_Report/`) 分析市场、竞品，生成分析报告。
*   **`BrandStrategist`:** (定义: `3_Info/`) 定义品牌核心元素、故事、视觉原则和网站规则。
*   **`WebsiteStrategist`:** (隐含，定义待补充) 制定网站整体策略（信息架构原则、内容支柱等）。
*   **`ContentStrategist`:** (定义: `4_Strategy/`) 规划内容主题，创建详细内容简报 (Briefs)。
*   **`Keyword_Researcher`:** (定义: `sub_agents/KeywordAgent/` - 假设) 研究关键词，为策略和内容提供支持。
*   **`TrendSpotterAgent`:** (定义: `sub_agents/TrendSpotterAgent/`) 监控市场热点和趋势。
*   **`InformationArchitect`:** (隐含，定义待补充) 设计网站信息架构和导航。
*   **`UX_Designer`:** (定义: `5_Outline/`) 基于简报设计页面线框图 (Wireframes)。
*   **`PromptEngineer`:** (隐含，定义待补充) (可选) 基于简报和线框图，为 ContentWriter 生成详细 Prompt。
*   **`ContentWriter`:** (定义: `6_Detail/`) 基于 Prompt 或简报/线框图，撰写结构化页面内容 (JSON)。
*   **`SEO_Specialist`:** (定义: `7_SEO/`) 优化页面元数据，生成 Schema Markup。
*   **`AssetGenerationAgent`:** (隐含，定义待补充，模板: `template_System/Template_Prompt_ImageGenerator.md`) (可选) 使用 AI 生成图片等资产。
*   **`AssetManagerAgent`:** (隐含，定义待补充) (可选) 管理资产存储和更新内容中的路径引用。
*   **`WebDeveloperAgent`:** (定义: `9_WebsiteCode/`) 基于内容 JSON、设计和 SEO 信息，生成网站代码。
*   **`ReviewerAgent` / `User_Proxy`:** (隐含，定义待补充) 负责在关键节点审核产出物并提供反馈/批准。

*(**注:** 标记为“隐含”的角色虽然在流程中被提及或有模板支持，但尚未创建独立的 `.md` 定义文件。)*

## 2. 外部输入 / 配置变量汇总 (External Inputs / Configuration Variables Summary)

以下是启动或运行此工作流程时，通常需要从外部（用户、配置文件、启动参数）提供的关键信息：

*   **项目/任务基本信息:**
    *   `project_name`: 项目或任务的唯一标识名称。
    *   `initial_request`: 初始的项目目标描述或具体的页面/内容创建请求（可能包含 `Template_InputChecklist_BriefCreation.md` 中的部分信息）。
*   **源信息收集 (`SourceCollectorAgent` 输入):**
    *   `source_collection_tasks`: 需要收集的源列表及其类型（URLs, 文件路径, API 端点等）。
    *   (可选) `proxy_credentials`: 访问受限资源的代理或认证信息。
*   **品牌核心信息 (可能部分由 `BrandStrategist` 定义，但初始输入可能来自用户):**
    *   `brand_name`: 品牌名称。
    *   `initial_brand_guidelines`: 任何已有的品牌文档或核心价值描述。
    *   `target_audience_overview`: 对目标受众的基本描述。
*   **具体产品/服务信息 (用于产品页等):**
    *   `product_database_or_files`: 指向包含详细产品信息的数据库、API 或文件列表的指针/路径。`ContentStrategist` 或 `ContentWriter` 需要从中提取特定产品的信息。
*   **技术栈配置 (`WebDeveloperAgent` 输入):**
    *   `tech_stack_info`: 指定网站使用的前端框架、库、CSS 预处理器等技术细节。
*   **API 密钥/访问权限 (用于特定 Agent):**
    *   `trendspotter_api_keys`: (如需) `TrendSpotterAgent` 访问社交媒体或趋势工具的 API 密钥。
    *   `asset_generator_api_keys`: (如需) `AssetGenerationAgent` 访问 AI 图片生成服务的 API 密钥。
    *   `market_data_api_keys`: (如需) `MarketAnalyst` 访问外部市场数据 API 的密钥。
*   **审核与批准 (涉及 `ReviewerAgent` / `User_Proxy`):**
    *   `reviewer_identity`: 指定负责审核的人员或 Agent。
    *   `approval_mechanism`: 审核结果如何反馈给系统（例如，手动更新状态文件、API 回调、特定 Agent 交互）。
*   **部署配置 (如果流程包含部署):**
    *   `deployment_target`: 服务器地址、认证信息、目标路径等。

---

**备注:** 此列表旨在提供一个概览，具体实现中可能需要更详细的配置项。建议使用配置文件 (如 `.env`, `config.yaml`) 来管理这些外部输入和密钥。
