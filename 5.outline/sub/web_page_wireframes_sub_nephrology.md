# 核心页面内容框架及布局建议: 肾功能检测产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将肾功能检测相关关键词（如尿微量白蛋白检测, 肌酐检测）的自然搜索流量提高 15%，并将来自此页面的产品详情页点击率提高 10%，支持相关产品线的销售线索增长。
    *   次要: 提升 reOpenTest 在肾功能快速检测领域的品牌认知度和专业形象，强调其在早期肾损伤筛查中的价值。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 肾功能检测]

    <header class="page-header">
      <h1>[H1: 肾功能快速检测解决方案 / reOpenTest 肾功能诊断产品]</h1>
      <p class="intro-paragraph">
        [引言: 简述肾功能检测在维护健康和管理慢性病（尤其是糖尿病、高血压并发症）中的重要性，强调早期发现肾损伤的意义。突出 reOpenTest 解决方案的优势：准确、可靠、便捷，助力早期干预。自然融入核心关键词。]
      </p>
    </header>

    <nav class="sub-category-nav">
      <ul>
        <li><a href="#early-markers">[早期肾损伤标志物 (重点: mAlb)]</a></li>
        <li><a href="#assessment-markers">[肾功能评估指标 (重点: Cr)]</a></li>
        <li><a href="#other-markers" style="display: [根据是否有其他指标产品决定 none 或 inline-block];">[其他肾功能指标 (如有)]</a></li>
        <!-- Add other sub-categories if applicable -->
      </ul>
    </nav>

    <section id="early-markers" class="product-list-section">
      <h2>[子标题: 早期肾损伤标志物]</h2>
      <div class="filters-toolbar">
        [筛选控件: 按检测项目 (例如: mAlb), 样本类型 (尿液), 方法学 (如适用)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each early marker product, especially mAlb -->
        <div class="product-card highlight-malb"> <!-- Highlight mAlb card if needed -->
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (例如: 尿微量白蛋白 (mAlb) 快速检测)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义 (例如 早期肾损伤筛查)]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="assessment-markers" class="product-list-section">
      <h2>[子标题: 肾功能评估指标]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按检测项目 (例如: Cr), 样本类型 (血清/血浆 - 如有, 尿液), 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each assessment marker product, especially Cr -->
        <div class="product-card highlight-cr"> <!-- Highlight Cr card if needed -->
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (例如: 肌酐 (Cr) 快速检测)]</h3>
          <p class="key-features">[关键特性简述: 样本类型, 检测时间, 预期用途/临床意义]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取说明书]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="other-markers" class="product-list-section" style="display: [根据是否有其他指标产品决定 none 或 block];">
      <h2>[子标题: 其他肾功能指标]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按检测项目 (例如: BUN), 样本类型, 方法学 (如适用)]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each other marker product -->
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

    <section class="value-proposition-section" style="background-color: var(--secondary-color-light, #e8f4fc);"> <!-- Optional section, focus on early detection value -->
      <h2>[标题: 早期筛查，守护肾脏健康]</h2>
      <div class="value-points">
        <div class="point">
          <i class="icon-[早期预警]"></i>
          <h3>[早期发现肾损伤]</h3>
          <p>[强调尿微量白蛋白 (mAlb) 等指标在早期肾损伤筛查中的重要性，尤其对糖尿病/高血压患者]</p>
        </div>
        <div class="point">
          <i class="icon-[可靠性]"></i>
          <h3>[结果准确可靠]</h3>
          <p>[展示相关认证 (CE, ISO) 或性能验证信息，建立信任]</p>
        </div>
        <div class="point">
          <i class="icon-[便捷性]"></i>
          <h3>[检测方便快捷]</h3>
          <p>[突出尿液检测等方法的便捷性]</p>
        </div>
      </div>
    </section>

    <section class="related-resources-section">
      <h2>[标题: 了解肾脏健康与检测 / 相关资源]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "尿微量白蛋白：为何需要关注？"]</a></li>
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "慢性肾脏病的早期信号"]</a></li>
        <li><a href="[疾病科普页面链接]">[疾病科普页面: 例如 慢性肾脏病 (CKD)]</a></li>
        <li><a href="[疾病科普页面链接]">[疾病科普页面: 例如 糖尿病肾病]</a></li>
        <li><a href="[技术文档/白皮书链接]">[技术文档/白皮书标题: 例如 "reOpenTest mAlb/Cr 检测性能研究"]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background">
      <h2>[标题: 获取肾功能检测产品详细信息]</h2>
      <div class="cta-buttons">
        <a href="[产品手册下载链接]" class="button primary">[CTA: 下载产品手册]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售顾问]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 获取报价]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[早期肾损伤检测信息链接]">了解早期肾损伤检测</a> | <a href="[技术规格汇总页链接]">查看技术规格</a>
      </div>
    </section>

    [页脚 Footer]
    ```

*   **布局建议:**
    *   **整体:** 采用单栏布局，结构清晰。子分类导航置于引言下方。
    *   **头部:** 页面标题和引言居中或左对齐。
    *   **子分类导航:** 水平导航栏，样式简洁。
    *   **产品列表:** 每个子分类下使用网格布局 (Grid)，每行显示 3-4 个产品卡片。mAlb 和 Cr 产品卡片可考虑视觉上略微突出。筛选/排序工具栏置于每个子分类列表上方。
    *   **价值主张/资源/CTA 区块:** 作为独立的横向区块，内容居中或采用多列布局。价值主张部分重点突出早期筛查的优势。
    *   **响应式:** 确保在小屏幕上布局合理调整，导航可能折叠，产品卡片变为单列或双列。

    **布局示意 (ASCII Art):**

    ```
    +-----------------------------------------------------------+
    | Breadcrumbs: Home > Products > Clinical > Nephrology      |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h1>Page Title (Renal Function)</h1>                 |
    |      <p>Introduction paragraph... focus on early detection</p>|
    |                                                           |
    +-----------------------------------------------------------+
    | [Early Markers (mAlb)] | [Assessment (Cr)] | [Others (Opt)]| <- Sub-category Nav
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>Early Kidney Injury Markers</h2>                 |
    | Filters: [Test] [Sample] | Sort: [Default]                |
    | +-------------+  +-------------+  +-------------+         |
    | | mAlb Img    |  | Other Img   |  | ...         |         | <- Highlight mAlb
    | | mAlb Test   |  | Title       |  |             |         |
    | | [View Detail] |  | [View Detail] |  |             |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      <h2>Renal Function Assessment Markers</h2>           |
    | Filters: [Test] [Sample] | Sort: [Default]                |
    | +-------------+  +-------------+  +-------------+         |
    | | Cr Img      |  | Other Img   |  | ...         |         | <- Highlight Cr
    | | Cr Test     |  | Title       |  |             |         |
    | | [View Detail] |  | [View Detail] |  |             |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      (Optional Other Markers Section)                     |
    +-----------------------------------------------------------+
    |        [Value Proposition Section - Focus Early Detection]|
    |        [Icon+Text Early] [Icon+Text Reliability] [Icon+Text Convenience] |
    +-----------------------------------------------------------+
    |             [Related Resources Section]                   |
    |             - Link mAlb Blog, CKD Blog                    |
    |             - Link CKD Info, Diabetic Nephropathy Info    |
    +-----------------------------------------------------------+
    |                  [CTA Section]                            |
    |        [Download Manual] [Contact Sales] [Quote]          |
    |        [Secondary Link Early Detection] | [Secondary Link Specs] |
    +-----------------------------------------------------------+
    |                     [Footer]                              |
    +-----------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA、标题、子分类导航选中项；辅助色 `#8dc2e8` 可用于次要按钮背景或区块背景；强调色 `#FF9800` 可用于 mAlb/Cr 相关元素的轻微强调；中性色 `#424242` 用于正文。
    *   **字体:** 标题 `Sora, sans-serif` (Bold)；正文 `Roboto, sans-serif`。
    *   **间距:** `rem` 单位，区块间距 `2rem` 或 `3rem`，列表内间距 `1rem`。
    *   **UI 元素:** 按钮、卡片使用圆角矩形。子分类导航样式简洁。图标使用线性图标。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/nephrology` 或 `/products/clinical-diagnostics/renal-function`
    *   **Title:** `肾功能快速检测 | 尿微量白蛋白 & 肌酐检测 | reOpenTest`
    *   **Meta Description:** `reOpenTest 提供准确可靠的肾功能快速检测产品，包括尿微量白蛋白 (mAlb) 和肌酐 (Cr)，助力早期肾损伤筛查和慢性肾病管理。`
    *   **Keywords:** 肾功能检测, 肾脏病检测, 尿微量白蛋白检测, mAlb test, 肌酐检测, Cr test, 早期肾损伤, CKD 检测, 快速诊断试剂, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关疾病科普页（CKD, 糖尿病肾病）、相关博客文章。
    *   **从此页链接出:** 必须链接到所有列出的肾功能产品详情页（特别是 mAlb/Cr）、产品手册下载链接、联系/报价页面、相关资源链接页面（博客、疾病科普、技术文档等）。

*   **备注:**
    *   产品列表和子分类需要根据实际产品线动态生成。
    *   页面内容和价值主张应重点突出早期筛查（特别是 mAlb）的价值。
    *   确保子分类导航链接 (`#early-markers`, `#assessment-markers` 等) 能正确跳转。
