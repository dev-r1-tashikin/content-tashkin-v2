# 核心页面内容框架及布局建议: 免疫学与炎症产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将免疫学与炎症相关关键词（如 CRP 检测, PCT 检测）的自然搜索流量提高 15%，并将来自此页面的产品详情页点击率提高 10%，支持相关产品线的销售线索增长。
    *   次要: 提升 reOpenTest 在免疫与炎症快速诊断领域的品牌认知度和专业形象，特别是在感染和炎症评估方面。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 免疫学与炎症]

    <header class="page-header">
      <h1>[H1: 免疫学与炎症快速检测解决方案 / reOpenTest 免疫与炎症诊断产品]</h1>
      <p class="intro-paragraph">
        [引言: 简述免疫学与炎症标志物检测在临床实践中的重要性，特别是在感染、炎症性疾病和自身免疫性疾病的诊断与管理方面。突出 reOpenTest 解决方案的优势：快速、可靠，辅助关键临床决策（如区分感染类型）。自然融入核心关键词。]
      </p>
    </header>

    <nav class="sub-category-nav">
      <ul>
        <li><a href="#inflammation-markers">[炎症标志物检测 (重点: CRP, PCT)]</a></li>
        <li><a href="#allergy" style="display: [根据是否有过敏产品决定 none 或 inline-block];">[过敏检测 (如有)]</a></li>
        <li><a href="#autoimmune" style="display: [根据是否有自身免疫产品决定 none 或 inline-block];">[自身免疫性疾病检测 (如有)]</a></li>
        <!-- Add other sub-categories if applicable -->
      </ul>
    </nav>

    <section id="inflammation-markers" class="product-list-section">
      <h2>[子标题: 炎症标志物检测]</h2>
      <div class="filters-toolbar">
        [筛选控件: 按检测项目 (例如: CRP, PCT), 样本类型 (全血/血清/血浆), 方法学 (如适用)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each inflammation marker product, especially CRP & PCT -->
        <div class="product-card highlight-crp-pct"> <!-- Highlight CRP/PCT cards if needed -->
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (例如: CRP 快速检测 / PCT 快速检测)]</h3>
          <p class="key-features">[关键特性简述: 检测时间, 样本类型, 预期用途/临床意义 (例如 辅助细菌感染诊断)]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="allergy" class="product-list-section" style="display: [根据是否有过敏产品决定 none 或 block];">
      <h2>[子标题: 过敏检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按过敏原类型, 样本类型, 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each allergy product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测项目)]</h3>
          <p class="key-features">[关键特性简述: 检测时间, 样本类型, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="autoimmune" class="product-list-section" style="display: [根据是否有自身免疫产品决定 none 或 block];">
      <h2>[子标题: 自身免疫性疾病检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按检测项目, 样本类型, 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each autoimmune product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测项目)]</h3>
          <p class="key-features">[关键特性简述: 检测时间, 样本类型, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <!-- Add other sub-category sections if applicable -->

    <section class="value-proposition-section" style="background-color: var(--secondary-color-light, #e8f4fc);"> <!-- Optional section, focus on CRP/PCT value -->
      <h2>[标题: 快速评估感染与炎症，支持及时干预]</h2>
      <div class="value-points">
        <div class="point">
          <i class="icon-[速度]"></i>
          <h3>[快速获取关键指标]</h3>
          <p>[强调快速 CRP/PCT 检测对于急诊和感染控制的重要性]</p>
        </div>
        <div class="point">
          <i class="icon-[鉴别诊断]"></i>
          <h3>[辅助鉴别诊断]</h3>
          <p>[突出 PCT 等指标在区分细菌/病毒感染中的价值，展示认证 (CE, ISO)]</p>
        </div>
        <div class="point">
          <i class="icon-[病情评估]"></i>
          <h3>[动态监测病情]</h3>
          <p>[简述 CRP/PCT 在评估炎症程度和治疗反应中的作用]</p>
        </div>
      </div>
    </section>

    <section class="related-resources-section">
      <h2>[标题: 深入了解免疫与炎症检测 / 相关资源]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "CRP 与 PCT：理解炎症标志物"]</a></li>
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "脓毒症的早期诊断挑战"]</a></li>
        <li><a href="[疾病科普页面链接]">[疾病科普页面: 例如 脓毒症 (Sepsis)]</a></li>
        <li><a href="[技术文档/白皮书链接]">[技术文档/白皮书标题: 例如 "reOpenTest CRP/PCT 检测性能评估"]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background">
      <h2>[标题: 获取免疫学与炎症产品详细信息]</h2>
      <div class="cta-buttons">
        <a href="[产品手册下载链接]" class="button primary">[CTA: 下载产品手册]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售顾问]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 获取报价]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[CRP/PCT 产品详情页链接]">了解 CRP/PCT 检测原理</a> | <a href="[临床应用案例链接]">查看临床应用案例</a>
      </div>
    </section>

    [页脚 Footer]
    ```

*   **布局建议:**
    *   **整体:** 采用单栏布局，结构清晰。子分类导航置于引言下方。
    *   **头部:** 页面标题和引言居中或左对齐。
    *   **子分类导航:** 水平导航栏，样式简洁。
    *   **产品列表:** 每个子分类下使用网格布局 (Grid)，每行显示 3-4 个产品卡片。CRP/PCT 产品卡片可考虑视觉上略微突出。筛选/排序工具栏置于每个子分类列表上方。
    *   **价值主张/资源/CTA 区块:** 作为独立的横向区块，内容居中或采用多列布局。价值主张部分重点突出 CRP/PCT 的优势。
    *   **响应式:** 确保在小屏幕上布局合理调整，导航可能折叠，产品卡片变为单列或双列。

    **布局示意 (ASCII Art):**

    ```
    +-----------------------------------------------------------+
    | Breadcrumbs: Home > Products > Clinical > Immunology      |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h1>Page Title (Immunology & Inflammation)</h1>      |
    |      <p>Introduction paragraph... focus on CRP/PCT</p>    |
    |                                                           |
    +-----------------------------------------------------------+
    | [Inflammation (CRP/PCT)] | [Allergy (Opt)] | [Autoimmune (Opt)] | <- Sub-category Nav
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>Inflammation Marker Detection</h2>               |
    | Filters: [Test] [Sample] | Sort: [Default]                |
    | +-------------+  +-------------+  +-------------+         |
    | | CRP Img     |  | PCT Img     |  | Other Img   |         | <- Highlight CRP/PCT
    | | CRP Test    |  | PCT Test    |  | Title       |         |
    | | [View Detail] |  | [View Detail] |  | [View Detail] |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      (Optional Allergy Detection Section)                 |
    +-----------------------------------------------------------+
    |      (Optional Autoimmune Detection Section)              |
    +-----------------------------------------------------------+
    |        [Value Proposition Section - Focus CRP/PCT]        |
    |        [Icon+Text Speed] [Icon+Text Differentiation] [Icon+Text Monitoring] |
    +-----------------------------------------------------------+
    |             [Related Resources Section]                   |
    |             - Link CRP/PCT Blog                           |
    |             - Link Sepsis Info                            |
    +-----------------------------------------------------------+
    |                  [CTA Section]                            |
    |        [Download Manual] [Contact Sales] [Quote]          |
    |        [Secondary Link CRP/PCT] | [Secondary Link Cases]  |
    +-----------------------------------------------------------+
    |                     [Footer]                              |
    +-----------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA、标题、子分类导航选中项；辅助色 `#8dc2e8` 可用于次要按钮背景或区块背景；强调色 `#FF9800` 可用于 CRP/PCT 相关元素的轻微强调；中性色 `#424242` 用于正文。
    *   **字体:** 标题 `Sora, sans-serif` (Bold)；正文 `Roboto, sans-serif`。
    *   **间距:** `rem` 单位，区块间距 `2rem` 或 `3rem`，列表内间距 `1rem`。
    *   **UI 元素:** 按钮、卡片使用圆角矩形。子分类导航样式简洁。图标使用线性图标。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/immunology-inflammation`
    *   **Title:** `免疫与炎症快速检测 | CRP & PCT 检测 | reOpenTest`
    *   **Meta Description:** `reOpenTest 提供快速可靠的免疫学与炎症标志物检测，包括 CRP 和 PCT，辅助感染评估与鉴别诊断。了解我们的解决方案。`
    *   **Keywords:** 免疫检测, 炎症检测, CRP 检测, PCT 检测, C反应蛋白, 降钙素原, 炎症标志物, 脓毒症标志物, 快速诊断试剂, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关疾病科普页（脓毒症）、解决方案页（急诊科/ICU）、相关博客文章。
    *   **从此页链接出:** 必须链接到所有列出的免疫学与炎症产品详情页（特别是 CRP/PCT）、产品手册下载链接、联系/报价页面、相关资源链接页面（博客、疾病科普、技术文档等）。

*   **备注:**
    *   产品列表和子分类需要根据实际产品线动态生成，确认是否有过敏和自身免疫产品。
    *   页面内容和价值主张应重点突出 CRP 和 PCT 检测的优势和应用场景。
    *   确保子分类导航链接 (`#inflammation-markers`, `#allergy` 等) 能正确跳转。
