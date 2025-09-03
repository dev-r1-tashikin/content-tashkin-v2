# 页面内容框架与布局建议: 呼吸道传染病专题

**页面类型:** Topic Page (专题页面)
**Schema.org `@type`:** `WebPage` 或 `CollectionPage` (如果页面结构侧重于列出不同疾病或产品)
**页面目标:** 提供全面、权威的呼吸道传染病及其快速检测方案信息，建立品牌专业形象，吸引相关搜索流量，并引导用户了解具体产品/解决方案。
**建议文件名/URL Slug:** `topic_respiratory_infectious_diseases`

---

## 内容框架 (Content Outline)

```markdown
[Header: Logo, Main Navigation (Products, Solutions, Support, About, Contact)]

<!-- Section 1: Hero Banner -->
<section class="hero bg-primary-color text-white">
  <h1>[引人入胜的标题: 例如：“应对呼吸道挑战：reOpenTest 全面的快速检测解决方案”]</h1>
  <p>[引言段落: 强调呼吸道疾病的普遍性、危害以及快速诊断的重要性，简述 reOpenTest 的承诺与能力]</p>
  [CTA Button: "浏览检测方案" -> #solutions]
</section>

<!-- Section 2: Common Respiratory Diseases Overview -->
<section class="disease-overview py-3">
  <h2>常见呼吸道传染病概览</h2>
  <!-- Option 1: Tabs -->
  <div class="tabs">
    <button class="tab-link active" data-tab="flu">流感 (Influenza)</button>
    <button class="tab-link" data-tab="covid">新冠 (COVID-19)</button>
    <button class="tab-link" data-tab="rsv">RSV</button>
    <button class="tab-link" data-tab="other">其他</button>
  </div>
  <div id="flu" class="tab-content active">
    <h3>流感 (Influenza)</h3>
    <p>[症状、传播途径、检测必要性简述]</p>
    <p>了解 reOpenTest [流感检测产品名称] -> [Link to Product Detail Page]</p>
  </div>
  <div id="covid" class="tab-content">
    <h3>新冠 (COVID-19)</h3>
    <p>[症状、变种、持续检测需求简述]</p>
    <p>了解 reOpenTest [新冠检测产品名称] -> [Link to Product Detail Page]</p>
  </div>
  <div id="rsv" class="tab-content">
    <h3>呼吸道合胞病毒 (RSV)</h3>
    <p>[对特定人群危害、检测意义简述]</p>
    <p>了解 reOpenTest [RSV 检测产品名称] -> [Link to Product Detail Page]</p>
  </div>
  <div id="other" class="tab-content">
    <h3>其他常见呼吸道病原体</h3>
    <p>[如腺病毒等简要介绍]</p>
    <p>了解 reOpenTest [相关检测产品名称] -> [Link to Product Detail Page]</p>
  </div>
  <!-- Option 2: Accordion or Grid Layout could also be used -->
</section>

<!-- Section 3: Why Choose Rapid Testing? -->
<section class="why-rapid-testing bg-light py-3">
  <h2>为什么选择快速检测？</h2>
  <div class="grid-container columns-4">
    <div class="grid-item">
      [Icon: Clock]
      <h4>及时诊断与治疗</h4>
      <p>[简要说明]</p>
    </div>
    <div class="grid-item">
      [Icon: Shield]
      <h4>快速分诊与隔离</h4>
      <p>[简要说明控制传播]</p>
    </div>
    <div class="grid-item">
      [Icon: Pill with cross]
      <h4>减少抗生素滥用</h4>
      <p>[简要说明]</p>
    </div>
    <div class="grid-item">
      [Icon: Chart Increase]
      <h4>提高医疗效率</h4>
      <p>[简要说明资源利用]</p>
    </div>
  </div>
</section>

<!-- Section 4: reOpenTest Solutions -->
<section id="solutions" class="reopentest-solutions py-3">
  <h2>reOpenTest 呼吸道检测解决方案</h2>
  <p>[引导性文字，强调全面性、快速、可靠]</p>
  
  <h3>我们的产品线</h3>
  [图表或清晰列表: 按病原体 (新冠、流感、RSV、联检) 或按检测类型展示产品系列]
  [Link to Full Product Catalog/Respiratory Section]

  <h3>核心优势</h3>
  <div class="grid-container columns-4">
      <div class="grid-item">
          [Icon: Rocket]
          <h4>快速结果</h4>
          <p>多数产品 15 分钟内提供结果</p>
      </div>
      <div class="grid-item">
          [Icon: Target]
          <h4>高准确性</h4>
          <p>经临床验证，性能可靠 (灵敏度/特异性 [可引述范围])</p>
      </div>
      <div class="grid-item">
          [Icon: Easy]
          <h4>操作简便</h4>
          <p>适用于多种场景，部分产品无需专业设备</p>
      </div>
      <div class="grid-item">
          [Icon: Badge/Certificate]
          <h4>权威认证</h4>
          <p>符合 CE, ISO 标准，获 PEI, HSC 等认可</p>
      </div>
  </div>

  <h3>重点产品推荐</h3>
  <div class="product-highlights grid-container columns-3">
      <div class="product-card">
          [Product Image: COVID Antigen Test]
          <h4>新冠抗原快速检测</h4>
          <p>[简要描述和优势]</p>
          [Link: "了解详情" -> Product Detail Page]
      </div>
      <div class="product-card">
          [Product Image: Flu A/B Test]
          <h4>流感 A/B 快速检测</h4>
          <p>[简要描述和优势]</p>
          [Link: "了解详情" -> Product Detail Page]
      </div>
      <div class="product-card">
          [Product Image: Combo Test]
          <h4>新冠/流感/RSV 联检</h4>
          <p>[简要描述和优势]</p>
          [Link: "了解详情" -> Product Detail Page]
      </div>
  </div>
</section>

<!-- Section 5: Application Scenarios -->
<section class="scenarios bg-light py-3">
    <h2>应用场景</h2>
    <div class="grid-container columns-3">
        <div class="scenario-item">
            [Icon: Hospital]
            <h4>医疗机构</h4>
            <p>(急诊、门诊、住院部)</p>
        </div>
        <div class="scenario-item">
            [Icon: Building/Community]
            <h4>公共卫生筛查</h4>
            <p>(社区、交通枢纽)</p>
        </div>
        <div class="scenario-item">
            [Icon: Briefcase/Factory]
            <h4>企业与学校</h4>
            <p>(工作场所、校园)</p>
        </div>
        <!-- Add Home Use if applicable -->
    </div>
</section>

<!-- Section 6: Choosing the Right Test -->
<section class="choose-test py-3">
    <h2>如何选择合适的检测方案？</h2>
    <p>[根据不同场景 (临床诊断 vs. 筛查)、目标人群、所需检测的病原体种类等提供选择指导。]</p>
    [Link: "获取定制化解决方案" -> Contact Page or Solutions Page]
</section>

<!-- Section 7: Quality & Support -->
<section class="quality-support bg-neutral-light py-3">
    <div class="container grid-container columns-2">
        <div>
            <h3>质量保证</h3>
            <p>我们严格遵循 ISO13485 质量管理体系，所有产品均符合 CE 标准... [提及 PEI, HSC 等认证]</p>
            [Link: "了解我们的质量体系" -> About Us/Quality Page]
        </div>
        <div>
            <h3>客户支持</h3>
            <p>我们提供全面的技术支持和客户服务，确保您顺利使用我们的产品。</p>
            [Link: "访问支持中心" -> Support Page]
        </div>
    </div>
</section>

<!-- Section 8: Final CTA -->
<section class="final-cta text-center py-4 bg-primary-color text-white">
    <h2>准备好提升您的呼吸道疾病检测能力了吗？</h2>
    <p>探索我们的全系列产品，或联系我们的专家获取定制化解决方案。</p>
    [CTA Button: "浏览所有产品" -> Product Catalog]
    [CTA Button (Secondary): "联系销售专家" -> Contact Page]
</section>

[Footer: Copyright, Privacy Policy, Terms, Sitemap, Social Links]
```

