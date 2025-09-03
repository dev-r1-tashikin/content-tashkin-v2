# 网站内容生成 - 分阶段执行计划 (Phased Execution Plan)

**项目名称/版本:** [项目名称或标识]
**计划创建日期:** [YYYY-MM-DD]
**负责人 (Coordinator):** [Project_Manager 或协调者姓名/ID]

---

**目标:** 本计划旨在定义网站内容生成的分阶段目标和执行顺序，并明确各阶段开始前必须准备就绪的输入物料，以确保 AutoGen 团队按计划、有序地完成内容创建任务。

**执行说明:** 协调者 (或自动化脚本) 应按顺序检查各阶段的“前置条件/所需物料”。只有当前置条件满足时，才启动该阶段定义的页面/内容生成任务。

---

## 阶段 1: 核心页面框架与内容 (Phase 1: Core Pages Framework & Content)

**目标:** 搭建网站核心骨架，生成关键入口页面内容，验证核心流程。

**1.1 本阶段生成页面/内容:**

*   [ ] **首页 (Home Page)**
*   [ ] **关于我们 (About Us Page)**
*   [ ] **产品总览/分类入口页 (Products Overview/Category Entry Page)**
*   [ ] **联系我们 (Contact Us Page)**
*   [ ] **(可选) 核心解决方案入口页 (Core Solutions Entry Page)**

**1.2 前置条件 / 所需物料:**

*   **策略与基础信息:**
    *   [X] 最终版网站策略文档 (`4_Strategy/4_WebsiteStrategist_Strategy_WebsiteBasic.md`)
    *   [X] 最终版品牌基础信息 (`3_Info/3_BrandStrategist_Input_BrandBasicInfo.md`)
    *   [X] 最终版品牌故事 (`3_Info/3_BrandStrategist_Content_BrandStory.md`)
    *   [X] 最终版视觉指南 (`3_Info/3_BrandStrategist_Guidance_VisualStyle.md`)
*   **简报 (Briefs):**
    *   [ ] 已批准的首页简报 (`4_Strategy/Briefs/4_ContentStrategist_Brief_Home.md`)
    *   [ ] 已批准的关于我们简报 (`4_Strategy/Briefs/4_ContentStrategist_Brief_AboutUs.md`)
    *   [ ] 已批准的产品总览/分类入口页简报 (`4_Strategy/Briefs/4_ContentStrategist_Brief_ProductsOverview.md`)
    *   [ ] 已批准的联系我们简报 (`4_Strategy/Briefs/4_ContentStrategist_Brief_ContactUs.md`)
    *   [ ] (可选) 已批准的核心解决方案入口页简报
*   **线框图 (Wireframes):**
    *   [ ] 已批准的首页线框图 (`5_Outline/Sub/5_UXDesigner_Wireframe_Home.md`)
    *   [ ] 已批准的关于我们线框图 (`5_Outline/Sub/5_UXDesigner_Wireframe_AboutUs.md`)
    *   [ ] 已批准的产品总览/分类入口页线框图 (`5_Outline/Sub/5_UXDesigner_Wireframe_ProductsOverview.md`)
    *   [ ] 已批准的联系我们线框图 (`5_Outline/Sub/5_UXDesigner_Wireframe_ContactUs.md`)
    *   [ ] (可选) 已批准的核心解决方案入口页线框图
*   **其他:**
    *   [ ] (如有) 核心关键词列表 (来自 `KeywordAgent` 或策略文档)

**1.3 预期产出:**

*   上述页面的**源语言**内容 JSON 文件 (位于 `6_Detail/Pages/[source_lang]/`)
*   (如果执行翻译) 上述页面的**目标语言**内容 JSON 文件 (位于 `6_Detail/Pages/[target_lang]/`)
*   上述页面的 SEO Schema 文件 (可能分语言存放于 `7_SEO/[lang]/`)
*   (可选) 上述页面的初步代码文件 (位于 `9_WebsiteCode/`, 可能需要处理 i18n)

---

## 阶段 2: 主要产品/解决方案详情页 (Phase 2: Main Product/Solution Detail Pages)

**目标:** 生成核心产品线或关键解决方案的详细介绍页面。

**2.1 本阶段生成页面/内容:**

