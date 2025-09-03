---
* 功能： 网站 SEO Schema (JSON-LD) 数据
* 描述：  包含网站基本信息和各页面的 SEO Schema (JSON-LD) 数据，用于搜索引擎优化
* 更新时间： 2025-03-26
---

```javascript
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "reOpenTest",
  "url": "https://www.reopentest.com",
  "logo": "https://www.reopentest.com/logo.png",
  "description": "reOpenTest 提供全系列IVD快速诊断试剂产品，15年研发生产经验，ISO13485和CE认证，服务全球客户。Test for Every Need.",
  "keywords": ["reOpenTest", "rapid test", "IVD", "快速诊断", "体外诊断", "即时检测"],
  "contactPoint": {
    "@type": "ContactPoint",
    "telephone": "+86-XXX-XXXX-XXXX",
    "contactType": "customer service",
    "areaServed": "Global",
    "availableLanguage": ["Chinese", "English"]
  },
  "sameAs": [
    "https://www.linkedin.com/company/reopentest",
    "https://www.facebook.com/reopentest",
    "https://twitter.com/reopentest"
  ],
  "potentialAction": {
    "@type": "SearchAction",
    "target": {
      "@type": "EntryPoint",
      "urlTemplate": "https://www.reopentest.com/search?q={search_term_string}"
    },
    "query-input": "required name=search_term_string"
  }
}
```

---

## 首页 (Home)

```javascript
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "url": "https://www.reopentest.com/",
  "name": "reOpenTest - Test for Every Need.",
  "description": "reOpenTest 提供全系列IVD快速诊断试剂产品，15年研发生产经验，ISO13485和CE认证，服务全球客户。Test for Every Need.",
  "keywords": ["reOpenTest", "rapid test", "IVD", "快速诊断", "体外诊断", "即时检测"]
}
```

---

## 产品总览页 (Product Overview)

```javascript
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "url": "https://www.reopentest.com/products",
  "name": "产品与服务 - reOpenTest",
  "description": "reOpenTest 提供 DoA、传染病、Fertility、STDs 等各类快速诊断产品。",
  "keywords": ["reOpenTest", "rapid test", "IVD", "快速诊断", "产品", "DoA", "传染病", "Fertility", "STDs"]
}
```

---

## DoA 产品分类页 (Product Category)

```javascript
{
  "@context": "https://schema.org",
  "@type": "CollectionPage",
  "url": "https://www.reopentest.com/products/doa",
  "name": "DoA 药物滥用检测产品 - reOpenTest",
  "description": "了解 reOpenTest 的 DoA 药物滥用检测产品，提供尿液、唾液、毛发等多种快速检测方案。",
  "keywords": ["reOpenTest", "DoA", "药物滥用检测", "尿液检测", "唾液检测", "毛发检测", "快速诊断"]
}
```

---

## COVID-19 抗原快速检测试剂盒 产品详情页 (Product Detail Page)

```javascript
{
  "@context": "https://schema.org",
  "@type": "Product",
  "url": "https://www.reopentest.com/products/infectious-diseases/covid-19-antigen-cassette",
  "name": "reOpenTest COVID-19 抗原快速检测试剂盒",
  "image": "https://www.reopentest.com/images/products/covid-19-antigen-cassette.jpg",
  "description": "reOpenTest COVID-19 抗原快速检测试剂盒，15分钟快速检测，准确可靠，适用于早期筛查。",
  "keywords": ["reOpenTest", "COVID-19", "新冠抗原检测", "快速检测试剂盒", "传染病检测", "rapid test", "IVD"],
  "brand": {
    "@type": "Brand",
    "name": "reOpenTest"
  },
  "category": "体外诊断试剂",
  "productCategory": "IVD Rapid Test",
  "offers": {
    "@type": "Offer",
    "url": "https://www.reopentest.com/products/infectious-diseases/covid-19-antigen-cassette",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  }
}
```

---

## 药物滥用 (DoA) 快速检测试剂盒 (尿液) 产品详情页 (Product Detail Page)

```javascript
{
  "@context": "https://schema.org",
  "@type": "Product",
  "url": "https://www.reopentest.com/products/doa/urine-doa-test-cassette",
  "name": "reOpenTest 药物滥用 (DoA) 快速检测试剂盒 (尿液)",
  "image": "https://www.reopentest.com/images/products/doa-urine-test-cassette.jpg",
  "description": "reOpenTest 药物滥用 (DoA) 快速检测试剂盒 (尿液)，快速、准确、灵敏，适用于各类药物滥用筛查场景。",
  "keywords": ["reOpenTest", "药物滥用检测", "DoA", "尿液检测", "快速检测试剂盒", "毒品检测", "drug of abuse", "rapid test", "IVD"],
  "brand": {
    "@type": "Brand",
    "name": "reOpenTest"
  },
  "category": "体外诊断试剂",
  "productCategory": "IVD Rapid Test",
  "offers": {
    "@type": "Offer",
    "url": "https://www.reopentest.com/products/doa/urine-doa-test-cassette",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  }
}
```

---

## 早孕检测试剂盒 (胶体金法) 产品详情页 (Product Detail Page)

```javascript
{
  "@context": "https://schema.org",
  "@type": "Product",
  "url": "https://www.reopentest.com/products/fertility/pregnancy-test-cassette",
  "name": "reOpenTest 早孕检测试剂盒 (胶体金法)",
  "image": "https://www.reopentest.com/images/products/pregnancy-test-cassette.jpg",
  "description": "reOpenTest 早孕检测试剂盒 (胶体金法)，高灵敏度，快速准确，居家自测，方便快捷。",
  "keywords": ["reOpenTest", "早孕检测", "验孕棒", "早孕试纸", "pregnancy test", "fertility test", "IVD", "快速诊断"],
  "brand": {
    "@type": "Brand",
    "name": "reOpenTest"
  },
  "category": "体外诊断试剂",
  "productCategory": "IVD Rapid Test",
  "offers": {
    "@type": "Offer",
    "url": "https://www.reopentest.com/products/fertility/pregnancy-test-cassette",
    "priceCurrency": "USD",
    "availability": "https://schema.org/InStock"
  }
}
```

---

## 关于我们 (About Us) 页面

```javascript
{
  "@context": "https://schema.org",
  "@type": "AboutPage",
  "url": "https://www.reopentest.com/about-us",
  "name": "关于我们 - reOpenTest",
  "description": "了解 reOpenTest 的品牌故事、公司简介、核心价值观和资质认证。我们致力于通过创新的快速诊断技术守护全球健康。",
  "keywords": ["reOpenTest", "关于我们", "公司简介", "品牌故事", "价值观", "资质认证", "IVD"]
}
```

---

## 医院感染控制解决方案页面 (Solution Detail Page)

```javascript
{
  "@context": "https://schema.org",
  "@type": "Article",
  "url": "https://www.reopentest.com/solutions/hospital-infection-control",
  "name": "医院感染控制解决方案 - reOpenTest",
  "description": "了解 reOpenTest 如何帮助您应对医院感染控制的挑战，提供快速、准确、可靠的诊断解决方案，有效预防和控制院内感染。",
  "keywords": ["reOpenTest", "医院感染控制", "院内感染", "HAI", "快速诊断", "解决方案", "传染病检测"]
}
