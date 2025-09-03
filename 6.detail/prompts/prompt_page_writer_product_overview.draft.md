---
* 功能：撰写 产品总览 (Product Overview) 页面的详细内容 - 通用模板
* 来源：页面框架 **从文件 6.outline/web_page_wireframes.md 中加载**，品牌信息来自 3.info/ 文件夹，内容策略来自 5.strategy/ 文件夹。
---

**【页面内容撰写 Agent - 产品总览 (Product Overview) - 通用模板】**

**职责/角色：**

*   你是一位精通产品营销、网页设计和文案写作的产品页面构建专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个内容清晰、导航便捷、能够有效实现页面目标 (展示所有产品类别，方便用户快速找到所需产品) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 2):**
    *   页面目标: 展示所有产品类别，方便用户快速找到所需产品。
    *   内容框架:
        ```markdown
        [Logo] [导航栏]

        # 产品与服务

        ## [产品类别列表]
        [类别 1: DoA]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 2: 传染病]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 3: Fertility]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 4: STDs]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]

        [页脚]
        ```
    *   布局建议: 采用列表或网格布局... (详见 wireframe)
        ```
         --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |                页面标题: 产品与服务             |
        --------------------------------------------------
        |  [产品类别 1] [产品类别 2] [产品类别 3] [产品类别 4] |
        |  (图片+介绍+按钮) (图片+介绍+按钮) ...          |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与首页保持一致。图片: 高质量产品图片。CTA按钮: 醒目，引导用户点击。
    *   SEO 建议: URL: `/products`, Title: 产品与服务 - reOpenTest, Description: reOpenTest 提供 DoA、传染病、Fertility、STDs 等各类快速诊断产品。, Keywords: reOpenTest, rapid test, IVD, 快速诊断, 产品, DoA, 传染病, Fertility, STDs
    *   链接关系: **(请从 web_page_wireframes.md 文件中 Section 2 加载)** 链接到各个产品详情页。
*   **品牌信息 (来自 3.info/):** 参考 3.info/ 文件夹中的品牌信息
*   **内容策略 (来自 5.strategy/):** 参考 5.strategy/ 文件夹中的内容策略

**输出 (JSON 格式):**

**目标JSON:**
```json
{
  "pageType": "product-overview",
  "page": {
    "url": "/products",
    "title": "[品牌名称] - 产品与服务",
    "meta": {
      "description": "[产品总览页面SEO描述]",
      "keywords": ["[核心关键词]", "[产品类别关键词]"]
    },
    "content": {
      "sections": [
        // ... (Page Header Section JSON structure) ...
        // ... (Product Categories Grid Section JSON structure) ...
      ]
    },
    "assets": {
      "images": [
        // ... (Image assets for product categories) ...
      ],
      "video": []
    },
    "styles": {
      "notes": "[视觉风格指南]"
    }
  }
}
```

**参考JSON示例:**
```json
{
  "pageType": "product-overview",
  "page": {
    "url": "/products",
    "title": "产品与服务 - reOpenTest",
    "meta": {
      "description": "reOpenTest 提供 DoA、传染病、Fertility、STDs 等各类快速诊断产品。",
      "keywords": ["reOpenTest", "rapid test", "IVD", "产品"]
    },
    "content": {
      "sections": [
        {
          "type": "page-header",
          "headline": "产品与服务"
        },
        {
          "type": "grid",
          "items": [
            { "title": "DoA", "description": "药物滥用检测", "link": "/products/doa" },
            { "title": "传染病", "description": "传染病检测", "link": "/products/infectious-diseases" }
          ]
        }
      ]
    }
  }
}
```
---
* 功能：撰写 产品总览 (Product Overview) 页面的详细内容 - 通用模板
* 来源：页面框架 **从文件 6.outline/web_page_wireframes.md 中加载**，品牌信息来自 3.info/ 文件夹，内容策略来自 5.strategy/ 文件夹。
---

**【页面内容撰写 Agent - 产品总览 (Product Overview) - 通用模板】**

**职责/角色：**

*   你是一位精通产品营销、网页设计和文案写作的产品页面构建专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个内容清晰、导航便捷、能够有效实现页面目标 (展示所有产品类别，方便用户快速找到所需产品) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 2):**
    *   页面目标: 展示所有产品类别，方便用户快速找到所需产品。
    *   内容框架:
        ```markdown
        [Logo] [导航栏]

        # 产品与服务

        ## [产品类别列表]
        [类别 1: DoA]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 2: 传染病]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 3: Fertility]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]
        [类别 4: STDs]
        [图片]
        [简要介绍]
        [行动号召按钮: 查看详情]

        [页脚]
        ```
    *   布局建议: 采用列表或网格布局... (详见 wireframe)
        ```
         --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |                页面标题: 产品与服务             |
        --------------------------------------------------
        |  [产品类别 1] [产品类别 2] [产品类别 3] [产品类别 4] |
        |  (图片+介绍+按钮) (图片+介绍+按钮) ...          |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与首页保持一致。图片: 高质量产品图片。CTA按钮: 醒目，引导用户点击。
    *   SEO 建议: URL: `/products`, Title: 产品与服务 - reOpenTest, Description: reOpenTest 提供 DoA、传染病、Fertility、STDs 等各类快速诊断产品。, Keywords: reOpenTest, rapid test, IVD, 快速诊断, 产品, DoA, 传染病, Fertility, STDs
    *   链接关系: 链接到各个产品详情页。
