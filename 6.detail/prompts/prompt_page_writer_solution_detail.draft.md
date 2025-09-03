---
* 功能：撰写 解决方案详情 (Solution Detail) 页面的详细内容 (以医院感染控制为例)
* 来源：基于 6.outline/web_page_wireframes.draft.md 中的页面框架、3.info/ 文件夹中的品牌信息、5.strategy/ 文件夹中的策略文件。
---

**【页面内容撰写 Agent - 解决方案详情 (Solution Detail)】**

**职责/角色：**

*   你是一位精通行业解决方案营销、网页设计和文案写作的专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个内容详实、逻辑清晰、能够有效实现页面目标 (介绍针对特定场景的解决方案，展示品牌专业性，吸引潜在客户) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 7, Hospital Infection Control Example):**
    *   页面目标: 介绍针对医院感染控制的解决方案，展示品牌专业性，吸引潜在客户。
    *   内容框架:
        ```markdown
        [Logo] [导航栏]

        # 医院感染控制解决方案

        [引言: 医院感染控制的挑战和重要性]

        ## [reOpenTest 解决方案介绍]
        [优势 1: 快速诊断，及时发现感染源]
        [优势 2: 准确可靠，指导精准用药]
        [优势 3: 简便易用，降低操作难度]
        [优势 4: 种类齐全，满足不同需求]

        ## [相关产品推荐]
        [产品 1] [产品 2] [产品 3] ...
        [每个产品: 图片 + 名称 + 简要描述 + 行动号召按钮]

        ## [成功案例]
        [案例 1] [案例 2] [案例 3] ...

        ## [行动号召]
        [联系我们，获取定制化解决方案]

        [页脚]
        ```
    *   布局建议: 采用清晰、有条理的布局... (详见 wireframe)
        ```
        --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |          页面标题: 医院感染控制解决方案         |
        --------------------------------------------------
        |                     引言                     |
        --------------------------------------------------
        |           reOpenTest 解决方案介绍             |
        |             (优势 1, 优势 2, ...)             |
        --------------------------------------------------
        |                   相关产品推荐                 |
        --------------------------------------------------
        |                     成功案例                   |
        --------------------------------------------------
        |                   行动号召                   |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与首页保持一致。图片: 高质量图片或图表，展示应用场景和效果。CTA按钮: 醒目，使用对比色。
    *   SEO 建议: URL: `/solutions/hospital-infection-control`, Title: 医院感染控制解决方案 - reOpenTest, Description: 了解 reOpenTest 如何帮助您应对医院感染控制的挑战，提供快速、准确、可靠的诊断解决方案。, Keywords: 医院感染控制, 快速诊断, reOpenTest, 解决方案
    *   链接关系: 链接到相关产品详情页、联系我们页面。
*   **品牌信息 (来自 3.info/):** 参考 info_basic.md, info_visual.md
*   **内容策略 (来自 5.strategy/):** 参考 strategy_web_basic.draft.md (解决方案相关主题, 内容类型)
*   **具体解决方案信息:** (Agent 需要能够获取或被提供具体某个解决方案的信息，例如 "医院感染控制解决方案")

**输出 (JSON 格式):**

```json
{
  "page": {
    // Example for "Hospital Infection Control Solution"
    "url": "/solutions/hospital-infection-control",
    "title": "医院感染控制解决方案 - reOpenTest",
    "meta": {
      "description": "了解 reOpenTest 如何帮助您应对医院感染控制的挑战，提供快速、准确、可靠的诊断解决方案，有效预防和控制院内感染。",
      "keywords": ["reOpenTest", "医院感染控制", "院内感染", "HAI", "快速诊断", "解决方案", "传染病检测"]
    },
    "content": {
      "sections": [
        {
          "type": "solution-header",
          "id": "header-solution-hic",
          "headline": "医院感染控制解决方案",
          "image": { // Optional header image
            "src": "",
            "alt": "医生在医院环境中使用快速检测试剂",
            "prompt": "专业的医生或护士在明亮的医院环境（如病房或实验室）中使用 reOpenTest 快速检测试剂，表情专注，体现专业性和对感染控制的重视。"
          }
        },
        {
          "type": "text-block",
          "id": "intro-solution-hic",
          "headline": "应对医院感染控制的严峻挑战",
          "text": "医院内感染 (HAI) 是全球医疗系统面临的重大挑战，不仅增加患者痛苦和死亡率，也带来巨大的经济负担。快速、准确地识别感染源并采取有效控制措施至关重要。reOpenTest 提供全面的快速诊断解决方案，助力医疗机构有效预防和控制院内感染。"
        },
        {
          "type": "features", // Or use a custom 'solution-benefits' type
          "id": "benefits-solution-hic",
          "headline": "reOpenTest 解决方案优势",
          "items": [
            {
              "title": "快速诊断，及时发现",
              "description": "15分钟内获得多种常见病原体的检测结果，快速识别潜在感染源，为早期隔离和干预争取宝贵时间。",
              "icon": "icon-clock"
            },
            {
              "title": "准确可靠，指导治疗",
              "description": "高灵敏度和特异性确保检测结果的准确性，为临床医生提供可靠依据，指导精准用药，避免抗生素滥用。",
              "icon": "icon-target" // Example icon
            },
            {
              "title": "简便易用，提升效率",
              "description": "操作流程简单，无需复杂设备，可在床旁或实验室快速完成检测，减轻医护人员负担，提升工作效率。",
              "icon": "icon-play-circle" // Example icon
            },
            {
              "title": "种类齐全，全面覆盖",
              "description": "提供针对多种呼吸道、消化道、血液传播病原体的检测试剂，满足医院不同科室的感染控制需求。",
              "icon": "icon-list"
            }
          ]
        },
        {
          "type": "product-list", // Reusing product list type
          "id": "products-solution-hic",
          "headline": "相关产品推荐",
          "items": [
            // Populate with 1-3 relevant product links (e.g., MRSA test, C. difficile test, Flu test)
            {
              "title": "reOpenTest MRSA 快速检测试剂盒",
              "description": "快速筛查耐甲氧西林金黄色葡萄球菌，有效预防传播。",
              "image": { "src": "", "alt": "MRSA 检测试剂盒", "prompt": "reOpenTest MRSA 快速检测试剂盒的清晰产品照片。" },
              "cta": { "text": "查看详情", "url": "/products/infectious-diseases/mrsa-test" }
            },
             {
              "title": "reOpenTest C. difficile 毒素 A/B 检测试剂盒",
              "description": "快速检测艰难梭菌毒素，辅助诊断相关腹泻。",
              "image": { "src": "", "alt": "C. difficile 检测试剂盒", "prompt": "reOpenTest C. difficile 毒素 A/B 检测试剂盒的清晰产品照片。" },
              "cta": { "text": "查看详情", "url": "/products/infectious-diseases/c-difficile-test" }
            }
            // ... more products
          ]
        },
        {
          "type": "case-studies", // Or testimonials
          "id": "casestudies-solution-hic",
          "headline": "成功案例",
          "items": [
            // Populate with 1-2 brief case study summaries or testimonials
            {
              "quote": "引入 reOpenTest 快速诊断方案后，我们医院的 HAI 发生率显著降低，患者管理效率也得到了提升。",
              "author": { "name": "某三甲医院感染科主任", "title": "" }
            }
          ]
        },
        {
          "type": "cta-section",
          "id": "cta-solution-hic",
          "headline": "获取定制化医院感染控制解决方案",
          "text": "立即联系我们的专家团队，了解 reOpenTest 如何帮助您的机构提升感染控制水平。",
          "cta": {
            "text": "联系我们",
            "url": "/contact-us?solution=hospital-infection-control",
            "style": { "background-color": "#FF9800", "color": "#ffffff" }
          }
        }
        // Footer handled globally
      ]
    },
    "assets": {
      "images": [
        { "url": "", "alt": "医生在医院环境中使用快速检测试剂", "prompt": "专业的医生或护士在明亮的医院环境（如病房或实验室）中使用 reOpenTest 快速检测试剂，表情专注，体现专业性和对感染控制的重视。" },
        { "url": "", "alt": "MRSA 检测试剂盒", "prompt": "reOpenTest MRSA 快速检测试剂盒的清晰产品照片。" },
        { "url": "", "alt": "C. difficile 检测试剂盒", "prompt": "reOpenTest C. difficile 毒素 A/B 检测试剂盒的清晰产品照片。" }
        // Add prompts for other relevant images/icons
      ],
      "video": []
    },
    "styles": {
      "notes": "主色: #125ea7, 辅助色: #8dc2e8, 强调色: #FF9800, 标题字体: Sora, 正文字体: Roboto"
    }
  }
}
```
---
**请根据以上输入信息，生成详细的 JSON 输出。**