*   [ ] **产品详情页 - 产品 A** (例如: COVID-19 抗原检测)
*   [ ] **产品详情页 - 产品 B** (例如: DOA 尿液检测杯)
*   [ ] **产品详情页 - 产品 C** (例如: 早孕检测试纸)
*   [ ] **解决方案详情页 - 方案 X** (例如: 大规模筛查方案)
*   [ ] **(其他核心产品/方案)...**

**2.2 前置条件 / 所需物料:**

*   **阶段 1 完成状态:** [ ] 阶段 1 已完成并通过审核。
*   **简报 (Briefs):**
    *   [ ] 已批准的产品 A 简报 (`4_Strategy/Briefs/4_ContentStrategist_Brief_ProductA.md`)
    *   [ ] 已批准的产品 B 简报
    *   [ ] 已批准的产品 C 简报
    *   [ ] 已批准的解决方案 X 简报
    *   [ ] ...
*   **线框图 (Wireframes):**
    *   [ ] 已批准的产品详情页通用线框图 (或特定产品的线框图)
    *   [ ] 已批准的解决方案详情页通用线框图 (或特定方案的线框图)
*   **详细产品/方案信息:**
    *   [ ] 产品 A 的详细规格、特点、优势、说明书等信息源
    *   [ ] 产品 B 的详细信息源
    *   [ ] 产品 C 的详细信息源
    *   [ ] 解决方案 X 的详细信息源 (包含关联产品、案例等)
    *   [ ] ...
*   **其他:**
    *   [ ] (如有) 各产品/方案的特定关键词列表

**2.3 预期产出:**

*   上述页面的**源语言**内容 JSON 文件 (位于 `6_Detail/Pages/[source_lang]/`)
*   (如果执行翻译) 上述页面的**目标语言**内容 JSON 文件 (位于 `6_Detail/Pages/[target_lang]/`)
*   上述页面的 SEO Schema 文件 (可能分语言存放于 `7_SEO/[lang]/`)
*   (可选) 上述页面的代码文件 (位于 `9_WebsiteCode/`, 可能需要处理 i18n)

---

## 阶段 3: 次要页面与支持性内容 (Phase 3: Secondary Pages & Supporting Content)

**目标:** 完善网站结构，生成支持性页面和初步的博客/新闻内容。

**3.1 本阶段生成页面/内容:**

*   [ ] **支持与资源页 (Support/Resources Page)**
*   [ ] **FAQ 页面**
*   [ ] **博客/新闻列表页 (Blog/News Listing Page)**
*   [ ] **博客文章 1 (Blog Post 1)**
*   [ ] **博客文章 2 (Blog Post 2)**
*   [ ] **(其他次要分类页、案例研究页等)...**

**3.2 前置条件 / 所需物料:**

*   **阶段 2 完成状态:** [ ] 阶段 2 已完成并通过审核。
*   **简报 (Briefs):**
    *   [ ] 已批准的支持与资源页简报
    *   [ ] 已批准的 FAQ 页面简报 (可能需要用户问题输入)
    *   [ ] 已批准的博客列表页简报
    *   [ ] 已批准的博客文章 1 简报 (包含主题、关键词、要点)
    *   [ ] 已批准的博客文章 2 简报
    *   [ ] ...
*   **线框图 (Wireframes):**
    *   [ ] 已批准的相关页面线框图
*   **其他:**
    *   [ ] FAQ 问题列表
    *   [ ] 博客文章主题和初步资料

**3.3 预期产出:**

*   上述页面的**源语言**内容 JSON 文件 (位于 `6_Detail/Pages/[source_lang]/`)
*   (如果执行翻译) 上述页面的**目标语言**内容 JSON 文件 (位于 `6_Detail/Pages/[target_lang]/`)
*   上述页面的 SEO Schema 文件 (可能分语言存放于 `7_SEO/[lang]/`)
*   (可选) 上述页面的代码文件 (位于 `9_WebsiteCode/`, 可能需要处理 i18n)

---

## (后续阶段 - 可根据需要添加)

*   **阶段 4: 深度内容与优化 (Phase 4: In-depth Content & Optimization)**
    *   目标: 生成白皮书、深度技术文章、进行 A/B 测试内容准备等。
    *   ...
*   **阶段 5: 本地化/多语言内容 (Phase 5: Localization/Multilingual Content)**
    *   目标: 生成其他语言版本的内容。
    *   ...

---
