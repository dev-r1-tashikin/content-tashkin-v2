{
    "page_slug": "order-online",
    "page_url": "/order-online",
  "pageMetadata": {
    "pageType": "Account & Ordering Hub Page",
    "title": "客户中心 - reOpenTest",
    "description": "登录您的 reOpenTest 账户，访问在线订购系统、管理订单、查看信息并获取支持。",
    "urlSlug": "order-online",
    "targetAudience": "reOpenTest 现有注册客户 (经销商、医疗机构、政府客户等)",
    "coreMessage": "您的 reOpenTest 在线中心：轻松订购，便捷管理。"
  },
  "pageHeader": "[全局页眉占位符]",
  "mainContent": {
    "containerClass": "order-hub-container",
    "style": "max-width: 1200px; margin: 0 auto; padding: 2rem 1rem;",
    "sections": [
      {
        "sectionId": "welcome",
        "elementType": "section",
        "className": "welcome-section",
        "style": "text-align: center; margin-bottom: 2rem;",
        "content": [
          {
            "elementType": "h1",
            "style": "font-family: Sora, sans-serif; color: var(--primary-color, #125ea7); font-weight: 600;",
            "text": "reOpenTest 客户中心"
          },
          {
            "elementType": "p",
            "style": "font-family: Roboto, sans-serif; color: var(--neutral-color, #424242); font-size: 1.1rem;",
            "text": "欢迎！请登录以访问在线订购、账户管理及支持服务。"
          }
        ]
      },
      {
        "sectionId": "login",
        "elementType": "section",
        "className": "login-module",
        "style": "background-color: #f8f9fa; padding: 2rem; border-radius: 8px; max-width: 500px; margin: 0 auto 3rem auto; box-shadow: 0 2px 4px rgba(0,0,0,0.1);",
        "content": [
          {
            "elementType": "h2",
            "style": "font-family: Sora, sans-serif; text-align: center; margin-bottom: 1.5rem; color: var(--primary-color, #125ea7);",
            "text": "客户登录"
          },
          {
            "elementType": "form",
            "attributes": { "action": "[登录处理URL]", "method": "post" },
            "content": [
              {
                "elementType": "div",
                "style": "margin-bottom: 1rem;",
                "content": [
                  { "elementType": "label", "attributes": { "for": "username" }, "style": "display: block; margin-bottom: 0.5rem; font-family: Roboto, sans-serif; font-weight: 500;", "text": "用户名或邮箱" },
                  { "elementType": "input", "attributes": { "type": "text", "id": "username", "name": "username", "required": true, "placeholder": "请输入您的用户名或邮箱" }, "style": "width: 100%; padding: 0.75rem; border: 1px solid #ced4da; border-radius: 4px; font-family: Roboto, sans-serif;" }
                ]
              },
              {
                "elementType": "div",
                "style": "margin-bottom: 1rem;",
                "content": [
                  { "elementType": "label", "attributes": { "for": "password" }, "style": "display: block; margin-bottom: 0.5rem; font-family: Roboto, sans-serif; font-weight: 500;", "text": "密码" },
                  { "elementType": "input", "attributes": { "type": "password", "id": "password", "name": "password", "required": true, "placeholder": "请输入您的密码" }, "style": "width: 100%; padding: 0.75rem; border: 1px solid #ced4da; border-radius: 4px; font-family: Roboto, sans-serif;" }
                ]
              },
              {
                "elementType": "div",
                "style": "text-align: right; margin-bottom: 1.5rem;",
                "content": [
                  { "elementType": "a", "attributes": { "href": "/forgot-password" }, "style": "font-family: Roboto, sans-serif; color: var(--primary-color, #125ea7); text-decoration: none; font-size: 0.9rem;", "text": "忘记密码？" }
                ]
              },
              { "elementType": "button", "attributes": { "type": "submit" }, "style": "width: 100%; padding: 0.8rem; background-color: var(--primary-color, #125ea7); color: white; border: none; border-radius: 4px; font-family: Sora, sans-serif; font-size: 1rem; font-weight: 600; cursor: pointer;", "text": "登录" }
            ]
          }
        ]
      },
      {
        "sectionId": "functional-navigation",
        "elementType": "section",
        "className": "functional-navigation",
        "style": "display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 2rem; margin-bottom: 3rem;",
        "content": [
          {
            "elementType": "div",
            "className": "module online-ordering",
            "style": "border: 1px solid #e0e0e0; padding: 1.5rem; border-radius: 8px; text-align: center;",
            "content": [
              { "elementType": "h3", "style": "font-family: Sora, sans-serif; margin-bottom: 1rem; color: var(--primary-color, #125ea7);", "text": "在线订购" },
              { "elementType": "p", "style": "font-family: Roboto, sans-serif; margin-bottom: 1.5rem; color: var(--neutral-color, #424242);", "text": "通过我们的在线平台快速、便捷地订购所需产品。" },
              { "elementType": "a", "attributes": { "href": "https://medlab.tarinn.com", "target": "_blank", "class": "cta-button" }, "style": "display: inline-block; padding: 0.7rem 1.5rem; background-color: var(--accent-color, #FF9800); color: white; text-decoration: none; border-radius: 4px; font-family: Sora, sans-serif; font-weight: 600;", "text": "立即订购" }
            ]
          },
          {
            "elementType": "div",
            "className": "module account-management",
            "style": "border: 1px solid #e0e0e0; padding: 1.5rem; border-radius: 8px; text-align: center;",
            "content": [
              { "elementType": "h3", "style": "font-family: Sora, sans-serif; margin-bottom: 1rem; color: var(--primary-color, #125ea7);", "text": "账户管理" },
              { "elementType": "p", "style": "font-family: Roboto, sans-serif; margin-bottom: 1.5rem; color: var(--neutral-color, #424242);", "text": "管理您的账户信息、查看订单历史、发票及更多内容。" },
              { "elementType": "a", "attributes": { "href": "/account/dashboard", "class": "cta-button" }, "style": "display: inline-block; padding: 0.7rem 1.5rem; background-color: var(--primary-color, #125ea7); color: white; text-decoration: none; border-radius: 4px; font-family: Sora, sans-serif; font-weight: 600;", "text": "访问客户中心" },
              {
                "elementType": "ul",
                "style": "list-style: none; padding: 0; margin-top: 1.5rem; font-size: 0.9rem;",
                "content": [
                  { "elementType": "li", "style": "margin-bottom: 0.5rem;", "content": [{ "elementType": "a", "attributes": { "href": "/account/orders" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none;", "text": "查看订单历史" }] },
                  { "elementType": "li", "style": "margin-bottom: 0.5rem;", "content": [{ "elementType": "a", "attributes": { "href": "/account/addresses" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none;", "text": "管理地址簿" }] },
                  { "elementType": "li", "content": [{ "elementType": "a", "attributes": { "href": "/account/invoices" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none;", "text": "查看发票" }] }
                ]
              }
            ]
          }
        ]
      },
      {
        "sectionId": "support",
        "elementType": "section",
        "className": "support-help",
        "style": "text-align: center; margin-bottom: 3rem; padding: 1.5rem; background-color: #f8f9fa; border-radius: 8px;",
        "content": [
          { "elementType": "h2", "style": "font-family: Sora, sans-serif; margin-bottom: 1rem; color: var(--primary-color, #125ea7);", "text": "需要帮助？" },
          { "elementType": "p", "style": "font-family: Roboto, sans-serif; margin-bottom: 1rem; color: var(--neutral-color, #424242);", "text": "如果您在登录或使用过程中遇到任何问题，我们的支持团队随时为您服务。" },
          { "elementType": "p", "style": "font-family: Roboto, sans-serif; margin-bottom: 0.5rem; color: var(--neutral-color, #424242);", "text": "客户支持电话: **[在此插入官方支持电话]**" },
          { "elementType": "p", "content": [{ "elementType": "a", "attributes": { "href": "/contact-support" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none; font-weight: 500;", "text": "在线联系我们" }] }
        ]
      },
      {
        "sectionId": "resources",
        "elementType": "section",
        "className": "resources",
        "style": "margin-bottom: 3rem;",
        "content": [
          { "elementType": "h2", "style": "font-family: Sora, sans-serif; text-align: center; margin-bottom: 1.5rem; color: var(--primary-color, #125ea7);", "text": "常用资源" },
          {
            "elementType": "ul",
            "style": "list-style: none; padding: 0; text-align: center;",
            "content": [
              { "elementType": "li", "style": "margin-bottom: 0.8rem;", "content": [{ "elementType": "a", "attributes": { "href": "/resources/online-ordering-guide.pdf" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none; font-family: Roboto, sans-serif;", "text": "在线订购快速入门指南" }] },
              { "elementType": "li", "style": "margin-bottom: 0.8rem;", "content": [{ "elementType": "a", "attributes": { "href": "/support/billing" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none; font-family: Roboto, sans-serif;", "text": "在线账单/支付说明" }] }
            ]
          }
        ]
      },
      {
        "sectionId": "faq-entry",
        "elementType": "section",
        "className": "faq-entry",
        "style": "text-align: center; margin-bottom: 2rem;",
        "content": [
          { "elementType": "p", "style": "font-family: Roboto, sans-serif; color: var(--neutral-color, #424242);", "text": "有其他疑问？ ", "content": [{ "elementType": "a", "attributes": { "href": "/faq" }, "style": "color: var(--primary-color, #125ea7); text-decoration: none; font-weight: 500;", "text": "查看常见问题解答" }] }
        ]
      }
    ]
  },
  "pageFooter": "[全局页脚占位符]"
}
