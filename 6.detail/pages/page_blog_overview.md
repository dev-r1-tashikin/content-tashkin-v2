{
    "page_slug": "blog",
    "page_url": "/blog",
  "page_type": "blog_overview",
  "page": {
    "url": "/blog", // Or /news, keeping /blog consistent with reference
    "title": "reOpenTest 博客与新闻 | IVD 洞察与行业动态", // Updated title reflecting brand and focus
    "meta": {
      "description": "探索 reOpenTest 的最新博客文章和公司新闻，获取关于体外诊断 (IVD)、快速检测技术、行业趋势和 reOpenTest 解决方案的专业见解。", // Updated description based on strategy
      "keywords": [ // Updated keywords based on strategy
        "reOpenTest 博客",
        "IVD 新闻",
        "体外诊断",
        "快速诊断试剂",
        "POCT",
        "医疗诊断资讯",
        "行业洞察",
        "公司新闻"
      ]
    },
    "content": {
      "sections": [
        {
          "type": "page_header",
          "id": "blog-header",
          "headline": "博客与新闻", // Kept simple
          "subheadline": "获取 reOpenTest 在体外诊断领域的最新动态、专业知识和创新进展。" // Updated subheadline
        },
        {
          "type": "article_list_section",
          "id": "article-list",
          "filters": [ // Adjusted filters based on strategy content pillars/product lines
             {
              "label": "分类",
              "type": "dropdown",
              "options": [
                { "value": "all", "label": "所有分类"},
                { "value": "ivd-technology", "label": "IVD 技术解读"}, // Reflects strategy
                { "value": "product-application", "label": "产品应用"}, // Reflects strategy
                { "value": "industry-insights", "label": "行业洞察"}, // Reflects strategy
                { "value": "case-studies", "label": "案例研究"}, // Reflects strategy
            { "value": "company-news", "label": "公司新闻"} // Kept from reference
              ]
            }
          ],
          "sort_options": [
            { "value": "newest", "label": "最新发布" },
            { "value": "oldest", "label": "最早发布" }
          ],
          "articles": [ // Kept example articles, categories adjusted slightly
            {
              "title": "呼吸道联检：经销商抓住季节性增长机遇 | reOpenTest",
              "excerpt": "了解呼吸道联合检测市场潜力与 reOpenTest 优势。为经销商提供抓住季节性机遇、提升诊断销售额的策略。立即咨询合作！",
              "image": {
                "src": "/assets/images/blog-thumb-respiratory-combo-growth.jpg",
                "alt": "呼吸道联合检测经销商增长机遇",
                "prompt": "Thumbnail image for a blog post about respiratory combo test distributor growth opportunities. Could show a graph indicating seasonal demand, a distributor looking at combo test products, or a healthcare setting using the tests during flu season. Convey opportunity and timeliness."
              },
              "link": "/blog/respiratory-combo-test-distributor-growth-opportunity",
              "publish_date": "2025-04-13",
              "author_name": "reOpenTest 市场团队",
              "category": "行业洞察" // Or "经销商机遇"
            },
            {
              "title": "如何选择可靠诊断供应商？5大关键因素(药物检测杯)| reOpenTest",
              "excerpt": "寻找可靠诊断供应商？本指南以药物检测杯为例，解析评估 IVD 制造商的5大关键因素：质量、供应链、定制、支持和条款。",
              "image": {
                "src": "/assets/images/blog-thumb-supplier-selection.jpg",
                "alt": "如何选择可靠诊断供应商？5大关键因素",
                "prompt": "Thumbnail image for a blog post about choosing a reliable diagnostic supplier, using drug test cups as an example. Could show a checklist, a magnifying glass over supplier options, or a graphic representing the 5 key factors. Convey thorough evaluation and trust."
              },
              "link": "/blog/how-to-choose-reliable-diagnostic-supplier-drug-test-cup-example",
              "publish_date": "2025-04-13",
              "author_name": "reOpenTest 供应链团队",
              "category": "行业洞察" // Or "供应商选择" if that category exists
            },
            {
              "title": "不仅仅是达标：为何快速诊断试剂的准确性与可靠性是经销商成功的关键？",
              "excerpt": "在竞争日益激烈的体外诊断 (IVD) 市场，仅仅满足基本的合规标准已远不足以确保持续成功。对于 B2B 经销商而言，您所代理和销售的快速诊断试剂的准确性与可靠性...",
              "image": {
                "src": "/assets/images/blog-thumb-accuracy-reliability.jpg",
                "alt": "诊断试剂准确性与可靠性对经销商成功的重要性",
                "prompt": "Thumbnail image for a blog post about diagnostic test accuracy and reliability for distributor success. Could show a graph indicating high accuracy, quality control symbols, or a successful business handshake. Convey precision and trust."
              },
              "link": "/blog/diagnostic-test-accuracy-reliability-distributor-success",
              "publish_date": "2025-04-13",
              "author_name": "reOpenTest 质量控制团队",
              "category": "行业洞察" // Or "质量保证" if that category exists
            },
           
            
            
            // ... Add more articles/news items placeholders
          ],
          "pagination": {
            "current_page": 1,
            "total_pages": 1, // Adjust if more articles
            "items_per_page": 9
          }
        },
        
        },
        { // Optional subscribe CTA based on reference file structure
          "type": "subscribe_cta",
          "id": "blog-subscribe",
          "headline": "订阅获取最新 IVD 资讯",
          "body": "将最新的体外诊断行业洞察和 reOpenTest 新闻直接发送到您的邮箱。",
          "form": {
             "fields": [
               { "name": "email", "type": "email", "placeholder": "请输入您的邮箱地址", "required": true }
             ],
             "submit_button": { "text": "立即订阅" }
          }
        }
      ]
    },
    "assets": { // Updated asset placeholders
      "images": [
        {"url": "/assets/images/blog-thumb-rapid-test-importance.jpg", "alt": "医护人员使用 reOpenTest 快速诊断试剂", "prompt": "Thumbnail image for a blog post about the importance of rapid tests in infectious disease screening. Could show a healthcare worker using a reOpenTest kit, a visual representation of rapid results, or a public health scenario. Convey speed and reliability."},
        {"url": "/assets/images/blog-thumb-poct-efficiency.jpg", "alt": "社区诊所医生使用 POCT 设备", "prompt": "Thumbnail image for a blog post about POCT efficiency in primary care. Could show a doctor using a portable testing device in a clinic setting, a patient receiving faster results, or a graphic illustrating improved workflow. Convey accessibility and efficiency."},
        {"url": "/assets/images/blog-thumb-partnership.jpg", "alt": "reOpenTest 与合作伙伴握手的象征性图片", "prompt": "Thumbnail image representing a strategic partnership. Could show logos of both companies, a handshake graphic, or a team meeting photo. Convey collaboration and shared goals."}
        // Add other article thumbnail URLs
      ],
      "icons": [] // Kept empty as per reference
    },
    "styles": { // Kept CSS from reference, assuming it aligns with visual guide's principles
      "css": "/* 博客概览页特定 CSS */\n.article_list_section { /* Layout for filters + list */ } \n.article_list_section .filters { margin-bottom: 1.5rem; } \n.article_list_section .article_grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 2rem; } \n.article_grid .article_card { border: 1px solid var(--border-color, #e0e0e0); border-radius: var(--card-radius, 8px); overflow: hidden; display: flex; flex-direction: column; background-color: var(--card-bg-color, #ffffff); transition: box-shadow 0.3s ease; } \n.article_grid .article_card:hover { box-shadow: 0 4px 12px rgba(0,0,0,0.1); } \n.article_grid .article_card img { display: block; width: 100%; height: 200px; object-fit: cover; } \n.article_grid .article_card .content { padding: 1.5rem; flex-grow: 1; display: flex; flex-direction: column; } \n.article_grid .article_card h3 { margin-top: 0; font-size: 1.25rem; font-family: 'Sora', sans-serif; color: var(--heading-color, #333); margin-bottom: 0.75rem; } \n.article_grid .article_card .metadata { font-size: 0.875rem; color: var(--text-muted-color, #757575); margin-bottom: 0.5rem; font-family: 'Roboto', sans-serif; } \n.article_grid .article_card .excerpt { margin-bottom: 1rem; color: var(--text-color, #424242); font-family: 'Roboto', sans-serif; line-height: 1.6; flex-grow: 1; } \n.article_grid .article_card .read_more { font-weight: 600; color: var(--primary-color, #125ea7); text-decoration: none; font-family: 'Roboto', sans-serif; margin-top: auto; align-self: flex-start; } \n.article_grid .article_card .read_more:hover { text-decoration: underline; } \n.pagination { margin-top: 2rem; text-align: center; } \n.subscribe_cta { background-color: var(--light-bg-color, #f8f9fa); padding: 3rem 1rem; text-align: center; margin-top: 3rem;} \n.subscribe_cta h2 { font-family: 'Sora', sans-serif; margin-bottom: 1rem; } \n.subscribe_cta p { margin-bottom: 1.5rem; max-width: 600px; margin-left: auto; margin-right: auto; } \n.subscribe_cta form { display: flex; justify-content: center; gap: 0.5rem; max-width: 400px; margin: 0 auto; } \n.subscribe_cta input[type='email'] { flex-grow: 1; padding: 0.75rem 1rem; border: 1px solid var(--border-color, #ced4da); border-radius: var(--input-radius, 4px); } \n.subscribe_cta button { background-color: var(--primary-color, #125ea7); color: white; border: none; padding: 0.75rem 1.5rem; border-radius: var(--button-radius, 4px); cursor: pointer; transition: background-color 0.3s ease; } \n.subscribe_cta button:hover { background-color: var(--primary-dark-color, #0e4a81); }"
    }
  }
}