---

## 布局建议 (Layout Recommendation)

*   **整体:** 采用现代、简洁、专业的单栏或主内容区+侧边栏（用于导航或相关链接）布局。注重留白，确保信息层级清晰。
*   **移动端:** 必须采用响应式设计，确保在手机和平板上阅读和导航流畅。卡片式布局、折叠菜单、可滑动内容等适用于小屏幕。

**布局示意 (Markdown Sketch):**

```
+------------------------------------------------------+
| Header: Logo | Navigation (Products, Solutions...)   |
+------------------------------------------------------+
| Section 1: Hero Banner (Full Width)                  |
| H1 Title                                             |
| Intro Text                                           |
| [CTA Button]                                         |
+------------------------------------------------------+
| Section 2: Disease Overview (Centered Content Width) |
| H2 Title                                             |
| [Tabs: Flu | COVID | RSV | Other]                   |
| [Tab Content Area]                                   |
+------------------------------------------------------+
| Section 3: Why Rapid Testing (Full Width, BG Color)  |
| H2 Title                                             |
| [Icon Grid: 4 Columns]                               |
| [Icon][Icon][Icon][Icon]                             |
| [Text][Text][Text][Text]                             |
+------------------------------------------------------+
| Section 4: reOpenTest Solutions (Centered)           |
| H2 Title                                             |
| H3 Product Line -> [Chart/List]                      |
| H3 Core Advantages -> [Icon Grid: 4 Columns]         |
| H3 Product Highlights -> [Card Grid: 3 Columns]      |
| [Card][Card][Card]                                   |
+------------------------------------------------------+
| Section 5: Scenarios (Full Width, BG Color)          |
| H2 Title                                             |
| [Icon Grid: 3 Columns]                               |
| [Icon][Icon][Icon]                                   |
| [Text][Text][Text]                                   |
+------------------------------------------------------+
| Section 6: Choosing Test (Centered)                  |
| H2 Title                                             |
| [Text Content]                                       |
| [CTA Link]                                           |
+------------------------------------------------------+
| Section 7: Quality & Support (Full Width, BG Color)  |
| [2 Column Grid: Quality | Support]                   |
| [Text][Link] | [Text][Link]                         |
+------------------------------------------------------+
| Section 8: Final CTA (Full Width, BG Color, Centered)|
| H2 Title                                             |
| [Text Content]                                       |
| [CTA Button] [Secondary CTA Button]                  |
+------------------------------------------------------+
| Footer: Links | Copyright                            |
+------------------------------------------------------+
```

