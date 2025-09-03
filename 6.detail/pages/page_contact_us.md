{
    "page_slug": "contact-us",
    "page_url": "/contact-us",
  "page_type": "contact_us",
  "page": {
    "url": "/contact-us",
    "title": "联系我们 | reOpenTest - 全球领先的体外诊断解决方案提供商",
    "meta": {
      "description": "联系 reOpenTest 获取产品信息、寻求合作或技术支持。我们提供多种联系方式，包括在线表单、电话和邮件。",
      "keywords": [
        "联系 reOpenTest",
        "reOpenTest 联系方式",
        "IVD 供应商联系",
        "诊断试剂合作",
        "reOpenTest 支持",
        "体外诊断",
        "快速检测"
      ]
    },
    "content": {
      "sections": [
        {
          "type": "page_header",
          "id": "contact-header",
          "headline": "联系我们",
          "subheadline": "Test for Every Need. 我们致力于提供快速、可靠的 IVD 解决方案。期待您的垂询，请选择最适合您的方式与我们联系。"
        },
        {
          "type": "contact_form_section",
          "id": "contact-form",
          "headline": "在线留言",
          "body": "请填写以下表单，我们的专业团队将尽快与您联系。",
          "form": {
            "fields": [
              { "name": "name", "label": "您的姓名", "type": "text", "required": true, "placeholder": "请输入您的姓名" },
              { "name": "email", "label": "您的邮箱", "type": "email", "required": true, "placeholder": "请输入您的电子邮箱地址" },
              { "name": "phone", "label": "联系电话", "type": "tel", "required": false, "placeholder": "请输入您的电话号码 (可选)" },
              { "name": "company", "label": "公司/机构名称", "type": "text", "required": false, "placeholder": "请输入您的公司或机构名称 (可选)" },
              { "name": "country", "label": "国家/地区", "type": "text", "required": false, "placeholder": "请输入您所在的国家或地区 (可选)" },
              { "name": "inquiry_type", "label": "咨询类型", "type": "select", "required": true, "options": [
                  {"value": "", "text": "请选择咨询类型"},
                  {"value": "general", "text": "一般咨询"},
                  {"value": "sales", "text": "产品销售/报价"},
                  {"value": "support", "text": "技术支持/售后服务"},
                  {"value": "partnership", "text": "经销商/合作"},
                  {"value": "order", "text": "订单查询"}
                ]
              },
              { "name": "message", "label": "您的留言", "type": "textarea", "required": true, "placeholder": "请在此处输入您的具体问题或需求..." }
            ],
            "submit_button_text": "提交信息"
          }
        },
        {
          "type": "contact_info_block",
          "id": "contact-details",
          "headline": "联系方式",
          "contact_details": [
             { "type": "header", "text": "中国总部 (China HQ):"},
             { "type": "contact_person", "icon": "user", "text": "业务咨询 (Oversea Contact): Cindy Wang" },
             { "type": "email", "icon": "envelope", "text": "邮箱 (Email): info@reopentest.com", "link": "mailto:info@reopentest.com" },
             { "type": "phone", "icon": "phone-alt", "text": "电话/WhatsApp (Tel/WhatsApp): +86-0571-87763175", "link": "tel:+86-0571-87763175" },
             { "type": "fax", "icon": "fax", "text": "传真 (Fax): +86-0571-87763175" },
             { "type": "working_hours", "icon": "clock", "text": "工作时间: 周一至周五, 北京时间 09:00-17:00" },
             { "type": "address", "icon": "map-marker-alt", "text": "办公室地址: 中国浙江省杭州市滨江区月明路560号正泰大厦A座201室 (邮编: 310052)" },
             { "type": "address", "icon": "industry", "text": "工厂地址: 中国浙江省湖州市安吉县递铺街道塘浦工业园文蕴路489号3号厂房2楼" }
          ]
        },
        {
          "type": "map_section",
          "id": "location-map",
          "headline": "我们的位置 (杭州办公室)",
          "map": {
            "latitude": "30.1897", // Approximate Latitude for Yueming Road 560
            "longitude": "120.1945",
            "zoom_level": 14,
            "marker_title": "reOpenTest 杭州办公室",
            "google_maps_embed_url": "https://maps.google.com/maps?q=yue%20ming%20road%20No.560%2C%20hangzhou%2C%20china&t=&z=14&ie=UTF8&iwloc=&output=embed"
          }
        }
      ]
    },
    "assets": {
      "images": [],
      "icons": ["user", "envelope", "phone-alt", "fax", "clock", "map-marker-alt", "industry"]
    },
    "styles": {
      "css": ".contact_form_section, .contact_info_block, .map_section { margin-bottom: 2rem; } \n.contact_form_section form { display: grid; gap: 1rem; } \n.contact_form_section label { display: block; margin-bottom: 0.25rem; font-weight: 600; } \n.contact_form_section input[type='text'], \n.contact_form_section input[type='email'], \n.contact_form_section input[type='tel'], \n.contact_form_section select, \n.contact_form_section textarea { width: 100%; padding: 0.75rem; border: 1px solid #ccc; border-radius: 4px; font-family: 'Roboto', sans-serif; } \n.contact_form_section textarea { min-height: 150px; } \n.contact_info_block .contact_details { list-style: none; padding: 0; } \n.contact_info_block .contact_details li { display: flex; align-items: center; gap: 0.75rem; margin-bottom: 0.75rem; } \n.contact_info_block .contact_details .icon { width: 20px; text-align: center; color: #125ea7; } \n.contact_info_block .contact_details .header { font-weight: 600; margin-top: 1rem; margin-bottom: 0.5rem; list-style: none; font-family: 'Sora', sans-serif; } \n.map_section iframe { border: 0; border-radius: 8px; width: 100%; height: 400px; }"
    }
  }
}
