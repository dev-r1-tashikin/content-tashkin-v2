# 核心页面内容框架及布局建议: 心脏病学产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将心脏标志物相关关键词的自然搜索流量提高 20%，并将来自此页面的产品详情页点击率提高 15%，最终支持销售线索增长 10%。
    *   次要: 提升 reOpenTest 在心脏病快速诊断领域的品牌专业形象。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 心脏病学]

    <header class="page-header">
      <h1>[H1: 心脏标志物快速检测解决方案 / reOpenTest 心脏病学诊断产品]</h1>
      <p class="intro-paragraph">
        [引言: 强调心脏标志物检测在急诊和临床中的重要性 (例如，“时间就是心肌”)。突出 reOpenTest 解决方案的优势：快速（15分钟 USP）、可靠、全面。自然融入核心关键词。]
      </p>
    </header>

    <section class="product-list-section">
      <div class="filters-toolbar">
        [筛选控件: 按标志物 (Troponin I/T, CK-MB, Myoglobin, BNP, NT-proBNP, D-Dimer), 样本类型 (全血/血清/血浆), 检测平台 (如适用)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>

      <div class="product-grid">
        <!-- Repeat for each product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h2>[产品名称 (包含检测的标志物)]</h2>
          <p class="key-features">[关键特性简述: 检测时间、样本类型、关键性能指标摘要]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格表]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section class="value-proposition-section" style="background-color: var(--secondary-color-light, #e8f4fc);"> <!-- Optional section -->
      <h2>[标题: 为何选择 reOpenTest 心脏标志物检测?]</h2>
      <div class="value-points">
        <div class="point">
          <i class="icon-[速度]"></i>
          <h3>[快速诊断，争分夺秒]</h3>
          <p>[强调速度 (15分钟) 对改善患者预后的重要性]</p>
        </div>
        <div class="point">
          <i class="icon-[可靠性]"></i>
          <h3>[结果可靠，值得信赖]</h3>
          <p>[展示相关认证标志 (CE, ISO) 或临床验证摘要链接]</p>
        </div>
        <div class="point">
          <i class="icon-[全面]"></i>
          <h3>[全面覆盖，满足所需]</h3>
          <p>[简述产品线覆盖的主要心脏标志物]</p>
        </div>
      </div>
      [可选: 客户评价/专家引言]
    </section>

    <section class="related-resources-section">
      <h2>[标题: 深入了解心脏标志物检测 / 相关资源]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "高敏肌钙蛋白在 AMI 诊断中的应用"]</a></li>
        <li><a href="[技术文档/白皮书链接]">[文档标题: 例如 "reOpenTest 心脏标志物检测性能研究"]</a></li>
        <li><a href="[案例研究链接]">[案例研究标题 (如有)]</a></li>
        <li><a href="[Webinar 录播链接]">[Webinar 标题 (如有)]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background"> <!-- Use a distinct background -->
      <h2>[标题: 获取完整的心脏病学产品信息]</h2>
      <div class="cta-buttons">
        <a href="[产品目录下载链接]" class="button primary">[CTA: 下载心脏病学产品目录]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售代表咨询]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 请求报价]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[快速检测技术页面链接]">探索我们的快速检测技术</a> | <a href="[资源中心/研究页面链接]">阅读相关白皮书</a>
      </div>
    </section>

    [页脚 Footer]
    ```

*   **布局建议:**
    *   **整体:** 采用单栏或主内容区+侧边栏（用于筛选）的布局，保持清晰、现代感。大量留白。
    *   **头部:** 页面标题和引言居中或左对齐，占据视觉焦点。
    *   **产品列表:** 网格布局 (Grid)，每行显示 3-4 个产品卡片，确保卡片大小一致，对齐整洁。筛选/排序工具栏置于列表上方。
    *   **价值主张/资源/CTA 区块:** 作为独立的横向区块，内容居中或采用多列布局（如价值点）。CTA 区块应视觉突出。
    *   **响应式:** 确保在不同屏幕尺寸下布局能自动调整，产品卡片在小屏幕上可能变为单列或双列。

    **布局示意 (ASCII Art):**

    ```
    +------------------------------------------------------+
    | Breadcrumbs: Home > Products > Clinical > Cardiology |
    +------------------------------------------------------+
    |                                                      |
    |          <h1>Page Title (Cardiology)</h1>            |
    |          <p>Introduction paragraph...</p>             |
    |                                                      |
    +------------------------------------------------------+
    | Filters: [Marker] [Sample] [Platform] | Sort: [Default] |
    +------------------------------------------------------+
    | +-------------+  +-------------+  +-------------+    |
    | | Product Img |  | Product Img |  | Product Img |    |
    | | Title       |  | Title       |  | Title       |    |
    | | Features... |  | Features... |  | Features... |    |
    | | [View Detail] |  | [View Detail] |  | [View Detail] |    |
    | +-------------+  +-------------+  +-------------+    |
    | +-------------+  +-------------+  +-------------+    |
    | | Product Img |  | Product Img |  | Product Img |    |
    | | ...         |  | ...         |  | ...         |    |
    | +-------------+  +-------------+  +-------------+    |
    +------------------------------------------------------+
    |        [Optional Value Proposition Section]          |
    |        [Icon+Text] [Icon+Text] [Icon+Text]           |
    +------------------------------------------------------+
    |             [Related Resources Section]              |
    |             - Link 1                                 |
    |             - Link 2                                 |
    +------------------------------------------------------+
    |                  [CTA Section]                       |
    |        [Download Catalog] [Contact Sales] [Quote]    |
    |        [Secondary Link 1] | [Secondary Link 2]      |
    +------------------------------------------------------+
    |                     [Footer]                         |
    +------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA 按钮、标题强调等；辅助色 `#8dc2e8` 可用于背景区分或次要元素；强调色 `#FF9800` 用于需要特别突出的元素（谨慎使用）；中性色 `#424242` 用于正文。
    *   **字体:** 标题使用 `Sora, sans-serif` (可考虑 Bold 字重)；正文和产品描述使用 `Roboto, sans-serif`。
    *   **间距:** 使用 `rem` 单位，保持足够的留白 (例如，区块间距 `2rem` 或 `3rem`，卡片内边距 `1rem`)。
    *   **UI 元素:** 按钮、卡片使用圆角矩形，风格简洁统一。图标使用线性图标。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/cardiology` 或 `/products/cardiac-markers`
    *   **Title:** `心脏标志物快速检测 | reOpenTest 心脏病学诊断`
    *   **Meta Description:** `reOpenTest 提供快速、可靠的心脏标志物检测解决方案，包括肌钙蛋白、BNP 等。15分钟获取结果，助力临床快速决策。了解更多产品信息。`
    *   **Keywords:** 心脏标志物检测, 快速心肌标志物检测, 心肌肌钙蛋白检测, Troponin test, BNP, NT-proBNP, D-Dimer, POCT 心脏标志物, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关解决方案页（如急诊科）、相关博客文章。
    *   **从此页链接出:** 必须链接到所有列出的心脏标志物产品详情页、产品目录下载链接、联系/报价页面、相关资源链接页面（博客、技术文档等）。

*   **备注:**
    *   产品列表需要动态加载或根据实际产品数据生成。
    *   筛选功能的具体实现需要前后端配合。
    *   确保所有链接目标有效。
    *   强调速度 (15分钟) 和可靠性 (认证) 是关键卖点。
