# 文件命名规范 (File Naming Convention)

**目的:** 统一项目文件的命名方式，提高可读性、可维护性和自动化处理的便利性。

**版本:** 1.0
**制定日期:** 2025-03-27

---

## 规范格式

所有项目文件（除少数特殊配置文件外）应遵循以下命名格式：

`[阶段编号]_[主要Agent角色]_[输出类型]_[具体标识/主题]_[状态].[扩展名]`

## 各部分说明

1.  **`[阶段编号]` (Phase Number):**
    *   描述: 文件所属的主要工作流程阶段编号。
    *   格式: 数字 (1-9)。
    *   示例: `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8` (资产), `9` (代码)。
    *   对应目录: `1_Source`, `2_Report`, `3_Info`, `4_Strategy`, `5_Outline`, `6_Detail`, `7_SEO`, `8_Assets`, `9_WebsiteCode`。
    *   **多语言注意:** 在 `6_Detail/Pages` 和 `7_SEO` 等目录下，可能会根据 ISO 语言代码创建子目录 (如 `en/`, `de/`, `zh-CN/`) 来存放不同语言版本的文件。文件名本身通常保持一致，通过目录区分语言。

2.  **`[主要Agent角色]` (Primary Agent Role):**
    *   描述: 创建或主要负责该文件的 Agent 角色名称。
    *   格式: 驼峰式命名 (CamelCase)。
    *   示例: `SourceCollector`, `MarketAnalyst`, `BrandStrategist`, `InitialPlanner`, `WebsiteStrategist`, `ContentStrategist`, `StrategyAuditor`, `InformationArchitect`, `UXDesigner`, `PromptEngineer`, `ContentWriter`, `SEOSpecialist`, `AssetGenerationAgent`, `WebDeveloperAgent`, `ProjectManager`。

3.  **`[输出类型]` (Output Type):**
    *   描述: 文件的性质或内容类型。
    *   格式: 驼峰式命名 (CamelCase)。
    *   示例: `Input`, `Report`, `Plan`, `Strategy`, `Brief`, `Architecture`, `Wireframe`, `Prompt`, `Content`, `Schema`, `Guidance`, `Review`, `Script`, `Template`, `Checklist`, `Documentation`, `Image`, `Icon`, `Video`, `Document`, `CodeComponent`, `Stylesheet`, `Executable`。

4.  **`[具体标识/主题]` (Specific Identifier/Topic):**
    *   描述: 文件的具体内容标识，使其具有唯一性。可以是页面名称、产品名称、主题、功能等。
    *   格式: 驼峰式命名 (CamelCase) 或使用下划线连接的多个词 (snake_case)，保持一致性即可。建议优先使用驼峰式。
    *   示例: `Competitor1`, `MarketInfoHtmlAnalysis`, `BrandBasicInfo`, `InitialWebsite`, `WebsiteBasic`, `FemaleHormoneTesting`, `HomePage`, `ProductCovid19Antigen`, `AboutUsWriter`, `GeneratedJs`, `GetInfoGuidance`, `StrategyPlan`, `WebPageGeneric`, `Website`, `BatchInfo`, `PageWriter`, `ImageGenerator`, `WebDeveloper`, `ContentUpdate`, `BriefDocument`, `PhasedExecution`, `AgentRole`, `StructuredData`, `NamingConvention`。

5.  **`[状态]` (Status - Optional):**
    *   描述: 文件当前的状态，可选。如果省略，默认为最终版本。
    *   格式: 小写。
    *   示例: `draft`, `review`, `final` (通常省略 final)。

6.  **`[扩展名]` (Extension):**
    *   描述: 文件的标准扩展名。
    *   格式: 小写。
    *   示例: `.md`, `.html`, `.css`, `.js`, `.json`, `.run`, `.py`, `.png`, `.jpg`, `.svg`, `.pdf`, `.jsx`, `.vue`。

## 示例

*   `1_SourceCollector_Input_Competitor1.html`
*   `2_MarketAnalyst_Report_MarketInfoHtmlAnalysis.md`
*   `3_BrandStrategist_Input_BrandBasicInfo.md`
*   `4_Strategy/4_WebsiteStrategist_Strategy_WebsiteBasic.draft.md`
*   `4_Strategy/Briefs/4_ContentStrategist_Brief_FemaleHormoneTesting.draft.md`
*   `5_Outline/Sub/5_UXDesigner_Wireframe_Home.md`
*   `6_Detail/Pages/6_ContentWriter_Content_AboutUs.json` (假设内容输出为 JSON)
*   `6_Detail/Prompts/6_PromptEngineer_Prompt_ProductDetailWriter.md`
*   `7_SEO/7_SEOSpecialist_Schema_HomePage.jsonld`
*   `8_Assets/images/8_AssetGenerationAgent_Image_HeroBackground.jpg`
*   `9_WebsiteCode/src/pages/9_WebDeveloperAgent_CodeComponent_HomePage.jsx`
*   `template_System/Template_Prompt_PageWriter.md`
*   `template_System/Documentation_NamingConvention.md`

---

**备注:** 团队成员和 Agent 在创建新文件时应严格遵守此规范。
