# 页面链接分析与层级结构 (6.detail/pages)

本文档分析了 `6.detail/pages` 目录下所有 Markdown 页面的内部链接有效性，并梳理了推断出的页面层级结构。

## 链接检查结果

### 1. URL 定义不一致

*   **问题:** `page_theme_toxicology_drug_monitoring.md` 文件定义的 URL 是 `/products/doa-testing`，但 `product_overview.md` 和 `page_home.md` 中链接到的是 `/products/toxicology-drug-monitoring`。
*   **建议:** 统一 URL。建议将 `page_theme_toxicology_drug_monitoring.md` 中的 `page.url` 修改为 `/products/toxicology-drug-monitoring` 以保持一致性，或者修改 `product_overview.md` 和 `page_home.md` 中的链接为 `/products/doa-testing`。

### 2. 内部链接有效性 (基于 `6.detail/pages` 目录)

以下是在 `6.detail/pages` 目录中找到的页面及其定义的 URL：

*   `/` (page_home.md)
*   `/products` (product_overview.md)
*   `/products/cardiology` (page_theme_cardiology.md)
*   `/products/endocrinology-metabolism` (page_theme_endocrinology_metabolism.md)
*   `/products/gastrointestinal-health` (page_theme_gastrointestinal_health.md)
*   `/products/hematology-coagulation` (page_theme_hematology_coagulation.md)
*   `/products/immunology-inflammation` (page_theme_immunology_inflammation.md)
*   `/products/infectious-disease` (page_theme_infectious_disease.md)
*   `/products/nephrology` (page_theme_nephrology.md)
*   `/products/oncology` (page_theme_oncology.md)
*   `/solutions/hospital-infection-control` (page_theme_solution_hospital_infection_control.md) - *注意: URL 结构不同*
*   `/products/doa-testing` (page_theme_toxicology_drug_monitoring.md) - *注意: URL 不一致问题*
*   `/products/urinalysis` (page_theme_urinalysis.md)
*   `/products/womens-health-reproduction` (page_theme_womens_health_reproduction.md)
*   `/about-us` (page_about_us.md)
*   `/blog` (page_blog_overview.md)
*   `/contact-us` (page_contact_us.md)
*   `/products/infectious-diseases/covid-19-antigen-cassette` (page_product_detail_covid19_antigen.md)

**结论:**
*   主要导航页面（Home, Product Overview, About Us, Contact Us, Blog Overview）之间的链接基本有效。
*   从 Product Overview 到各个产品主题页面的链接基本有效（除了 Toxicology/DOA 的不一致问题）。
*   从 Home 到重点产品主题页面的链接有效（除了 Toxicology/DOA 的不一致问题）。
*   从各个主题页面返回 Home 和 Product Overview 的链接（通过面包屑）有效。
*   `page_theme_solution_hospital_infection_control.md` 使用了 `/solutions/` 路径，与其他产品主题页面的 `/products/` 不同，需确认是否符合预期。

### 3. 缺失的产品详情页

大量产品主题页面链接到了具体的产品详情页，但这些页面文件在 `6.detail/pages` 目录中缺失。例如：
*   `/products/cardiology/cardiac-markers-combo-test`
*   `/products/cardiology/cardiac-troponin-i-test`
*   `/products/endocrinology/hba1c-rapid-test`
*   `/products/gastrointestinal/hpylori-antigen-fecal`
*   `/products/d-dimer-rapid-test`
*   `/products/inflammation/crp-semi-quantitative-test`
*   `/products/infectious-disease/adenovirus-antigen-test` (除了 COVID-19 页面)
*   `/products/nephrology/microalbumin-rapid-test`
*   `/products/oncology/cea-test`
*   `/products/doa/urine-cup-12-panel-ad`
*   `/products/urinalysis/strips-11-param-vc`
*   `/products/womens-health-reproduction/amh-test`
*   ...等等

**建议:** 需要创建这些缺失的产品详情页 Markdown 文件，或者确认它们是否存在于其他目录。

### 4. 外部/未定义页面链接

存在大量指向 `/resources`, `/blog`, `/news`, `/faq`, `/partners`, `/support`, `/technology`, `/disease-info`, `/where-to-buy`, `/request-quote`, `/downloads`, `/quality-and-cases`, `/quality-and-certifications` 等路径的链接。

**建议:** 这些页面文件不在 `6.detail/pages` 目录下。需要确认这些页面是否存在于网站的其他部分，或者是否需要创建。

## 推断的页面层级结构 (基于 `6.detail/pages`)

```
/ (Home)
├── /products (Product Overview)
│   ├── /products/cardiology (Theme: Cardiology)
│   │   └── /products/cardiology/{product-detail}* (Product Detail - 缺失)
│   ├── /products/infectious-disease (Theme: Infectious Disease)
│   │   ├── /products/infectious-diseases/covid-19-antigen-cassette (Product Detail - 存在)
│   │   └── /products/infectious-disease/{product-detail}* (Product Detail - 缺失)
│   ├── /products/oncology (Theme: Oncology)
│   │   └── /products/oncology/{product-detail}* (Product Detail - 缺失)
│   ├── /products/nephrology (Theme: Nephrology)
│   │   └── /products/nephrology/{product-detail}* (Product Detail - 缺失)
│   ├── /products/endocrinology-metabolism (Theme: Endocrinology & Metabolism)
│   │   └── /products/endocrinology/{product-detail}* (Product Detail - 缺失)
│   ├── /products/gastrointestinal-health (Theme: Gastrointestinal Health)
│   │   └── /products/gastrointestinal/{product-detail}* (Product Detail - 缺失)
│   ├── /products/hematology-coagulation (Theme: Hematology & Coagulation)
│   │   └── /products/d-dimer-rapid-test* (Product Detail - 缺失)
│   ├── /products/immunology-inflammation (Theme: Immunology & Inflammation)
│   │   └── /products/inflammation/{product-detail}* (Product Detail - 缺失)
│   ├── /products/toxicology-drug-monitoring (or /products/doa-testing) (Theme: Toxicology/DOA) - **URL 不一致**
│   │   ├── /products/toxicology/{product-detail}* (Product Detail - 缺失)
│   │   └── /products/doa/{product-detail}* (Product Detail - 缺失)
│   ├── /products/urinalysis (Theme: Urinalysis)
│   │   └── /products/urinalysis/{product-detail}* (Product Detail - 缺失)
│   └── /products/womens-health-reproduction (Theme: Women's Health & Reproduction)
│       ├── /products/womens-health-reproduction/{product-detail}* (Product Detail - 缺失)
│       ├── /products/pregnancy/{product-detail}* (Product Detail - 缺失)
│       └── /products/std/{product-detail}* (Product Detail - 缺失)
├── /solutions/hospital-infection-control (Solution: Hospital Infection Control) - *注意: 路径不同*
├── /about-us (About Us)
├── /blog (Blog Overview)
│   └── /blog/{article-slug}* (Blog Post - 外部/缺失)
│   └── /news/{news-slug}* (News Post - 外部/缺失)
├── /contact-us (Contact Us)
└── 其他外部/未定义页面:
    ├── /resources/...*
    ├── /faq/...*
    ├── /partners/...*
    ├── /support/...*
    ├── /technology/...*
    ├── /disease-info/...*
    ├── /where-to-buy*
    ├── /request-quote*
    ├── /downloads/...*
    ├── /quality-and-cases*
    └── /quality-and-certifications*

*注: `*` 表示该页面或其下的子页面在 `6.detail/pages` 目录中缺失或被认为是外部链接。*
