# 文件状态管理说明 (Status Management Documentation)

**目的:** 定义项目文件中 `[状态]` 标识 (如 `draft`, `review`, `final`) 的使用规则、流转机制和管理方式。

**版本:** 1.0
**创建日期:** 2025-03-27

---

## 1. 状态定义

本项目主要使用以下文件状态标识（附加在文件名主体和扩展名之间，用点 `.` 分隔）：

*   **`.draft`:**
    *   含义: 文件是初稿或正在进行中的版本，尚未经过正式审核。
    *   使用者: 主要由创建内容的 Agent (如 `ContentStrategist`, `UX_Designer`, `ContentWriter`) 在首次生成文件时使用。
    *   示例: `4_Strategy/4_WebsiteStrategist_Strategy_WebsiteBasic.draft.md`
*   **`.review`:**
    *   含义: 文件已完成草稿，提交进行审核。
    *   使用者: 当一个 `.draft` 文件准备好被审核时，可以将其重命名（或复制）为 `.review` 版本，并触发审核流程。审核意见可以记录在同名的 `.review.md` 文件中，或者直接在此文件上进行注释（取决于审核流程设计）。
    *   示例: `5_Outline/Sub/5_UXDesigner_Wireframe_Home.review.md` (表示此线框图待审核)
*   **(无状态标识 / `final`):**
    *   含义: 文件已通过审核，是当前阶段的最终、稳定版本，可以被后续流程安全使用。
    *   使用者: 当 `.review` 文件通过审核后，应将其重命名，移除状态标识（或明确标记为 `.final`，但通常省略更简洁）。
    *   示例: `3_Info/3_BrandStrategist_Content_BrandStory.md` (表示这是最终的品牌故事文档)

## 2. 状态流转规则

1.  **创建:** Agent 生成新文件时，通常应标记为 `.draft`。
    *   `Agent A` -> `FileName.draft.ext`
2.  **提交审核:** 当 `.draft` 文件完成后，由 `Agent A` 或 `ProjectManager` 将其标记为 `.review` (通常通过重命名或复制)，并通知/触发 `ReviewerAgent`。
    *   `FileName.draft.ext` -> `FileName.review.ext` (提交审核)
3.  **审核:** `ReviewerAgent` 对 `.review` 文件进行审核。
    *   **审核通过:**
        *   `ReviewerAgent` 输出审核通过的结论。
        *   `ProjectManager` 或自动化脚本将 `.review` 文件重命名，移除状态标识，使其成为最终版本。
        *   `FileName.review.ext` -> `FileName.ext` (审核通过)
    *   **需要修改:**
        *   `ReviewerAgent` 输出具体的修改意见 (可能记录在 `FileName.review.md` 或其他地方)。
        *   文件保持 `.review` 状态 (或退回 `.draft` 状态，取决于流程设计)。
        *   `ProjectManager` 将修改任务分配回 `Agent A`。
        *   `Agent A` 修改后，重新提交审核 (回到步骤 2)。

## 3. 管理方式

*   **自动化:** 理想情况下，状态流转（特别是审核通过后的重命名）应由工作流编排脚本或 `ProjectManager` Agent 自动处理。
*   **手动:** 在自动化未完全实现时，可由人工项目经理根据审核结果手动重命名文件。
*   **版本控制:** 建议使用 Git 等版本控制系统管理所有文件，包括不同状态的版本，以便追踪历史记录和进行回滚。`.draft` 和 `.review` 文件可以视为开发分支上的临时状态，最终合并到主分支的是移除状态标识的 `final` 版本。

## 4. 文件引用

*   后续 Agent 在其输入中应优先引用**没有状态标识**的最终版本文件。
*   只有在特定流程（如审核、基于草稿的迭代）中，才应引用带有 `.draft` 或 `.review` 状态的文件。

---

**备注:** 清晰的状态管理有助于避免在工作流程中使用错误的或未审核的文件版本，确保流程的稳定性和产出物的质量。
