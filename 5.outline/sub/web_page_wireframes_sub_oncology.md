# 核心页面内容框架及布局建议: 肿瘤标志物检测产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将肿瘤标志物检测相关关键词（如 CEA 检测, AFP 检测, PSA 检测）的自然搜索流量提高 15%，并将来自此页面的产品详情页点击率提高 10%，支持相关产品线的销售线索增长。
    *   次要: 提升 reOpenTest 在肿瘤标志物快速检测领域的品牌认知度和专业形象。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 肿瘤学]

    <header class="page-header">
      <h1>[H1: 肿瘤标志物快速检测解决方案 / reOpenTest 肿瘤学诊断产品]</h1>
      <p class="intro-paragraph">
        [引言: 简述肿瘤标志物检测在肿瘤诊疗过程中的作用（辅助诊断、监测等），强调其临床价值。突出 reOpenTest 解决方案的优势：准确、可靠、高效。自然融入核心关键词。**注意：强调是辅助诊断和监测作用。**]
      </p>
    </header>

    <nav class="sub-category-nav">
      <ul>
        <li><a href="#digestive-markers">[消化系统肿瘤标志物 (如 CEA, AFP)]</a></li>
        <li><a href="#prostate-markers" style="display: [根据是否有 PSA 产品决定 none 或 inline-block];">[前列腺癌标志物 (如 PSA)]</a></li>
        <li><a href="#other-markers" style="display: [根据是否有其他类别产品决定 none 或 inline-block];">[其他肿瘤标志物 (如有)]</a></li>
        <!-- Add other sub-categories if applicable -->
      </ul>
    </nav>

    <section id="digestive-markers" class="product-list-section">
      <h2>[子标题: 消化系统肿瘤标志物]</h2>
      <div class="filters-toolbar">
        [筛选控件: 按检测标志物 (例如: CEA, AFP, CA19-9), 样本类型 (血清/血浆), 方法学 (如适用)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each digestive marker product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测标志物)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义 (例如 辅助诊断/监测)]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="prostate-markers" class="product-list-section" style="display: [根据是否有 PSA 产品决定 none 或 block];">
      <h2>[子标题: 前列腺癌标志物]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按检测标志物 (例如: PSA), 样本类型 (血清/血浆), 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each prostate marker product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (例如: PSA 快速检测)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="other-markers" class="product-list-section" style="display: [根据是否有其他类别产品决定 none 或 block];">
      <h2>[子标题: 其他肿瘤标志物]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按检测标志物, 样本类型, 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each other marker product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测标志物)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <!-- Add other sub-category sections if applicable -->

    <section class="value-proposition-section" style="background-color: var(--secondary-color-light, #e8f4fc);"> <!-- Optional section -->
      <h2>[标题: 可靠检测，辅助肿瘤管理]</h2>
      <div class="value-points">
        <div class="point">
          <i class="icon-[准确性]"></i>
          <h3>[结果准确，值得信赖]</h3>
          <p>[强调质量控制和检测准确性对于肿瘤标志物检测的重要性]</p>
        </div>
        <div class="point">
          <i class="icon-[可靠性]"></i>
          <h3>[性能可靠，稳定一致]</h3>
          <p>[展示相关认证 (CE, ISO) 或性能验证信息]</p>
        </div>
        <div class="point">
          <i class="icon-[效率]"></i>
          <h3>[快速高效，辅助决策]</h3>
          <p>[突出快速检测在临床流程中的效率优势]</p>
        </div>
      </div>
    </section>

    <section class="related-resources-section">
      <h2>[标题: 深入了解肿瘤标志物检测 / 相关资源]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "常见肿瘤标志物解读"]</a></li>
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "PSA 在前列腺癌筛查中的应用"]</a></li>
        <li><a href="[技术文档/白皮书链接]">[技术文档/白皮书标题: 例如 "reOpenTest CEA 检测性能评估"]</a></li>
        <li><a href="[临床研究摘要链接]">[临床研究摘要标题 (如有)]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background">
      <h2>[标题: 获取肿瘤标志物检测产品详细信息]</h2>
      <div class="cta-buttons">
        <a href="[产品手册下载链接]" class="button primary">[CTA: 下载产品手册]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售顾问]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 获取报价]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[检测技术信息链接]">了解检测技术</a> | <a href="[性能数据文档链接]">查看性能数据</a>
      </div>
    </section>

    [页脚 Footer]
    ```

*   **布局建议:**
    *   **整体:** 采用单栏布局，结构清晰。子分类导航置于引言下方。
    *   **头部:** 页面标题和引言居中或左对齐。
    *   **子分类导航:** 水平导航栏，样式简洁。
    *   **产品列表:** 每个子分类下使用网格布局 (Grid)，每行显示 3-4 个产品卡片。筛选/排序工具栏置于每个子分类列表上方。
    *   **价值主张/资源/CTA 区块:** 作为独立的横向区块，内容居中或采用多列布局。
    *   **响应式:** 确保在小屏幕上布局合理调整，导航可能折叠，产品卡片变为单列或双列。

    **布局示意 (ASCII Art):**

    ```
    +-----------------------------------------------------------+
    | Breadcrumbs: Home > Products > Clinical > Oncology        |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h1>Page Title (Oncology / Cancer Markers)</h1>      |
    |      <p>Introduction paragraph... auxiliary role...</p>   |
    |                                                           |
    +-----------------------------------------------------------+
    | [Digestive (CEA/AFP)] | [Prostate (PSA)] | [Others (Opt)] | <- Sub-category Nav
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>Digestive System Tumor Markers</h2>              |
    | Filters: [Marker] [Sample] | Sort: [Default]              |
    | +-------------+  +-------------+  +-------------+         |
    | | CEA Img     |  | AFP Img     |  | ...         |         |
    | | CEA Test    |  | AFP Test    |  |             |         |
    | | [View Detail] |  | [View Detail] |  |             |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      (Optional Prostate Cancer Markers Section)           |
    | Filters: [Marker] [Sample] | Sort: [Default]              |
    | +-------------+  +-------------+  +-------------+         |
    | | PSA Img     |  | ...         |  | ...         |         |
    | | PSA Test    |  |             |  |             |         |
    | | [View Detail] |  |             |  |             |         |
    | +-------------+  +-------------+  +-------------+         |
    +-----------------------------------------------------------+
    |      (Optional Other Markers Section)                     |
    +-----------------------------------------------------------+
    |        [Value Proposition Section - Reliability/Efficiency]|
    |        [Icon+Text Accuracy] [Icon+Text Reliability] [Icon+Text Efficiency] |
    +-----------------------------------------------------------+
    |             [Related Resources Section]                   |
    |             - Link Marker Blog, PSA Blog                  |
    |             - Link Performance Doc, Clinical Study        |
    +-----------------------------------------------------------+
    |                  [CTA Section]                            |
    |        [Download Manual] [Contact Sales] [Quote]          |
    |        [Secondary Link Tech] | [Secondary Link Data]      |
    +-----------------------------------------------------------+
    |                     [Footer]                              |
    +-----------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA、标题、子分类导航选中项；辅助色 `#8dc2e8` 可用于次要按钮背景或区块背景；强调色 `#FF9800` 谨慎使用；中性色 `#424242` 用于正文。
    *   **字体:** 标题 `Sora, sans-serif` (Bold)；正文 `Roboto, sans-serif`。
    *   **间距:** `rem` 单位，区块间距 `2rem` 或 `3rem`，列表内间距 `1rem`。
    *   **UI 元素:** 按钮、卡片使用圆角矩形。子分类导航样式简洁。图标使用线性图标。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/oncology` 或 `/products/clinical-diagnostics/cancer-markers`
    *   **Title:** `肿瘤标志物快速检测 | CEA, AFP, PSA 检测 | reOpenTest`
    *   **Meta Description:** `reOpenTest 提供准确可靠的肿瘤标志物快速检测产品，包括 CEA, AFP, PSA 等，辅助癌症诊断、监测与管理。了解我们的解决方案。`
    *   **Keywords:** 肿瘤标志物检测, 癌症标志物检测, cancer marker test, CEA 检测, AFP 检测, PSA 检测, 癌胚抗原, 甲胎蛋白, 前列腺特异抗原, 快速诊断试剂, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关疾病科普页、相关博客文章。
    *   **从此页链接出:** 必须链接到所有列出的肿瘤标志物产品详情页、产品手册下载链接、联系/报价页面、相关资源链接页面（博客、技术文档、研究等）。

*   **备注:**
    *   产品列表和子分类需要根据实际产品线动态生成。
    *   务必在内容中准确传达肿瘤标志物检测的辅助作用，避免误导。
    *   确保子分类导航链接 (`#digestive-markers`, `#prostate-markers` 等) 能正确跳转。
