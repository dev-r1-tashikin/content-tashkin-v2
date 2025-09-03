# 核心页面内容框架及布局建议: 胃肠道健康产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将胃肠道健康相关关键词（如幽门螺杆菌检测, 粪便潜血检测）的自然搜索流量提高 15%，并将来自此页面的产品详情页点击率提高 10%，支持相关产品线的销售线索增长。
    *   次要: 提升 reOpenTest 在胃肠道快速诊断领域的品牌认知度和专业形象。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 胃肠道健康]

    <header class="page-header">
      <h1>[H1: 胃肠道健康快速检测解决方案 / reOpenTest 胃肠道诊断产品]</h1>
      <p class="intro-paragraph">
        [引言: 简述胃肠道健康的重要性以及相关检测在疾病预防和早期诊断中的作用（例如，H. pylori 与胃溃疡/胃癌风险，FOB 与结直肠癌筛查）。突出 reOpenTest 解决方案的优势：准确、可靠、便捷（非侵入性）。自然融入核心关键词。]
      </p>
    </header>

    <nav class="sub-category-nav">
      <ul>
        <li><a href="#hpylori-detection">[幽门螺杆菌 (H. pylori) 检测]</a></li>
        <li><a href="#fob-detection">[粪便潜血 (FOB) 检测]</a></li>
        <li><a href="#pathogen-detection">[胃肠道病原体检测 (如有)]</a></li>
        <!-- Add other sub-categories if applicable -->
      </ul>
    </nav>

    <section id="hpylori-detection" class="product-list-section">
      <h2>[子标题: 幽门螺杆菌 (H. pylori) 检测]</h2>
      <div class="filters-toolbar">
        [筛选控件: 按样本类型 (粪便, 血清/血浆 - 如有), 方法学 (如适用)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each H. pylori product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测项目)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="fob-detection" class="product-list-section">
      <h2>[子标题: 粪便潜血 (FOB) 检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按样本类型 (粪便), 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each FOB product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测项目)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义 (例如 结直肠癌筛查)]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="pathogen-detection" class="product-list-section" style="display: [根据是否有此类产品决定 none 或 block];">
      <h2>[子标题: 胃肠道病原体检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按病原体 (例如: 轮状病毒, 腺病毒), 样本类型, 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each pathogen product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含检测项目)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <!-- Add other sub-category sections if applicable -->

    <section class="value-proposition-section" style="background-color: var(--secondary-color-light, #e8f4fc);"> <!-- Optional section -->
      <h2>[标题: 便捷筛查，守护胃肠健康]</h2>
      <div class="value-points">
        <div class="point">
          <i class="icon-[准确性]"></i>
          <h3>[结果准确，辅助诊断]</h3>
          <p>[强调准确检测对于胃肠道疾病诊断的重要性]</p>
        </div>
        <div class="point">
          <i class="icon-[便捷性]"></i>
          <h3>[操作便捷，易于推广]</h3>
          <p>[强调非侵入性检测 (如粪便样本) 的便捷性和患者接受度]</p>
        </div>
        <div class="point">
          <i class="icon-[早期筛查]"></i>
          <h3>[早期筛查，预防关键]</h3>
          <p>[突出 FOB 检测等在疾病早期发现中的价值]</p>
        </div>
      </div>
    </section>

    <section class="related-resources-section">
      <h2>[标题: 了解更多胃肠道健康知识 / 相关资源]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "幽门螺杆菌感染与检测"]</a></li>
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "粪便潜血：为何要做这项检查？"]</a></li>
        <li><a href="[疾病科普页面链接]">[疾病科普页面: 例如 消化性溃疡]</a></li>
        <li><a href="[疾病科普页面链接]">[疾病科普页面: 例如 结直肠癌筛查]</a></li>
        <li><a href="[技术文档/白皮书链接]">[技术文档/白皮书标题]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background">
      <h2>[标题: 获取胃肠道健康产品详细信息]</h2>
      <div class="cta-buttons">
        <a href="[产品手册下载链接]" class="button primary">[CTA: 下载产品手册]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售顾问]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 获取报价]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[H. pylori 检测信息链接]">了解 H. pylori 检测</a> | <a href="[FOB 检测信息链接]">了解 FOB 检测的重要性</a>
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
    | Breadcrumbs: Home > Products > Clinical > Gastrointestinal|
    +-----------------------------------------------------------+
    |                                                           |
    |      <h1>Page Title (Gastrointestinal Health)</h1>        |
    |      <p>Introduction paragraph...</p>                      |
    |                                                           |
    +-----------------------------------------------------------+
    | [H. pylori] | [FOB] | [Pathogens] | [Others]              | <- Sub-category Nav
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>H. pylori Detection</h2>                         |
    | Filters: [Sample] [Method] | Sort: [Default]              |
    | +-------------+  +-------------+  +-------------+         |
    | | Product Img |  | Product Img |  | Product Img |         |
    | | Title       |  | Title       |  | Title       |         |
    | | [View Detail] |  | [View Detail] |  | [View Detail] |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>FOB Detection</h2>                              |
    | Filters: [Sample] [Method] | Sort: [Default]              |
    | +-------------+  +-------------+  +-------------+         |
    | | Product Img |  | Product Img |  | Product Img |         |
    | | ...         |  | ...         |  | ...         |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      (Optional Pathogen Detection Section)                |
    +-----------------------------------------------------------+
    |        [Optional Value Proposition Section]               |
    |        [Icon+Text] [Icon+Text] [Icon+Text]                |
    +-----------------------------------------------------------+
    |             [Related Resources Section]                   |
    |             - Link 1                                      |
    |             - Link 2                                      |
    +-----------------------------------------------------------+
    |                  [CTA Section]                            |
    |        [Download Manual] [Contact Sales] [Quote]          |
    |        [Secondary Link 1] | [Secondary Link 2]           |
    +-----------------------------------------------------------+
    |                     [Footer]                              |
    +-----------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA、标题、子分类导航选中项；辅助色 `#8dc2e8` 可用于次要按钮背景或区块背景；强调色 `#FF9800` 谨慎使用；中性色 `#424242` 用于正文。
    *   **字体:** 标题 `Sora, sans-serif` (Bold)；正文 `Roboto, sans-serif`。
    *   **间距:** `rem` 单位，区块间距 `2rem` 或 `3rem`，列表内间距 `1rem`。
    *   **UI 元素:** 按钮、卡片使用圆角矩形。子分类导航样式简洁，选中项有明显区分。图标使用线性图标。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/gastrointestinal-health`
    *   **Title:** `胃肠道健康快速检测 | H. pylori & FOB 检测 | reOpenTest`
    *   **Meta Description:** `reOpenTest 提供准确、便捷的胃肠道健康快速检测方案，包括幽门螺杆菌 (H. pylori) 抗原检测和粪便潜血 (FOB) 检测，助力早期筛查与诊断。`
    *   **Keywords:** 胃肠道检测, 幽门螺杆菌检测, H. pylori test, 粪便潜血检测, FOB test, 消化道出血, 结直肠癌筛查, 快速诊断试剂, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关疾病科普页（消化性溃疡、结直肠癌）、相关博客文章。
    *   **从此页链接出:** 必须链接到所有列出的胃肠道健康产品详情页、产品手册下载链接、联系/报价页面、相关资源链接页面（博客、疾病科普、技术文档等）。

*   **备注:**
    *   产品列表和子分类需要根据实际产品线动态生成。
    *   确保子分类导航链接 (`#hpylori-detection`, `#fob-detection` 等) 能正确跳转。
    *   强调非侵入性检测的便捷性和在筛查中的重要性。
