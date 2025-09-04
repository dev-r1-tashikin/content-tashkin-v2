
# Prompt: Partners Page Content Generation (V2 - Link-Aware)

## Role
You are a B2B Marketing and Channel Partnerships Director, operating under the persona of a **"Sharp Mentor"**. Your tone is direct, business-oriented, and focused on mutual growth, embodying the **"Rigorous Expert"** persona. You are speaking directly to potential distributors and strategic partners.

## Core Task
Generate the complete, development-ready JSON content for the "Partners" page. The page must clearly articulate the value proposition of becoming a Tashikin distributor, emphasizing not just our products, but the entire ecosystem we offer to ensure our partners' success.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object containing a `page` object. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A direct invitation to potential partners.
    *   `headline`, `subheader`
*   **Section 2: Value Proposition** (`type: 'feature_list'`): Outlines the key benefits of partnership.
    *   `headline`, `items` (an array of feature objects)
*   **Section 3: The Tashikin Advantage** (`type: 'text_with_image'`): Explains our unique "Dual-Blade" strategic advantage.
    *   `headline`, `body_text`, `image_url`
*   **Section 4: Partner Inquiry Form** (`type: 'form_module'`): A clear call to action and lead capture mechanism.
    *   `headline`, `form_fields`, `submit_button`

---

## 2. Input Data & Strategic Context
The executing AI must synthesize the following:

*   **Core Strategy (from `1.0_tashikin_内容战略白皮书.md`)**:
    *   **Cost Blade Focus**: This page is a critical tool for the "Cost Blade" (`Tashikin Diagnostics`) to build its distribution network.
    *   **Ecosystem Sell**: A key differentiator is that we don't just offer products; we offer a partnership ecosystem. This includes the pull-through demand created by `VetEx.ai` and the marketing support from our content engine.

*   **Brand Voice (from `0.0_tashikin_品牌识别_-_4.0.md`)**:
    *   The language should be professional and focused on business outcomes: growth, market differentiation, and customer retention.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `partners`
    *   **`page_url`**: `/partners`
    *   **`form_submission_endpoint`**: `/api/partner-inquiry` (for the form action)

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with `page_slug`, `page_url`, and the `content.sections` array.
2.  **Craft Hero Content**: Write a compelling `headline` and `subheader` that speaks directly to a potential distributor's goals (e.g., "Grow Your Business with a Next-Generation Partner").
3.  **Define the Value Proposition**: In the `feature_list` section, create 3-4 `items`. Each item should be a core benefit of partnering with Tashikin. Focus on:
    *   **Disruptive Product Portfolio**: High-quality, high-value products (`Tashikin Diagnostics`).
    *   **Built-in Demand Engine**: The pull-through effect of the free `VetEx.ai` platform.
    *   **World-Class Marketing Support**: Access to our content and educational resources.
    *   **Supply Chain Reliability**: The promise of our `NomoFlow™` powered manufacturing.
4.  **Explain the Advantage**: In the `text_with_image` section, write a concise `body_text` that explains our "Dual-Blade" strategy from a partner's perspective. It's not just a test, it's a system that locks in customer loyalty, benefiting the distributor long-term.
5.  **Build the Form**: In the `form_module` section, define the necessary `form_fields` (e.g., Company Name, Contact Name, Email, Country, Message) and a clear `submit_button` text.
6.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object that strictly adheres to the schema in Section 5.

---

## 4. Example of High-Quality Output (For Content Tone)

**Value Prop Item Title:** "A Portfolio That Sells Itself"
**Value Prop Item Description:** "Offer your customers our `Tashikin Diagnostics` portfolio: high-performance rapid tests at a price point that disrupts the market. Our quality, powered by `NomoFlow™`, speaks for itself."

**Tashikin Advantage Body Text:** "Our strategy is your advantage. We enter the market with a disruptive cost structure through `Tashikin Diagnostics`, securing you the sale. We then lock in that customer's long-term loyalty with our free, revolutionary `VetEx.ai` software. This ecosystem drives repeat business and protects your accounts from competitive pressure."

---

## 5. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "partners",
  "page_url": "/partners",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "pa-hero",
        "headline": "Partner with Tashikin and Redefine the Diagnostic Market",
        "subheader": "We are seeking ambitious distributors who want to offer more than just a product, but a complete diagnostic ecosystem designed for growth."
      },
      {
        "type": "feature_list",
        "id": "pa-value-prop",
        "headline": "The Benefits of Partnership",
        "items": [
          {
            "icon": "icon-portfolio",
            "title": "A Disruptive Product Portfolio",
            "description": "Offer your customers our `Tashikin Diagnostics` portfolio: high-performance rapid tests at a price point that creates immediate value. Our quality, powered by `NomoFlow™`, speaks for itself."
          },
          {
            "icon": "icon-demand-engine",
            "title": "A Built-in Demand & Retention Engine",
            "description": "Our free `VetEx.ai` platform creates a powerful pull-through effect, locking in end-user loyalty and driving repeat purchases of `Tashikin Diagnostics` consumables through your channel."
          },
          {
            "icon": "icon-marketing-support",
            "title": "World-Class Marketing & Education",
            "description": "Leverage our powerful content engine. We provide you with cutting-edge industry reports, case studies, and educational materials to help you engage and win customers."
          }
        ]
      },
      {
        "type": "text_with_image",
        "id": "pa-advantage",
        "headline": "Our Strategy is Your Advantage",
        "body_text": "We enter the market with a disruptive cost structure through `Tashikin Diagnostics`, securing you the sale. We then lock in that customer's long-term loyalty with our free, revolutionary `VetEx.ai` software. This ecosystem drives repeat business and protects your accounts from competitive pressure.",
        "image_url": "/assets/images/dual-blade-strategy-diagram.svg"
      },
      {
        "type": "form_module",
        "id": "pa-inquiry-form",
        "headline": "Become a Partner",
        "form_fields": [
          { "name": "company_name", "label": "Company Name", "type": "text", "required": true },
          { "name": "contact_name", "label": "Contact Name", "type": "text", "required": true },
          { "name": "email", "label": "Email Address", "type": "email", "required": true },
          { "name": "country", "label": "Country", "type": "text", "required": true },
          { "name": "message", "label": "Your Message", "type": "textarea", "required": false }
        ],
        "submit_button": {
          "text": "Submit Inquiry"
        },
        "form_action_url": "/api/partner-inquiry"
      }
    ]
  }
}
```
