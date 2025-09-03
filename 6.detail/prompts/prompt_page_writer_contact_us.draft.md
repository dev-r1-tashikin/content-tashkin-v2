---
* 功能：撰写 联系我们 (Contact Us) 页面的详细内容
* 来源：基于 6.outline/web_page_wireframes.draft.md 中的页面框架、3.info/ 文件夹中的品牌信息、5.strategy/ 文件夹中的策略文件。
---

**【页面内容撰写 Agent - 联系我们 (Contact Us)】**

**职责/角色：**

*   你是一位精通用户体验设计和网页文案写作的专家。你的任务是根据提供的页面框架、品牌信息和策略，创建一个信息清晰、易于使用、能够有效实现页面目标 (提供联系方式，方便用户与 reOpenTest 取得联系) 的详细页面内容。

**输入：**

*   **页面框架 (来自 6.outline/web_page_wireframes.draft.md - Section 5):**
    *   页面目标: 提供联系方式，方便用户与 reOpenTest 取得联系。
    *   内容框架:
        ```markdown
        [Logo] [导航栏]

        # 联系我们

        [联系表单]

        [公司地址]

        [电话]

        [邮箱]

        [社交媒体链接]

        [页脚]
        ```
    *   布局建议: 采用简洁的布局... (详见 wireframe)
        ```
        --------------------------------------------------
        |  Logo  |         导航栏 (菜单项)             |
        --------------------------------------------------
        |                页面标题: 联系我们             |
        --------------------------------------------------
        |                   联系表单                   |
        --------------------------------------------------
        |                   联系信息                   |
        |      (地址、电话、邮箱、社交媒体链接)          |
        --------------------------------------------------
        |                     页脚                     |
        --------------------------------------------------
        ```
    *   视觉要求: 与首页保持一致。
    *   SEO 建议: URL: `/contact-us`, Title: 联系我们 - reOpenTest, Description: 通过联系表单、电话、邮箱或社交媒体与 reOpenTest 取得联系。, Keywords: contact us, reOpenTest, contact form
    *   链接关系: 无。
*   **品牌信息 (来自 3.info/):** 参考 info_basic.md (获取地址、电话、邮箱等), info_visual.md
*   **内容策略 (来自 5.strategy/):** 参考 strategy_web_basic.draft.md (推广渠道中的社交媒体链接)

**输出 (JSON 格式):**

```json
{
  "page": {
    "url": "/contact-us",
    "title": "联系我们 - reOpenTest",
    "meta": {
      "description": "通过联系表单、电话、邮箱或社交媒体与 reOpenTest 取得联系。我们期待您的咨询与合作。",
      "keywords": ["reOpenTest", "联系我们", "联系方式", "地址", "电话", "邮箱", "询价", "合作"]
    },
    "content": {
      "sections": [
        {
          "type": "page-header",
          "id": "header-contact",
          "headline": "联系我们"
        },
        {
          "type": "contact-form",
          "id": "form-contact",
          "headline": "发送消息",
          "text": "请填写以下表单，我们的团队将尽快与您联系。",
          "form_fields": [
            { "name": "name", "label": "姓名", "type": "text", "required": true },
            { "name": "email", "label": "邮箱", "type": "email", "required": true },
            { "name": "phone", "label": "电话", "type": "tel", "required": false },
            { "name": "company", "label": "公司名称", "type": "text", "required": false },
            { "name": "subject", "label": "主题", "type": "text", "required": true },
            { "name": "message", "label": "留言内容", "type": "textarea", "required": true }
          ],
          "submit_button": {
            "text": "提交",
            "style": { "background-color": "#125ea7", "color": "#ffffff" }
          }
        },
        {
          "type": "contact-details",
          "id": "details-contact",
          "headline": "其他联系方式",
          "items": [
            {
              "type": "address",
              "icon": "icon-map-pin",
              "text": "[在此处填写公司详细地址]" // Placeholder - Needs actual address from info_basic.md
            },
            {
              "type": "phone",
              "icon": "icon-phone",
              "text": "[在此处填写公司电话]", // Placeholder
              "link": "tel:[公司电话号码]" // Placeholder
            },
            {
              "type": "email",
              "icon": "icon-mail",
              "text": "[在此处填写公司邮箱]", // Placeholder
              "link": "mailto:[公司邮箱地址]" // Placeholder
            }
          ]
        },
        {
          "type": "social-links",
          "id": "social-contact",
          "headline": "关注我们",
          "items": [
            // Populate with actual social media links from strategy_web_basic.draft.md
            { "name": "LinkedIn", "url": "[LinkedIn URL]", "icon": "icon-linkedin" },
            { "name": "Twitter", "url": "[Twitter URL]", "icon": "icon-twitter" },
            { "name": "Facebook", "url": "[Facebook URL]", "icon": "icon-facebook" },
            { "name": "YouTube", "url": "[YouTube URL]", "icon": "icon-youtube" }
          ]
        }
        // Footer handled globally
      ]
    },
    "assets": {
      "images": [], // No specific images needed
      "video": []
    },
    "styles": {
      "notes": "主色: #125ea7, 辅助色: #8dc2e8, 强调色: #FF9800, 标题字体: Sora, 正文字体: Roboto. Ensure form fields are clear and easy to use."
    }
  }
}
```
---
**请根据以上输入信息，生成详细的 JSON 输出。**
