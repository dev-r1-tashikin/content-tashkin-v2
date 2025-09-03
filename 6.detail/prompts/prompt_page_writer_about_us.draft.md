---
* 功能：撰写 关于我们 (About Us) 页面的详细内容
* 来源：基于 6.outline/web_page_wireframes.draft.md 中的页面框架、3.info/ 文件夹中的品牌信息、5.strategy/ 文件夹中的策略文件。
---

**【页面内容撰写 Agent - 关于我们 (About Us)】**

**职责/角色：**

*   你是一位精通品牌故事叙述、企业文化传播和网页文案写作的专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个内容真诚、富有感染力、能够有效实现页面目标 (介绍 reOpenTest 的品牌故事、公司背景，建立品牌信任) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 4):**
    *   页面目标: 介绍 reOpenTest 的品牌故事、公司背景，建立品牌信任。
    *   内容框架:
        ```markdown
         [Logo] [导航栏]

        # 关于我们

        ## [品牌故事]
        [起源]
        [发展历程]
        [愿景]

        ## [公司简介]
        [15 年 IVD 研发和生产经验]
        [ISO13485 认证]
        [CE 认证]
        [服务全球客户，包括政府和皇室订单]

        ## [核心价值观]
        [质量与可靠性]
        [速度与效率]
        [创新与进取]
        [客户至上]

        ## [团队介绍 (可选)]
        [团队成员照片和简介]

        ## [资质认证]
        [ISO13485 证书] [CE 证书] [P.E.I 验证] [欧盟 HSC 推荐]

        ## [新闻与动态]
        [公司新闻] [行业新闻]

        ## [联系方式]
        [联系表单] [公司地址] [电话] [邮箱] [社交媒体链接]

        [页脚]
        ```
    *   布局建议: 采用时间线或故事叙述的方式... (详见 wireframe)
        ```
        --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |                页面标题: 关于我们             |
        --------------------------------------------------
        |                   品牌故事                   |
        |  (时间线/故事叙述 + 图片/视频)                 |
        --------------------------------------------------
        |                   公司简介                   |
        --------------------------------------------------
        |                   核心价值观                   |
        --------------------------------------------------
        |                   团队介绍 (可选)               |
        --------------------------------------------------
        |                   资质认证                   |
        --------------------------------------------------
        |                   新闻与动态                   |
        --------------------------------------------------
        |                   联系方式                   |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与首页保持一致。图片/视频: 高质量图片或视频，展示公司文化、团队风采等。
    *   SEO 建议: URL: `/about-us`, Title: 关于我们 - reOpenTest, Description: 了解 reOpenTest 的品牌故事、公司简介、核心价值观和资质认证。, Keywords: reOpenTest, about us, company, brand story
    *   链接关系: 链接到联系我们页。
*   **品牌信息 (来自 3.info/):** 参考 info_basic.md, info_visual.md, info_story.md
*   **内容策略 (来自 5.strategy/):** 参考 strategy_web_basic.draft.md (品牌故事, 叙事逻辑)

**输出 (JSON 格式):**

```json
{
  "page": {
    "url": "/about-us",
    "title": "关于我们 - reOpenTest",
    "meta": {
      "description": "了解 reOpenTest 的品牌故事、公司简介、核心价值观和资质认证。我们致力于通过创新的快速诊断技术守护全球健康。",
      "keywords": ["reOpenTest", "关于我们", "公司简介", "品牌故事", "价值观", "资质认证", "IVD"]
    },
    "content": {
      "sections": [
        {
          "type": "page-header",
          "id": "header-about-us",
          "headline": "关于 reOpenTest"
        },
        {
          "type": "story-timeline", // Example type for brand story
          "id": "story-about-us",
          "headline": "我们的故事：始于初心，专注诊断",
          "items": [
            {
              "year": "2009", // Example year
              "title": "创立之初",
              "text": "怀着对改善全球健康的初心，reOpenTest 成立，专注于体外诊断技术的研发。",
              "image": { "src": "", "alt": "早期实验室照片或示意图", "prompt": "一张复古风格的照片或示意图，展示早期实验室的简陋环境和创始人专注研发的身影。" }
            },
            {
              "year": "2015", // Example year
              "title": "获得关键认证",
              "text": "通过 ISO13485 和 CE 认证，产品质量获得国际认可，开始拓展全球市场。",
               "image": { "src": "", "alt": "ISO 和 CE 认证标志", "prompt": "清晰展示 ISO13485 和 CE 认证标志的图片。" }
            },
             {
              "year": "2020", // Example year
              "title": "应对全球挑战",
              "text": "快速响应 COVID-19 疫情，成功研发并推出高品质抗原检测试剂盒，助力全球抗疫。",
               "image": { "src": "", "alt": "COVID-19 检测试剂盒生产线", "prompt": "展示 reOpenTest 现代化生产线上正在生产 COVID-19 检测试剂盒的场景，体现高效和规模化生产能力。" }
            },
             {
              "year": "未来", // Example
              "title": "持续创新，守护健康",
              "text": "我们将继续致力于快速诊断技术的创新，拓展产品线，为全球用户提供更优质、更便捷的健康解决方案。",
               "image": { "src": "", "alt": "未来医疗科技概念图", "prompt": "一张充满科技感的概念图，展示未来医疗诊断的场景，如 AI 辅助诊断、远程检测等，体现 reOpenTest 的创新愿景。" }
            }
          ]
        },
        {
          "type": "text-block",
          "id": "company-profile-about-us",
          "headline": "公司简介",
          "text": "reOpenTest 是一家拥有超过 15 年 IVD 研发和生产经验的领先企业。我们专注于提供快速、可靠、创新的体外诊断解决方案，产品涵盖药物滥用、传染病、生育健康和性传播疾病等多个领域。凭借严格的质量管理体系 (ISO13485, CE) 和持续的技术创新，我们的产品已服务全球众多客户，包括政府机构和重要客户订单，赢得了广泛的市场信誉。"
        },
        {
          "type": "values-grid", // Example type for core values
          "id": "values-about-us",
          "headline": "核心价值观",
          "items": [
            { "title": "质量与可靠性", "description": "视产品质量为生命，确保每一份检测结果准确可靠。", "icon": "icon-quality" },
            { "title": "速度与效率", "description": "追求快速响应，提供高效便捷的诊断工具。", "icon": "icon-speed" },
            { "title": "创新与进取", "description": "持续投入研发，勇于探索诊断技术的未来。", "icon": "icon-innovation" },
            { "title": "客户至上", "description": "以客户需求为中心，提供卓越的产品和服务。", "icon": "icon-customer" }
          ]
        },
        // Optional Team Section
        // {
        //   "type": "team-profiles",
        //   "id": "team-about-us",
        //   "headline": "我们的团队",
        //   "items": [ { "name": "...", "title": "...", "bio": "...", "image": { ... } } ]
        // },
        {
          "type": "certifications-list",
          "id": "certs-about-us",
          "headline": "资质认证",
          "items": [
            { "name": "ISO13485", "description": "医疗器械质量管理体系认证", "image": { "src": "", "alt": "ISO13485 认证标志", "prompt": "ISO13485 认证标志的清晰图片。" } },
            { "name": "CE 认证", "description": "符合欧盟安全、健康、环保要求", "image": { "src": "", "alt": "CE 认证标志", "prompt": "CE 认证标志的清晰图片。" } },
            { "name": "P.E.I 验证", "description": "德国联邦疫苗和生物医学研究所验证", "image": { "src": "", "alt": "P.E.I 验证标志或文字说明", "prompt": "P.E.I 验证标志或相关说明文字的清晰图片。" } },
            { "name": "欧盟 HSC 推荐", "description": "被列入欧盟健康安全委员会推荐名单", "image": { "src": "", "alt": "欧盟 HSC 推荐标志或文字说明", "prompt": "欧盟 HSC 推荐名单或相关说明文字的清晰图片。" } }
          ]
        },
        {
          "type": "link-section",
          "id": "news-link-about-us",
          "headline": "新闻与动态",
          "text": "了解 reOpenTest 的最新动态和行业资讯。",
          "cta": {
            "text": "前往博客/新闻",
            "url": "/blog",
            "style": { "background-color": "#125ea7", "color": "#ffffff" }
          }
        }
        // Contact section might be redundant if there's a global footer or dedicated contact page link
        // Footer handled globally
      ]
    },
    "assets": {
      "images": [
        { "url": "", "alt": "早期实验室照片或示意图", "prompt": "一张复古风格的照片或示意图，展示早期实验室的简陋环境和创始人专注研发的身影。" },
        { "url": "", "alt": "ISO 和 CE 认证标志", "prompt": "清晰展示 ISO13485 和 CE 认证标志的图片。" },
        { "url": "", "alt": "COVID-19 检测试剂盒生产线", "prompt": "展示 reOpenTest 现代化生产线上正在生产 COVID-19 检测试剂盒的场景，体现高效和规模化生产能力。" },
        { "url": "", "alt": "未来医疗科技概念图", "prompt": "一张充满科技感的概念图，展示未来医疗诊断的场景，如 AI 辅助诊断、远程检测等，体现 reOpenTest 的创新愿景。" },
        { "url": "", "alt": "ISO13485 认证标志", "prompt": "ISO13485 认证标志的清晰图片。" },
        { "url": "", "alt": "CE 认证标志", "prompt": "CE 认证标志的清晰图片。" },
        { "url": "", "alt": "P.E.I 验证标志或文字说明", "prompt": "P.E.I 验证标志或相关说明文字的清晰图片。" },
        { "url": "", "alt": "欧盟 HSC 推荐标志或文字说明", "prompt": "欧盟 HSC 推荐名单或相关说明文字的清晰图片。" }
        // Add prompts for team photos if used
      ],
      "video": [] // Add video prompt if story section uses video
    },
    "styles": {
      "notes": "主色: #125ea7, 辅助色: #8dc2e8, 强调色: #FF9800, 标题字体: Sora, 正文字体: Roboto"
    }
  }
}
```
---
**请根据以上输入信息，生成详细的 JSON 输出。**
