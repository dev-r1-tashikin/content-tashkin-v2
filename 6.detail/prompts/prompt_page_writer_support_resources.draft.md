---
* 功能：撰写 支持与资源 (Support & Resources) 页面的详细内容
* 来源：基于 6.outline/web_page_wireframes.draft.md 中的页面框架、3.info/ 文件夹中的品牌信息、5.strategy/ 文件夹中的策略文件。
---

**【页面内容撰写 Agent - 支持与资源 (Support & Resources)】**

**职责/角色：**

*   你是一位精通客户支持、技术文档撰写和信息架构设计的专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个信息清晰、易于查找、能够有效实现页面目标 (提供用户支持和相关资源，解答常见问题，提升用户体验) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 9):**
    *   页面目标: 提供用户支持和相关资源，解答常见问题，提升用户体验。
    *   内容框架:
        ```markdown
          [Logo] [导航栏]

          # 支持与资源

          ## [常见问题解答 (FAQ)]
          [问题 1] [答案 1]
          [问题 2] [答案 2]
          ...

          ## [技术文档下载]
          [文档 1 标题] [下载链接]
          [文档 2 标题] [下载链接]
          ...

          ## [联系客服]
          [联系表单] 或 [在线聊天入口]

          [页脚]
        ```
    *   布局建议: 采用清晰、有条理的布局... (详见 wireframe)
        ```
        --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |              页面标题: 支持与资源             |
        --------------------------------------------------
        |                 常见问题解答 (FAQ)             |
        --------------------------------------------------
        |                   技术文档下载                 |
        --------------------------------------------------
        |                   联系客服                   |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与网站整体风格保持一致。
    *   SEO 建议: URL: `/support` 或 `/resources`, Title: 支持与资源 - reOpenTest, Description: 获取 reOpenTest 的客户支持、技术文档、常见问题解答等。, Keywords: 支持, 资源, reOpenTest, FAQ, 技术文档, 联系客服
    *   链接关系: 链接到联系我们页面或在线客服。
*   **品牌信息 (来自 3.info/):** 参考 info_basic.md, info_visual.md
*   **内容策略 (来自 5.strategy/):** 参考 strategy_web_basic.draft.md (内容类型: FAQ, 技术文档)
*   **具体支持信息:** (Agent 需要能够获取或被提供常见的 FAQ、可下载的技术文档列表、售后服务政策等)

**输出 (JSON 格式):**

```json
{
  "page": {
    "url": "/support",
    "title": "支持与资源 - reOpenTest",
    "meta": {
      "description": "获取 reOpenTest 的客户支持、常见问题解答 (FAQ)、技术文档下载和售后服务信息。",
      "keywords": ["reOpenTest", "支持", "资源", "FAQ", "常见问题", "技术文档", "下载", "联系客服", "售后服务"]
    },
    "content": {
      "sections": [
        {
          "type": "page-header",
          "id": "header-support",
          "headline": "支持与资源"
        },
        {
          "type": "faq",
          "id": "faq-support",
          "headline": "常见问题解答 (FAQ)",
          "items": [
            // Populate with common questions and answers
            {
              "question": "如何购买 reOpenTest 产品？",
              "answer": "您可以通过我们的在线商店（如果适用）或联系我们的销售团队进行购买。请访问 [联系我们](/contact-us) 页面获取详细信息。"
            },
            {
              "question": "产品保质期是多久？如何储存？",
              "answer": "大部分产品的保质期为 24 个月。请在 2-30°C 的干燥环境中储存，避免阳光直射。具体请参照产品说明书。"
            },
            {
              "question": "检测结果如何判读？",
              "answer": "请严格按照产品说明书中的图示和说明进行结果判读。如有疑问，请咨询专业医疗人员或联系我们的技术支持。"
            },
            {
              "question": "如果检测结果无效怎么办？",
              "answer": "请检查操作步骤是否正确，样本量是否足够。如果问题仍然存在，请联系我们的客服获取帮助。"
            }
            // ... more FAQs
          ]
        },
        {
          "type": "downloads",
          "id": "downloads-support",
          "headline": "技术文档下载",
          "items": [
            // Populate with available documents
            {
              "title": "reOpenTest COVID-19 抗原快速检测试剂盒 - 产品手册",
              "url": "/downloads/covid-19-antigen-brochure.pdf",
              "icon": "icon-pdf" // Example icon
            },
            {
              "title": "reOpenTest COVID-19 抗原快速检测试剂盒 - 使用说明书",
              "url": "/downloads/covid-19-antigen-manual.pdf",
              "icon": "icon-pdf"
            },
             {
              "title": "reOpenTest DoA 尿液检测杯 - 产品手册",
              "url": "/downloads/doa-urine-cup-brochure.pdf",
              "icon": "icon-pdf"
            }
            // ... more documents
          ]
        },
         {
          "type": "text-block", // Section for After-Sales Policy (mentioned in strategy but not wireframe)
          "id": "aftersales-support",
          "headline": "售后服务政策",
          "text": "reOpenTest 致力于为客户提供优质的售后服务。如果您在使用过程中遇到任何问题，或对产品质量有疑问，请及时联系我们的客服团队。我们将根据具体情况提供技术支持、换货或退款服务。详细政策请参考 [售后服务条款](/terms#after-sales)。" // Example text
        },
        {
          "type": "contact-support",
          "id": "contact-support-section",
          "headline": "需要更多帮助？",
          "text": "如果您在常见问题或文档中找不到答案，请随时联系我们的客服团队。",
          "cta": {
            "text": "联系客服",
            "url": "/contact-us", // Link to contact page or potentially a chat widget
            "style": { "background-color": "#125ea7", "color": "#ffffff" }
          }
          // Could also include direct phone/email here if desired
        }
        // Footer handled globally
      ]
    },
    "assets": {
      "images": [], // No specific images requested in wireframe, icons handled in JSON
      "video": [],
      "documents": [ // List documents for reference
         "/downloads/covid-19-antigen-brochure.pdf",
         "/downloads/covid-19-antigen-manual.pdf",
         "/downloads/doa-urine-cup-brochure.pdf"
         // ... more document paths
      ]
    },
    "styles": {
      "notes": "主色: #125ea7, 辅助色: #8dc2e8, 强调色: #FF9800, 标题字体: Sora, 正文字体: Roboto. FAQ section might use accordion style."
    }
  }
}
```
---
**请根据以上输入信息，生成详细的 JSON 输出。**