*   **品牌信息 (来自 3.info/):** 参考 info_basic.md, info_visual.md
*   **内容策略 (来自 5.strategy/):** 参考 strategy_web_basic.draft.md (产品分类)

**输出 (JSON 格式):**

```json
{
  "page": {
    "url": "/products",
    "title": "产品与服务 - reOpenTest",
    "meta": {
      "description": "reOpenTest 提供 DoA、传染病、Fertility、STDs 等各类快速诊断产品。",
      "keywords": ["reOpenTest", "rapid test", "IVD", "快速诊断", "产品", "DoA", "传染病", "Fertility", "STDs"]
    },
    "content": {
      "sections": [
        {
          "type": "page-header", // Example type for page title
          "id": "header-product-overview",
          "headline": "产品与服务"
        },
        {
          "type": "grid", // Using grid for category list
          "id": "product-categories-overview",
          "items": [
            {
              "title": "DoA (药物滥用检测)",
              "description": "提供尿液、唾液、毛发等多种样本类型的快速药物滥用检测产品，结果准确可靠。",
              "image": {
                "src": "",
                "alt": "DoA 快速检测试剂盒",
                "prompt": "一组 reOpenTest DoA 快速检测试剂盒（尿液杯、唾液试纸等）整齐排列，背景干净明亮，突出产品的多样性和专业性。"
              },
              "cta": {
                "text": "查看详情",
                "url": "/products/doa",
                "style": { "background-color": "#125ea7", "color": "#ffffff" }
              }
            },
            {
              "title": "传染病检测",
              "description": "覆盖呼吸道、消化道、血液传播等多种传染病的快速筛查试剂，助力早期发现和防控。",
              "image": {
                "src": "",
                "alt": "传染病快速检测试剂盒",
                "prompt": "展示 reOpenTest 传染病快速检测试剂盒（如流感、COVID-19 试纸）的应用场景，例如医生为患者进行检测，背景为诊所环境。"
              },
              "cta": {
                "text": "查看详情",
                "url": "/products/infectious-diseases",
                "style": { "background-color": "#125ea7", "color": "#ffffff" }
              }
            },
            {
              "title": "Fertility (生育健康检测)",
              "description": "提供排卵、早孕等便捷可靠的居家生育健康检测产品，帮助用户更好地了解自身状况。",
              "image": {
                "src": "",
                "alt": "Fertility 快速检测试剂盒",
                "prompt": "温馨居家环境中，展示 reOpenTest 生育健康检测试剂盒（排卵试纸、早孕试纸），旁边放有日历或鲜花，营造关怀、希望的氛围。"
              },
              "cta": {
                "text": "查看详情",
                "url": "/products/fertility",
                "style": { "background-color": "#125ea7", "color": "#ffffff" }
              }
            },
            {
              "title": "STDs (性传播疾病检测)",
              "description": "提供保护隐私、操作简便的性传播疾病快速检测产品，关注个人健康。",
              "image": {
                "src": "",
                "alt": "STDs 快速检测试剂盒",
                "prompt": "简洁私密的环境中，展示 reOpenTest STDs 快速检测试剂盒包装，强调产品的隐私保护和易用性。"
              },
              "cta": {
                "text": "查看详情",
                "url": "/products/stds",
                "style": { "background-color": "#125ea7", "color": "#ffffff" }
              }
            }
          ]
        }
        // Footer handled globally
      ]
    },
    "assets": {
      "images": [
        { "url": "", "alt": "DoA 快速检测试剂盒", "prompt": "一组 reOpenTest DoA 快速检测试剂盒（尿液杯、唾液试纸等）整齐排列，背景干净明亮，突出产品的多样性和专业性。" },
        { "url": "", "alt": "传染病快速检测试剂盒", "prompt": "展示 reOpenTest 传染病快速检测试剂盒（如流感、COVID-19 试纸）的应用场景，例如医生为患者进行检测，背景为诊所环境。" },
        { "url": "", "alt": "Fertility 快速检测试剂盒", "prompt": "温馨居家环境中，展示 reOpenTest 生育健康检测试剂盒（排卵试纸、早孕试纸），旁边放有日历或鲜花，营造关怀、希望的氛围。" },
        { "url": "", "alt": "STDs 快速检测试剂盒", "prompt": "简洁私密的环境中，展示 reOpenTest STDs 快速检测试剂盒包装，强调产品的隐私保护和易用性。" }
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
