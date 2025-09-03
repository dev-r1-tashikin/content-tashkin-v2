# 核心页面内容框架及布局建议: 传染病诊断产品分类页

*   **页面类型名称:** 产品分类页面 (Product Category Page)
*   **Schema.org `@type`:** `CollectionPage` (包含 `Product` Schema)
*   **页面目标:**
    *   主要: 在 6 个月内，将传染病诊断相关关键词的自然搜索流量提高 25%，并将来自此页面的产品详情页点击率提高 15%，最终支持传染病产品线的销售线索增长 15%。
    *   次要: 强化 reOpenTest 作为传染病快速诊断领域领导者的品牌形象，突出其产品广度、速度和可靠性。

*   **内容框架:**

    ```markdown
    [面包屑导航: 首页 > 产品中心 > 临床诊断 > 传染病]

    <header class="page-header">
      <h1>[H1: 传染病快速诊断解决方案 / reOpenTest 传染病检测试剂]</h1>
      <p class="intro-paragraph">
        [引言: 强调快速准确诊断在控制传染病传播、指导治疗和保护公众健康中的关键作用。突出 reOpenTest 的核心优势：产品线广泛、15分钟快速、高准确性、权威认证 (P.E.I, HSC A类)、全球经验 (42国, 百万次测试)。自然融入核心关键词。]
      </p>
      <div class="key-usp-icons">
         <span><i class="icon-[广度]"></i> Test for Every Need</span>
         <span><i class="icon-[速度]"></i> 15分钟出结果</span>
         <span><i class="icon-[认证]"></i> 权威认证 (P.E.I, HSC A)</span>
         <span><i class="icon-[全球]"></i> 服务全球42国</span>
      </div>
    </header>

    <nav class="sub-category-nav card-style-nav"> <!-- Card style for better visual separation -->
      <div class="nav-card">
        <a href="#respiratory-infections">
          <i class="icon-[呼吸道]"></i>
          <h3>[呼吸道感染]</h3>
          <p>[简述: 如 COVID-19, 流感, RSV]</p>
        </a>
      </div>
      <div class="nav-card">
        <a href="#stds">
          <i class="icon-[STD]"></i>
          <h3>[性传播疾病]</h3>
          <p>[简述: 如 HIV, 梅毒等 (根据产品)]</p>
        </a>
      </div>
      <div class="nav-card" style="display: [根据是否有热带病产品决定 none 或 flex];">
        <a href="#tropical-others">
          <i class="icon-[热带病]"></i>
          <h3>[热带病/其他]</h3>
          <p>[简述: 如疟疾, 登革热等 (根据产品)]</p>
        </a>
      </div>
       <!-- Add other sub-categories if applicable -->
    </nav>

    <section id="respiratory-infections" class="product-list-section">
      <h2>[子标题: 呼吸道感染检测]</h2>
      <div class="filters-toolbar">
        [筛选控件: 按病原体 (COVID-19, Flu A/B, RSV), 样本类型 (鼻/咽拭子), 认证 (CE, P.E.I, HSC A), 检测类型 (抗原/抗体)]
        [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each respiratory product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含病原体)]</h3>
          <p class="key-features">[关键特性简述: 检测类型, 检测时间, 样本类型, 主要认证]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="stds" class="product-list-section">
      <h2>[子标题: 性传播疾病检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按病原体 (HIV, Syphilis), 样本类型 (血液, 血清/血浆), 认证, 检测类型]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each STD product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含病原体)]</h3>
          <p class="key-features">[关键特性简述: 检测类型, 检测时间, 样本类型, 主要认证]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <section id="tropical-others" class="product-list-section" style="display: [根据是否有热带病产品决定 none 或 block];">
      <h2>[子标题: 热带病/其他检测]</h2>
      <div class="filters-toolbar">
         [筛选控件: 按病原体 (Malaria, Dengue), 样本类型, 认证, 检测类型]
         [排序控件: (例如: 默认排序, 按名称)]
      </div>
      <div class="product-grid">
        <!-- Repeat for each tropical/other product -->
        <div class="product-card">
          <img src="[产品缩略图路径]" alt="[产品名称]">
          <h3>[产品名称 (包含病原体)]</h3>
          <p class="key-features">[关键特性简述: 检测类型, 检测时间, 样本类型, 主要认证]</p>
          <a href="[产品详情页链接]" class="button primary">[CTA: 查看详情 / 获取规格]</a>
        </div>
        <!-- ... more product cards -->
      </div>
    </section>

    <!-- Add other sub-category sections if applicable -->

    <section class="value-proposition-section highlight-section"> <!-- Highlight this section -->
      <h2>[标题: 全球信赖的传染病快速诊断领导者]</h2>
      <div class="value-points icon-left-text">
        <div class="point">
          <img src="[PEI Logo]" alt="P.E.I. Validation">
          <div>
            <h3>[德国 P.E.I. 权威验证]</h3>
            <p>[简述 P.E.I. 验证对产品质量和可靠性的意义]</p>
          </div>
        </div>
        <div class="point">
          <img src="[HSC Logo]" alt="EU HSC List A">
          <div>
            <h3>[欧盟 HSC A 类推荐]</h3>
            <p>[简述 HSC A 类推荐在欧盟市场的重要性和认可度]</p>
          </div>
        </div>
        <div class="point">
          <i class="icon-[全球经验]"></i>
          <div>
            <h3>[服务全球，经验丰富]</h3>
            <p>[提及服务超过 42 个国家，完成超百万次检测，以及重要合作案例 (如政府招标)]</p>
          </div>
        </div>
      </div>
      <a href="[认证/案例研究页面链接]" class="button secondary">[CTA: 查看我们的质量承诺与成功案例]</a>
    </section>

    <section class="related-resources-section">
      <h2>[标题: 深入了解传染病诊断 / 相关资源与洞察]</h2>
      <ul class="resource-links">
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "抗原 vs 抗体检测：如何选择？"]</a></li>
        <li><a href="[相关博客文章链接]">[博客文章标题: 例如 "流感与 COVID-19 联合检测的意义"]</a></li>
        <li><a href="[案例研究链接]">[案例研究标题: 例如 "reOpenTest 助力某国公共卫生筛查项目"]</a></li>
        <li><a href="[白皮书/技术文档链接]">[文档标题: 例如 "快速抗原检测技术原理与应用"]</a></li>
        <li><a href="[相关新闻稿链接]">[新闻稿标题: 关于 P.E.I 验证, HSC 推荐等]</a></li>
      </ul>
    </section>

    <section class="cta-section primary-cta-background">
      <h2>[标题: 获取 reOpenTest 传染病诊断解决方案]</h2>
      <div class="cta-buttons">
        <a href="[产品目录下载链接]" class="button primary">[CTA: 下载传染病产品目录]</a>
        <a href="[联系表单链接]" class="button secondary">[CTA: 联系销售代表]</a>
        <a href="[报价请求链接]" class="button secondary">[CTA: 获取批量采购报价]</a>
        <a href="[合作伙伴申请链接]" class="button secondary outline">[CTA: 成为分销伙伴]</a>
      </div>
      <div class="secondary-cta-links">
         <a href="[认证信息页面链接]">了解我们的质量认证</a> | <a href="[案例研究页面链接]">查看案例研究</a>
      </div>
    </section>

    [页脚 Footer]
    ```

