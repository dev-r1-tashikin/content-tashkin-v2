### **Prompt: Tashikin 品牌初始站点生成指令 (Project "Cornerstone")**

**致：** Firebase (高级Web开发专家)

**发件人：** Tashikin 战略委员会

**主题：** **项目 "Cornerstone" - 构建 Tashikin V4.0 品牌官方网站基石**

**指令版本：** 1.0

**核心任务：**

您的任务是根据本指令，**完整地、精确地**构建 `Tashikin` 品牌官方网站的初始版本。最终产出物是一个名为 `_site/` 的目录，其中包含所有根据 V4.0 战略设计的核心页面HTML文件。

**您必须遵循的两个核心战略蓝图：**

1.  **《Tashikin 品牌识别核心指南 V4.0》:** 这是品牌的灵魂。所有视觉设计（颜色、字体）、文案基调和品牌哲学都必须严格遵守此指南。
2.  **《sitemap.xml V2.0 - 战略聚焦版》:** 这是网站的骨架。您必须根据此文件定义的页面层级和URL结构来创建对应的目录和`index.html`文件。

---

### **第一部分：技术与环境规格 (The "How")**

1.  **前端框架：** **禁止**使用任何重量级JS框架 (如 React, Vue)。本项目是纯粹的、基于 **Tailwind CSS** 的静态站点。
2.  **CSS 实现：** 必须通过 **Tailwind CSS 的 CDN 模式** 实现。将以下代码添加到每个 HTML 文件的 `<head>` 中：
    ```html
    <script src="https://cdn.tailwindcss.com"></script>
    ```
3.  **字体引入：** 必须通过 **Google Fonts CDN** 引入 `Montserrat` (用于标题) 和 `Lato` (用于正文)。将以下代码添加到每个 HTML 文件的 `<head>` 中：
    ```html
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@400;700&family=Montserrat:wght@700;900&display=swap" rel="stylesheet">
    ```
4.  **自定义配置 (Tailwind)：** 在 `<head>` 的 `<style type="text/tailwindcss">` 标签中配置字体和颜色，以确保全局一致性：
    ```html
    @layer base {
      html {
        font-family: 'Lato', sans-serif;
      }
      h1, h2, h3, h4, h5 {
        font-family: 'Montserrat', sans-serif;
      }
    }
    ```
5.  **颜色变量：**
    *   **主色 (可靠蓝):** `#005A9C`
    *   **文本 (深岩灰):** `#1F2937`
    *   **辅助文本 (中岩灰):** `#6B7280`
    *   **背景 (浅岩灰):** `#F3F4F6`

---

### **第二部分：页面生成指令 (The "What")**

您需要根据 `sitemap.xml` 创建以下目录结构和文件。以下是每个核心页面的内容和结构指令：

#### **1. `_site/index.html` (首页)**

*   **目标：** 成为品牌的“第一印象”，传递 `Certainty, Uncovered.` 的核心承诺。
*   **内容结构：**
    1.  **导航栏：** 包含 logo (暂用 "Tashikin" 文字代替) 和指向“解决方案”、“产品”、“核心技术”、“关于我们”和“联系我们”的链接。
    2.  **Hero 区域：**
        *   **背景：** 使用深色调 (如 `深岩灰`) 或高质量的抽象医学/科技图片占位符。
        *   **主标题 (H1):** `Certainty, Uncovered.` (使用 `Montserrat` 字体，大字号，白色)。
        *   **副标题：** “我们通过革命性的诊断工具与智能洞察，揭示病例背后的确定性，赋能全球兽医。”
        *   **行动号召 (CTA):** 两个并排的按钮：
            *   `了解我们的解决方案` (主色背景) -> 指向 `/solutions/`
            *   `探索我们的产品` (描边样式) -> 指向 `/products/`
    3.  **双尖刀战略介绍区：**
        *   **标题 (H2):** “一个使命，两把尖刀”
        *   **左侧卡片 (`Tashikin Diagnostics`):**
            *   标题: `成本尖刀：Tashikin Diagnostics`
            *   描述: “提供无与伦比的可靠性与性价比，赢得兽医的广泛信赖。”
            *   链接: `探索诊断产品 >` -> 指向 `/products/diagnostics/`
        *   **右侧卡片 (`VetEx`):**
            *   标题: `智能尖刀：VetEx AI 平台`
            *   描述: “以革命性的智能与洞察，连接数据点，定义诊断的未来。”
            *   链接: `了解 VetEx >` -> 指向 `/products/vetex-ai-platform/`
    4.  **技术背书区 (`NomoFlow™`):**
        *   一个横跨整个页面的区域，背景色使用 `浅岩灰`。
        *   **居中内容:** `所有 Tashikin 产品均由我们行业领先的 NomoFlow™ 制造工艺平台强力驱动，确保卓越品质。` (logo 暂用 "NomoFlow™" 文字代替)。
        *   **链接:** `了解我们的核心技术 >` -> 指向 `/technology/nomoflow/`
    5.  **页脚：** 包含版权信息、隐私政策、服务条款链接。

