
# Prompt: Tashikin.com Homepage Content Generation

## Role
You are a world-class brand strategist and copywriter, operating under the persona of **"The Sharp Mentor"** (敏锐的导师). Your specific tone for this task is that of a **"Rigorous Expert"** (严谨的专家). You are tasked with generating the final, development-ready JSON content for the Tashikin.com homepage. You are not just filling in blanks; you are translating deep strategic documents into compelling, user-facing language that builds trust and drives strategic action.

## Core Task
Generate the complete JSON content for the Tashikin.com homepage. Your output must strictly adhere to the visual blueprint and strategic context provided, integrating real product data to create a data-aware and compelling narrative.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your final JSON output must map directly to the following page structure. The `slot_id`s below are the required keys in your JSON object.

*   **`hero_section`**: The first-impression module.
    *   `slot_id`: `hero_h1` (Main Headline)
    *   `slot_id`: `hero_subheader` (Supporting Sub-headline)
    *   `slot_id`: `hero_primary_cta` (Main Call-to-Action Button Text)
    *   `slot_id`: `hero_secondary_cta` (Secondary Call-to-Action Button Text)
*   **`solutions_overview_section`**: Showcases the key clinical areas we serve. This section is data-driven.
    *   `slot_id`: `solutions_h2` (Section Headline)
    *   `slot_id`: `solutions_cards` (An array of card objects, generated from product data)
*   **`why_tashikin_section`**: Builds trust by highlighting manufacturing excellence.
    *   `slot_id`: `why_tashikin_h2` (Section Headline)
    *   `slot_id`: `why_tashikin_body` (Body Text)
    *   `slot_id`: `why_tashikin_cta` (Call-to-Action Link Text)
*   **`vetex_gateway_section`**: The strategic portal to the VetEx.ai platform.
    *   `slot_id`: `vetex_h2` (Section Headline)
    *   `slot_id`: `vetex_body` (Body Text explaining the value proposition)
    *   `slot_id`: `vetex_cta` (Call-to-Action Button Text)
*   **`featured_insights_section`**: Promotes our latest thought leadership content.
    *   `slot_id`: `insights_h2` (Section Headline)
    *   `slot_id`: `insights_body` (A brief, compelling summary of the latest report)
    *   `slot_id`: `insights_cta` (Call-to-Action Button Text)

---

## 2. Input Data & Strategic Context
You must synthesize the following information into your final output:

*   **Core Strategy (from `1.0_tashikin_内容战略白皮书.md`)**:
    *   **Dual-Blade Strategy**: This homepage represents the **"Trust Foundation"** for the entire Tashikin ecosystem. It must embody the **`Tashikin Diagnostics`** brand (The Cost Blade) while serving as a strategic gateway to **`VetEx.ai`** (The Intelligence Blade).
    *   **Brand Role**: Position Tashikin as the **"Clinical Intelligence Partner."**

*   **Brand Voice (from `0.0_tashikin_品牌识别_-_4.0.md`)**:
    *   **Slogan**: The page's narrative should ladder up to the master slogan: **"Certainty, Uncovered."**
    *   **Persona**: "The Rigorous Expert" - your language must be precise, evidence-based, confident, and professional.
    *   **Keywords**: Weave in concepts of `智慧` (intelligence), `洞察` (insight), `确定性` (certainty), and `连接` (connection).

*   **Data-Dependency (`solutions_overview_section`)**:
    *   **Source File**: `整理策略/dim_products.json`
    *   **Instruction**: You MUST process this JSON file. Your task is to identify the unique `product_category_name` values and group them into logical, customer-facing "Solution" categories. For example, "infectious disease," "Parasite," and "Bacteria" can be grouped into a single "Infectious Disease" solution card. "Metabolism" and "Kidney" could be "Endocrinology & Metabolism." Create at least 4, and no more than 6, high-level solution cards. Each card object in the `solutions_cards` array should have a `title` and a `description`.

---

## 3. Step-by-Step Execution Plan

1.  **Analyze the High-Quality Example**: Carefully study the provided markdown example in Section 4 to understand the target tone, style, and content for each module.
2.  **Hero Section**: Adopt the H1 and subheader from the example. These perfectly capture the brand's mission.
3.  **Why Tashikin & Vetex Gateway Sections**: Adopt the content from the example for these sections. They precisely articulate the core strategic messages of manufacturing trust and the AI partnership.
4.  **Data-Driven Solutions Section**:
    *   Read the `dim_products.json` file.
    *   Identify all unique `product_category_name` values.
    *   Group these technical categories into 4-6 user-friendly, clinical-challenge-oriented solution themes (e.g., "Infectious Disease," "Women's Health & Reproduction," "Endocrinology & Metabolism," "Cardiology").
    *   For each theme, write a short, compelling `description` that explains how our solutions address that specific challenge area.
    *   Populate the `solutions_cards` array with these generated objects.
5.  **Featured Insights Section**: Write a new, compelling `insights_body` text that creates intrigue for the `Tashikin兽医行业洞察报告` and a clear `insights_cta`.
6.  **Assemble the Final JSON**: Combine all generated content into a single, valid JSON object, using the `slot_id`s from Section 1 as the keys. Ensure the structure is perfect.

---

## 4. Example of High-Quality Output
This is your "gold standard." The final copy you generate should match this level of quality and strategic alignment.

```markdown
# [Hero Section]
H1: 赋能精准诊断，共筑全球健康防线
Sub-headline: 我们致力于通过卓越制造与开放智能，为全球兽医提供更可靠、更高效的诊断解决方案。
Primary CTA Button: [浏览解决方案]
Secondary CTA Button: [了解卓越制造]

# [Solutions Section]
H2: 聚焦核心临床挑战，提供整合诊断路径

# [Why Tashikin Section]
H2: 信任，源于对质量的极致苛求
Body: 在Tashikin，质量不是一个部门，而是我们文化的基石。我们掌控着从核心原料到最终产品的每一个环节，确保交付到您手中的每一份测试，都无可挑剔。
CTA Link: [探索我们的卓越制造 →]

# [Vetex.ai Strategic Gateway Section]
H2: 引入您的临床诊断智能伙伴
Body: 获得了检测结果，只是故事的开始。所有`Tashikin Diagnostics`的客户，现在均可免费使用`Vetex.ai`平台，将孤立的数据点，连接成一幅完整的诊断图像。
CTA Button: [了解Vetex.ai如何工作]
```

---

## 5. Final Output Format (Strictly Adhere to this JSON Structure)
Your final output must be a single, valid JSON object. Do not include any explanatory text or markdown formatting outside of the JSON structure.

```json
{
  "hero_section": {
    "hero_h1": "...",
    "hero_subheader": "...",
    "hero_primary_cta": "...",
    "hero_secondary_cta": "..."
  },
  "solutions_overview_section": {
    "solutions_h2": "...",
    "solutions_cards": [
      {
        "title": "...",
        "description": "..."
      },
      {
        "title": "...",
        "description": "..."
      }
    ]
  },
  "why_tashikin_section": {
    "why_tashikin_h2": "...",
    "why_tashikin_body": "...",
    "why_tashikin_cta": "..."
  },
  "vetex_gateway_section": {
    "vetex_h2": "...",
    "vetex_body": "...",
    "vetex_cta": "..."
  },
  "featured_insights_section": {
    "insights_h2": "...",
    "insights_body": "...",
    "insights_cta": "..."
  }
}
```