*   **布局建议:**
    *   **整体:** 采用单栏布局，内容区块清晰。头部区域突出核心 USP。子分类导航采用卡片式，更具视觉吸引力。
    *   **头部:** 页面标题和引言下方增加 USP 图标行，强化品牌优势。
    *   **子分类导航:** 卡片式水平排列，每个卡片包含图标、标题和简述。
    *   **产品列表:** 每个子分类下使用网格布局 (Grid)，每行显示 3-4 个产品卡片。筛选/排序工具栏置于每个子分类列表上方。
    *   **价值主张强化区:** 使用左右布局（图标/Logo + 文字）或多列布局，视觉上突出权威认证和全球经验。
    *   **资源/CTA 区块:** 作为独立的横向区块。CTA 区块包含针对不同需求的多个按钮。
    *   **响应式:** 确保在小屏幕上布局合理调整，导航卡片可能变为垂直堆叠或轮播，产品卡片变为单列或双列。

    **布局示意 (ASCII Art):**

    ```
    +-----------------------------------------------------------+
    | Breadcrumbs: Home > Products > Clinical > Infectious Dis. |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h1>Page Title (Infectious Disease)</h1>             |
    |      <p>Introduction paragraph... USPs...</p>              |
    |      [Icon] USP 1 | [Icon] USP 2 | [Icon] USP 3 | [Icon] USP 4 |
    |                                                           |
    +-----------------------------------------------------------+
    | +-----------------+ +-----------------+ +-----------------+ | <- Sub-category Nav Cards
    | | Icon + Title    | | Icon + Title    | | Icon + Title    | |
    | | Description...  | | Description...  | | Description...  | |
    | +-----------------+ +-----------------+ +-----------------+ |
    +-----------------------------------------------------------+
    |                                                           |
    |      <h2>Respiratory Infections Detection</h2>            |
    | Filters: [Pathogen] [Sample] [Cert] | Sort: [Default]     |
    | +-------------+  +-------------+  +-------------+         |
    | | Product Img |  | Product Img |  | Product Img |         |
    | | Title       |  | Title       |  | Title       |         |
    | | [View Detail] |  | [View Detail] |  | [View Detail] |         |
    | +-------------+  +-------------+  +-------------+         |
    |                                                           |
    +-----------------------------------------------------------+
    |      (STD Detection Section)                              |
    +-----------------------------------------------------------+
    |      (Tropical/Other Detection Section)                   |
    +-----------------------------------------------------------+
    |        [Value Proposition Section - Highlight Certs/Global]|
    |        [Logo PEI] + Text | [Logo HSC] + Text | [Icon Global] + Text |
    |        [Button: View Quality/Cases]                       |
    +-----------------------------------------------------------+
    |             [Related Resources Section]                   |
    |             - Link Blog 1, Blog 2                         |
    |             - Link Case Study, Whitepaper, News           |
    +-----------------------------------------------------------+
    |                  [CTA Section]                            |
    |        [Download] [Contact] [Quote] [Partner]             |
    |        [Secondary Link Certs] | [Secondary Link Cases]    |
    +-----------------------------------------------------------+
    |                     [Footer]                              |
    +-----------------------------------------------------------+
    ```