#### **2. `_site/about-us/index.html` (关于我们)**

*   **目标：** 讲述品牌故事，建立信任。
*   **内容结构：**
    1.  **页面标题 (H1):** “开辟智慧与洞察的第三战场”
    2.  **品牌故事：** (使用占位符文本) 详细阐述 Tashikin 如何在“系统与确定性”(IDEXX) 和“关怀与连接”(Zoetis) 之外，选择成为连接兽医“确定性大脑”与“关怀心脏”的“智能神经网络”。
    3.  **我们的使命 (H2):**
        *   描述: “我们不只是提供数据，我们帮助兽医连接所有线索，亲手揭示确定性。”
    4.  **集团背书 (H2):**
        *   标题: “源自 Tarinn Inc. 的创新血脉”
        *   描述: “作为 `Tarinn Inc.` 集团的一员，Tashikin 共享全球领先的研发与制造能力。” (logo 暂用 "Tarinn Inc." 文字代替)。
    5.  **页脚**

#### **3. `_site/products/index.html` (产品中心)**

*   **目标：** 作为产品世界的入口。
*   **内容结构：**
    1.  **页面标题 (H1):** “为每一种挑战而设计”
    2.  **内容与 `/index.html` 的“双尖刀战略介绍区”类似**，但提供更详细的描述。创建两个视觉上突出的大型链接卡片，分别指向 `Tashikin Diagnostics` 和 `VetEx AI Platform`。

#### **4. `_site/products/diagnostics/index.html` (诊断产品线)**

*   **目标：** 展示 `Tashikin Diagnostics` 的产品组合。
*   **内容结构：**
    1.  **页面标题 (H1):** “Tashikin Diagnostics: 可靠、精确、高效”
    2.  **副标题:** “按物种浏览我们的快速检测试剂”
    3.  **物种分类导航:**
        *   两个大型卡片/按钮: `犬类 (Canine)` 和 `猫科 (Feline)`。
        *   每个卡片链接到对应的页面 (当前先创建占位符页面 `_site/products/diagnostics/canine/index.html` 和 `feline/index.html`)。

#### **5. `_site/technology/nomoflow/index.html` (核心技术)**

*   **目标：** 建立对 `NomoFlow™` 平台的技术信任。
*   **内容结构：**
    1.  **页面标题 (H1):** `NomoFlow™: 我们卓越品质的基石`
    2.  **技术阐述：** (使用占位符文本) 详细解释 NomoFlow™ 如何确保产品批间差的稳定性、结果的可靠性，以及它作为 `Tarinn Inc.` 集团共享技术引擎的地位。
    3.  **优势列表 (H2):**
        *   **一致性:** “确保每一批次都拥有同样的卓越性能。”
        *   **可靠性:** “最大程度减少误差，提供您可信赖的结果。”
        *   **效率:** “优化的生产流程带来更高的性价比。”

#### **6. 其他页面**

*   为 `sitemap.xml` 中提到的所有其他URL（如 `/contact-us/`, `/solutions/`, `/privacy-policy/` 等）创建对应的目录和 `index.html` 文件。
*   这些页面目前只需要包含一个带有正确页面标题 (H1) 的基本布局，以表明页面已创建。例如，`_site/contact-us/index.html` 的 H1 应为“联系我们”。

---

**交付成果：**

一个完整的 `_site/` 目录，其内部文件结构严格匹配 `sitemap.xml V2.0` 的定义。所有 HTML 文件都使用 Tailwind CSS CDN 构建，并忠实反映 V4.0 品牌指南的视觉和内容策略。

**立即开始执行。**
