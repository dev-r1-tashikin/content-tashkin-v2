# 资产管理流程说明 (Asset Management Process Documentation)

**目的:** 描述网站内容所需资产（图片、图标、视频、文档等）从建议、生成/选择、存储到最终在内容中引用的完整流程。

**版本:** 1.0
**创建日期:** 2025-03-27

---

## 1. 流程概述

本流程旨在确保所有网站资产得到有效管理，包括需求提出、生成或选择、标准化存储以及在最终内容中的正确引用。涉及的主要 Agent 包括 `ContentWriter`, `AssetGenerationAgent`, 和 (可选的) `AssetManagerAgent`。

## 2. 流程步骤

1.  **资产需求提出 (`ContentWriter`):**
    *   **触发:** `ContentWriter` 在根据 Prompt (`Template_Prompt_PageWriter.md`) 生成页面内容 JSON (`6_Detail/Pages/...`) 时。
    *   **动作:**
        *   识别页面内容所需的视觉或其他资产（图片、图标、视频、PDF 文档等）。
        *   在输出的 JSON 文件中的 `suggested_assets` 部分，为每个所需资产创建一个条目。
        *   每个条目应包含：
            *   `suggested_name`: 建议的文件名（不含扩展名），遵循命名规范（例如，包含页面标识）。
            *   `type`: 资产类型 (`image`, `icon`, `video`, `document`)。
            *   `prompt` (对于 AI 生成的资产): 详细的生成提示，描述内容、风格、尺寸等要求 (参考 `Template_Prompt_ImageGenerator.md`)。
            *   `alt` (对于图片): 描述性的 alt 文本。
            *   `source_description` (对于非 AI 生成资产): 描述资产来源或提供现有资产的链接/路径。
    *   **输出:** 包含 `suggested_assets` 列表的页面内容 JSON 文件。

2.  **资产生成/选择 (`AssetGenerationAgent` / Manual):**
    *   **触发:** `ProjectManager` 或自动化脚本在内容 JSON 审核通过后，解析 `suggested_assets` 列表。
    *   **动作 (自动化 - `AssetGenerationAgent`):**
        *   接收 `suggested_assets` 中需要 AI 生成的条目。
        *   使用 `Template_Prompt_ImageGenerator.md` (或其他类型生成器的模板) 和相关上下文（如视觉指南）作为输入。
        *   调用 AI 生成模型生成资产。
        *   将生成的资产文件临时存储或直接按规范命名存入 `8_Assets/` 下的对应子目录 (如 `images`, `icons`)。
        *   输出包含生成成功的资产及其最终存储路径（或临时路径）的列表。
    *   **动作 (手动):**
        *   人工审核 `suggested_assets` 列表。
        *   根据 `prompt` 或 `source_description` 手动创建、编辑或从图库选择资产。
        *   将最终资产按规范命名存入 `8_Assets/` 下的对应子目录。
        *   手动记录最终资产的存储路径。
    *   **输出:** 最终确定的资产文件（已存储）和包含其最终相对路径的列表。

3.  **路径更新 (`AssetManagerAgent` - 可选 / `WebDeveloperAgent` / Manual):**
    *   **触发:** 资产生成/选择完成。
    *   **动作 (`AssetManagerAgent` - 如果定义):**
        *   接收最终资产路径列表和对应的页面内容 JSON 文件路径。
        *   读取内容 JSON 文件。
        *   根据 `suggested_name` 或其他标识符，在 JSON 的 `content.sections` 中找到引用该资产的位置（例如，`image.src`, `video.src`, `download_link.url`）。
        *   将占位符或临时路径更新为最终的相对路径 (相对于网站根目录或代码结构)。
        *   保存更新后的内容 JSON 文件。
    *   **动作 (`WebDeveloperAgent`):**
        *   `WebDeveloperAgent` 在生成代码时，直接接收最终资产路径列表作为输入，并在代码中引用正确的路径。这种方式下，内容 JSON 中的 `src` 可能保持为空或仅包含建议名称。
    *   **动作 (手动):**
        *   人工编辑内容 JSON 文件或最终的网站代码，填入正确的资产路径。
    *   **输出:** 更新了资产路径的内容 JSON 文件 或 直接在代码中使用了正确路径。

## 3. 存储结构

所有最终资产应存储在 `8_Assets/` 目录下，并按类型分子目录：

*   `8_Assets/images/`: 存放图片文件 (jpg, png, webp, svg 等)。
*   `8_Assets/icons/`: 存放图标文件 (svg, png 等)。
*   `8_Assets/videos/`: 存放视频文件 (mp4, webm 等)。
*   `8_Assets/documents/`: 存放可供下载的文档 (pdf, docx 等)。

文件名应遵循项目命名规范，例如包含阶段编号 (8)、Agent 角色 (AssetGenerationAgent)、类型 (Image)、具体标识 (HeroBackgroundHomePage) 等。
示例: `8_Assets/images/8_AssetGenerationAgent_Image_HeroBackgroundHomePage.jpg`

## 4. 引用规范

在内容 JSON 或最终代码中引用资产时，应使用相对于网站根目录或代码结构的标准相对路径。
示例: `/assets/images/8_AssetGenerationAgent_Image_HeroBackgroundHomePage.jpg` (假设 `8_Assets` 目录最终会映射到网站的 `/assets` 路径下)

---

**备注:** 流程的自动化程度（特别是步骤 2 和 3）取决于具体的技术实现和 Agent 能力。手动步骤可作为自动化未完全实现时的补充。
