# 品牌样式设计表 Report Guidance Style
**报告日期** 20250301
**报告人** 竞品网站分析AI

| 参数类别 | 参数名称 | 参数值 | 参数描述/应用场景 | 示例 CSS 代码 |
| --- | --- | --- | --- | --- |
| **颜色** | 主色 | #036AE0 | 品牌主色，用于 Banner 背景、Primary 按钮等 | `--primary-color: #036AE0;` |
|      | 辅助色 | #9CDCFF | 品牌辅助色，用于点缀、辅助背景等 | `--card-bg-alt: #9CDCFF;` |
|      | 强调色-成功 | #59B730 | 品牌强调色，用于成功、积极的提示 | `--success-color: #59B730;` |
|      | 强调色-错误 | #F02D37 | 品牌强调色，用于错误、危险的警示 | `--danger-color: #F02D37;` |
|      | 中性色-深灰 | #31353D | 主要文本颜色、深灰色背景 | `--text-color: #31353D;` |
|      | 中性色-浅灰 | #F0F0F0 | 浅灰色背景，用于 Section 背景、卡片背景等 | `--card-bg: #F0F0F0;` |
|      | 链接颜色 | #036AE0 | 默认链接颜色                               | `--link-color: #036AE0;` |
|      | 标题颜色 | #036AE0 | 默认标题颜色                               | `--heading-color: #036AE0;` |
|      | 按钮边框颜色 | #036AE0 | 默认按钮边框颜色                           | `--button-border-color: #036AE0;` |
|      | 边框颜色     | rgba(0, 0, 0, .2) | 默认边框颜色                             | `--border-color: rgba(0, 0, 0, .2);` |
| **字体** | 标题字体     | Sora, sans-serif | 用于 H1-H6 标题                           | `font-family: Sora, sans-serif;` |
|      | 正文字体     | Roboto, sans-serif | 用于段落、列表等正文内容                    | `font-family: Roboto, sans-serif;` |
|      | 字号-H1    | 42px              | H1 标题字号                              | `font-size: 42px;`                |
|      | 字号-H2    | 34px              | H2 标题字号                              | `font-size: 34px;`                |
|      | 字号-H3    | 26px              | H3 标题字号                              | `font-size: 26px;`                |
|      | 字号-H4    | 18px              | H4 标题字号                              | `font-size: 18px;`                |
|      | 字号-H5    | 18px              | H5 标题字号                              | `font-size: 18px;`                |
|      | 字号-H6    | 15px              | H6 标题字号                              | `font-size: 15px;`                |
|      | 字号-正文   | 15px              | 默认正文字号                             | `font-size: 15px;`                |
|      | 字重-标题   | 600               | 标题默认字重                             | `font-weight: 600;`               |
|      | 行高-标题   | 1.2               | 标题默认行高                             | `line-height: 1.2;`               |
|      | 行高-正文   | 1.6               | 正文默认行高                             | `line-height: 1.6;`               |
| **间距** | 常用 Margin  | 24px, 30px, 48px 等 | Section 垂直间距、模块间距等             | `margin-bottom: 24px;`             |
|      | 常用 Padding | 15px, 20px, 30px 等 | Section 内部 padding、组件内边距等       | `padding: 15px;`                  |
|      | Gutter 宽度 | 15px              | 栅格系统默认列间距                         | `padding-left: 15px;`              |
|      | 行间距     | 24px              | 列表、段落等行间距                         | `line-height: 24px;`               |
| **UI 元素样式** | 按钮圆角     | 100px             | 按钮默认圆角，圆形按钮                       | `border-radius: 100px;`           |
|      | 按钮 Padding | 6px 14px          | 默认按钮内边距                           | `padding: 6px 14px;`               |
|      | 按钮边框     | 1px solid #036AE0 | Default 按钮边框样式                     | `border: 1px solid #036AE0;`       |
|      | 按钮阴影     | rgba(0, 0, 0, .2)  | 按钮默认阴影                             | `box-shadow: 0 1px 1px #00000020;` |
|      | 表单圆角     | 4px               | 表单元素默认圆角                         | `border-radius: 4px;`              |
|      | 表单边框     | 1px solid #babdbf | 表单元素默认边框                         | `border: 1px solid #babdbf;`       |
|      | 卡片圆角     | 0px               | Panel 卡片默认圆角                        | `border-radius: 0;`                |
|      | 卡片边框     | 1px solid transparent | Panel 卡片默认边框                         | `border: 1px solid transparent;`   |
|      | 阴影         | rgba(0, 0, 0, .2)  | 默认阴影颜色                             | `box-shadow: 0 1px 1px #00000020;` |
| **主题** | 深色主题     | `.theme-dark`      | 深色主题，用于页脚或特殊模块                   | `.theme-dark { ... }`              |
|      | 品牌强调色主题 | `.theme-brand-primary` | 品牌强调色主题，突出品牌形象                   | `.theme-brand-primary { ... }`     |
|      | 白色主题     | `.theme-white`      | 白色主题，用于内容展示区域                   | `.theme-white { ... }`              |
| **其他视觉元素** | 分割线颜色   | #F0F0F0            | `<hr>` 分割线颜色                          | `border-top-color: #F0F0F0;`      |
|      | 动画时长     | 0.2s, 0.3s        | 页面过渡、UI 动效常用时长                  | `transition-duration: 0.2s;`       |
|      | 动画 easing  | ease-in-out, linear | 常用动画 easing 曲线                       | `transition-timing-function: ease-in-out;` |