*   **视觉要求:**
    *   **颜色:** 主色 `#125ea7` 用于主要 CTA、标题、导航选中项；辅助色 `#8dc2e8` 可用于次要按钮背景或区块背景；强调色 `#FF9800` 谨慎用于突出关键信息；中性色 `#424242` 用于正文。
    *   **字体:** 标题 `Sora, sans-serif` (Bold)；正文 `Roboto, sans-serif`。
    *   **间距:** `rem` 单位，区块间距 `2rem` 或 `3rem`，列表内间距 `1rem`。
    *   **UI 元素:** 按钮、卡片使用圆角矩形。子分类导航卡片样式统一。图标使用线性图标。权威认证 Logo 清晰展示。
    *   **图片:** 产品图片清晰、专业、背景统一。

*   **SEO 建议:**
    *   **URL:** `/products/clinical-diagnostics/infectious-disease`
    *   **Title:** `传染病快速诊断试剂 | COVID-19, 流感, STD 检测 | reOpenTest`
    *   **Meta Description:** `reOpenTest 提供广泛、快速、可靠的传染病快速诊断解决方案，涵盖呼吸道感染、STD 等。15分钟出结果，获 P.E.I./HSC 认证。`
    *   **Keywords:** 传染病快速检测, 快速抗原检测, 快速抗体检测, COVID-19 检测, 流感检测, STD 检测, IVD 传染病, P.E.I. 认证, HSC A 类, reOpenTest (根据详细研究调整)

*   **与其他页面的链接关系:**
    *   **链接到此页:** 从产品中心主页、临床诊断概述页、相关疾病科普页、解决方案页（公共卫生、医院感染控制）、相关博客文章、新闻稿。
    *   **从此页链接出:** 必须链接到所有列出的传染病产品详情页、产品目录下载链接、联系/报价/合作页面、相关资源链接页面（博客、案例、认证、新闻等）。

*   **备注:**
    *   产品列表和子分类需要根据实际产品线动态生成。
    *   页面内容和价值主张应重点突出产品广度、速度和权威认证。
    *   确保子分类导航链接 (`#respiratory-infections`, `#stds` 等) 能正确跳转。
    *   CTA 需包含面向分销商的入口。