---

## 视觉要求 (Visual Style)

*   **颜色:**
    *   主色: `#125ea7` (用于 Hero Banner 背景, 主要 CTA 按钮, 标题强调等)
    *   辅助色: `#8dc2e8` (用于次要元素, 图标背景, 或与主色搭配)
    *   强调色: `#FF9800` (用于次要 CTA 或需要特别突出的元素，谨慎使用)
    *   中性色: `#424242` (用于正文文本), `#f5f5f5` 或类似浅灰 (用于部分区块背景 `bg-light`, `bg-neutral-light`)
*   **字体:**
    *   标题 (H1-H3): `Sora, sans-serif` (可使用较粗字重如 600 或 700)
    *   正文: `Roboto, sans-serif` (字重 400)
*   **间距:** 遵循 `info_visual.md` 建议，使用 `rem` 单位，保持足够的留白 (e.g., `padding: 3rem 0;` for sections)。
*   **UI 元素:** 按钮使用圆角矩形，样式简洁。图标使用现代线性图标。卡片设计简洁，可带轻微阴影或边框。
*   **图片风格:** 高质量、专业、清晰。产品图需干净背景或展示使用场景。场景图需体现专业性（医疗环境、实验室等）。

---

## SEO 建议

*   **URL:** `/topics/respiratory-infectious-diseases`
*   **页面标题 (Title Tag):** 呼吸道传染病快速检测解决方案 | reOpenTest
*   **Meta Description:** 一站式了解流感、新冠、RSV等呼吸道传染病及其快速检测方案。reOpenTest提供全面、可靠的IVD快速诊断试剂。
*   **H1 标签:** 应包含核心关键词，如 "呼吸道传染病检测解决方案"。
*   **关键词密度:** 自然融入主要和次要关键词于标题、段落文本、图片 ALT 文本中。

---

## 与其他页面的链接关系

*   **内部链接入:** 首页、解决方案页、产品总览页、相关博客文章、新闻稿。
*   **内部链接出:** 具体呼吸道产品详情页、联系我们页、支持中心、关于我们（质量部分）、相关博客文章。
*   **外部链接:** （可选）WHO, CDC 等权威机构的相关疾病信息页面。

---

## 备注

*   内容需根据最新的产品信息和市场情况进行更新。
*   确保所有性能数据和认证信息准确无误。
*   移动端体验优先考虑。
