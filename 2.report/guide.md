品牌 HTML/CSS 模板 (基础/指导)》HTML 结构框架代码说明:

HTML 结构框架:

Header 区域: 网站顶部导航栏，代码框架请参考 c1.html 或 h1.html 文件。

Section 区域: main 元素内包含了多个不同类型的 Section 模块，总数超过 50 个，覆盖了 IVD 网站常见的页面布局和内容展示需求。

Section 模块示例: 包含了 Hero Banner, Feature Card, Image Card List, Video-Text Combination, List Info, Statistic Card, Contact Form, Full-width Image, Text-only Content, Icon Teaser, Call-to-Action, Image with Text Overlay 等多种 Section 模块示例。

内容组织形式: 每个 Section 模块都代表一种常见的内容组织形式，例如 Hero Section 用于品牌宣传，Feature Card Section 用于功能介绍，Image Card List Section 用于产品展示，Video-Text Combination Section 用于视频演示，List Info Section 用于信息列表，Statistic Card Section 用于数据统计，Contact Form Section 用于用户互动。

HTML 结构: 每个 Section 模块都使用了语义化的 HTML 结构，例如 <section>, <article>, <figure>, <h1>-<h6>, <p>, <ul>, <ol>, <a>, <img>, <video>, <form>, <button> 等 HTML 元素，并添加了相应的 CSS 类名，方便样式化和 JavaScript 操作。

动态效果、版式、尺寸比例: HTML 结构框架中，部分 Section 模块 (例如 Hero Section, Video-Text Combination Section, Image Card List Section) 已经融入了动态效果 (例如 Carousel 轮播图) 和常见的版式模式 (例如左图右文，图文混排)，并预留了可调整尺寸比例的图片容器 (例如 .feature-image-container-width, .video-masthead--fig-alt-2 等)。

备注信息: 每个 Section 模块示例，我都添加了 HTML 注释，用于说明该 Section 的名称标识 (data-section 属性) 和唯一编号 (data-sectionid 属性)，方便在 CMS 系统中进行识别和管理。

CSS 代码:

嵌入方式: CSS 代码以内嵌方式 ( <style> 标签) 嵌入到 HTML 文件的 <head> 标签中，方便您快速预览和使用模板。

品牌样式设计表参数: CSS 代码头部包含了 《品牌样式设计表》 中定义的 CSS 变量，方便您根据品牌需求快速定制网站的整体视觉风格。

全局样式、布局样式、UI 组件样式: CSS 代码包含了网站的全局样式、布局样式和常用 UI 组件的基础样式，您可以基于此模板快速构建和扩展网站的样式库。

Template 示例页面 HTML 结构框架设计原则和模式:

提炼原则:

信息层级清晰: 通过合理的 HTML 结构和 CSS 样式，清晰地划分页面信息层级，例如使用 <h1>-<h6> 区分标题层级，使用不同的 Section 模块组织不同类型的内容。

重点突出: 通过 Hero Section 突出品牌核心价值，通过 Feature Card 和 Image Card List 突出产品和服务的核心卖点，通过强调色和动效反馈突出重要操作按钮和提示信息。

留白舒适: 通过合理的 margin 和 padding 设置，保证页面和模块之间、内容元素之间的留白充足，提升网站的呼吸感和视觉舒适度。

总结模式:

Hero 区 + 多 Section 组合 (首页常用): Hero 区占据首屏，快速传递核心价值，多 Section 模块灵活组合，全面展示网站内容。

左图右文 / 右图左文: Video-Text Combination Section 和 Image Text Overlay Section 采用了经典的图文左右布局，图文并茂，信息呈现更生动直观。

卡片式设计: Feature Card Section 和 Image Card List Section 大量使用卡片式设计，信息呈现简洁直观、重点突出，卡片之间相互独立，方便用户快速浏览和筛选信息。

列表式布局: List Info Section 和导航菜单、页脚链接等使用了列表式布局，结构清晰、信息密度高、方便用户快速查找和定位。

适用场景:

Hero 区 + 多 Section 组合: 适用于网站首页、 landing page 等需要全面展示网站信息和吸引用户注意力的页面。

左图右文 / 右图左文: 适用于产品介绍、案例展示、团队介绍等需要图文结合的内容页面。

卡片式设计: 适用于功能介绍、产品列表、服务介绍、案例展示等模块化、结构化的信息展示。

列表式布局: 适用于导航菜单、信息列表、步骤流程等需要清晰呈现结构化信息的场景。

统计数据卡片: 适用于首页、关于我们页等需要突出展示重要数据的场景。