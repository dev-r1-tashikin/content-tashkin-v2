
# Prompt: Cardiology Solution Page Content Generation (V2)

## Role
You are a veterinary marketing specialist with a deep understanding of cardiology. Your persona is the **"Sharp Mentor"** and your tone is the **"Rigorous Expert"**. You are building a page to position Tashikin as a key partner in diagnosing and managing cardiac cases.

## Core Task
Generate the complete, development-ready JSON content for the **Cardiology Solution page**. This page will serve as a hub for veterinarians, connecting the challenges of cardiac diagnosis with Tashikin's specific solutions.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A headline focused on achieving diagnostic clarity in cardiology.
*   **Section 2: Clinical Challenges** (`type: 'feature_list'`): Outlines common diagnostic challenges in veterinary cardiology.
*   **Section 3: Recommended Products** (`type: 'product_grid'`): Showcases specific Tashikin products for cardiac assessment.
*   **Section 4: Related Resources** (`type: 'related_content_grid'`): Links to relevant case studies or articles.
*   **Section 5: CTA** (`type: 'cta_banner'`): A clear call to action.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page demonstrates our expertise in a complex and critical specialty. It must emphasize key selling points like **speed (15-minute results)** and **reliability (certified performance)** as noted in the wireframes.
*   **Data-Dependency**: The executing AI must reference `整理策略/dim_products.json` to identify and select products categorized under **"Cardiology"**.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `cardiology`
    *   **`page_url`**: `/solutions/cardiology`
    *   **`product_center_url`**: `/products`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a `headline` that speaks to the critical nature of cardiac diagnostics.
3.  **Define Clinical Challenges**: In the `feature_list` section, create 3-4 `items` describing common issues (e.g., "Differentiating Cardiac from Respiratory Disease", "Screening At-Risk Breeds", "Monitoring Chronic Heart Conditions").
4.  **Select Relevant Products**: 
    *   **Scan `dim_products.json`**: Search the `rows` in the product data file.
    *   **Filter**: Select all product objects where `product_category_name` is `"Cardiology"`.
    *   **Populate**: For each selected product, create an item in the `product_grid` section. Emphasize speed and reliability in the descriptions.
5.  **Link to Resources**: Create a placeholder link to a relevant resource.
6.  **Create CTA**: Write a CTA encouraging users to explore the products.
7.  **Assemble and Validate**: Ensure the final JSON is valid.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "cardiology",
  "page_url": "/solutions/cardiology",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "sol-card-hero",
        "headline": "Clarity and Confidence in Every Heartbeat",
        "subheader": "Rapid, reliable cardiac biomarkers to help you diagnose and manage with precision."
      },
      {
        "type": "feature_list",
        "id": "sol-card-challenges",
        "headline": "Key Challenges in Cardiac Cases",
        "items": [
          { "title": "Cardiac or Respiratory?", "description": "Use objective biomarker data to quickly assess the likelihood of cardiac disease in animals presenting with respiratory signs." },
          { "title": "Screening At-Risk Patients", "description": "Establish baselines and screen asymptomatic, at-risk breeds with a quick, reliable in-clinic test."
          },
          { "title": "Staging and Monitoring", "description": "Quantify cardiac stretch and damage to help stage and monitor patients with chronic valvular disease or cardiomyopathy."
          }
        ]
      },
      {
        "type": "product_grid",
        "id": "sol-card-products",
        "headline": "Our Cardiology Panel",
        "items": [
          {
            "product_name": "Canine NT-proBNP Test",
            "url": "/products/canine/nt-probnp",
            "image_url": "/assets/images/products/thumb-probnp.jpg",
            "description": "Get a quantitative assessment of cardiac stretch in just 15 minutes."
          }
        ]
      },
      {
        "type": "related_content_grid",
        "id": "sol-card-related",
        "headline": "Related Insights",
        "items": []
      },
      {
        "type": "cta_banner",
        "id": "sol-card-cta",
        "headline": "Explore Our Cardiology Solutions",
        "primary_cta": {
          "text": "Go to Product Center",
          "url": "/products"
        }
      }
    ]
  }
}
```
