
# Prompt: Canine Infectious Diseases Solution Page Content Generation (V2)

## Role
You are a veterinary marketing specialist with deep knowledge in canine infectious diseases. Your persona is the **"Sharp Mentor"** and your tone is the **"Rigorous Expert"**. You are building a page that establishes Tashikin as the definitive partner for diagnosing and managing these critical cases.

## Core Task
Generate the complete, development-ready JSON content for the **Canine Infectious Diseases Solution page**. The page must serve as a hub for veterinarians, connecting clinical challenges with Tashikin's specific diagnostic solutions.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A powerful headline focused on diagnostic confidence.
*   **Section 2: Clinical Challenges** (`type: 'feature_list'`): Outlines common diagnostic challenges for this category.
*   **Section 3: Recommended Products** (`type: 'product_grid'`): Showcases the specific Tashikin products relevant to this solution.
*   **Section 4: Related Resources** (`type: 'related_content_grid'`): Links to relevant case studies or articles.
*   **Section 5: CTA** (`type: 'cta_banner'`): A clear call to action to explore the products.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page supports the "Trust Foundation" by demonstrating our deep understanding of a specific clinical area. It funnels users from a clinical problem towards our specific product solutions.
*   **Data-Dependency**: The executing AI must reference `整理策略/dim_products.json` to identify and select the products that are specifically categorized under **"Canine Infectious Disease"**.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `canine-infectious-diseases`
    *   **`page_url`**: `/solutions/canine-infectious-diseases`
    *   **`product_center_url`**: `/products`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a `headline` that speaks to the challenge of diagnosing complex canine infectious diseases.
3.  **Define Clinical Challenges**: In the `feature_list` section, create 3-4 `items` describing common issues vets face (e.g., "Co-infections and Overlapping Symptoms", "Need for Rapid In-Clinic Results", "Client Communication on Vector-Borne Diseases").
4.  **Select Relevant Products**: 
    *   **Scan `dim_products.json`**: Programmatically search the `rows` in the product data file.
    *   **Filter**: Select all product objects where `product_category_name` is equal to `"Canine Infectious Disease"`.
    *   **Populate**: For each selected product, create an item in the `product_grid` section, including its `website_display_name` and a generated URL to its future product detail page.
5.  **Link to Resources**: In the `related_content_grid`, create a placeholder link to a relevant case study, for example, the case study on the "fever of unknown origin."
6.  **Create CTA**: Write a clear CTA that encourages users to explore the full product portfolio.
7.  **Assemble and Validate**: Ensure the final JSON is valid and all links are correct.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "canine-infectious-diseases",
  "page_url": "/solutions/canine-infectious-diseases",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "sol-cid-hero",
        "headline": "Navigating the Complexity of Canine Infectious Diseases",
        "subheader": "Confident diagnoses for challenging cases, from vector-borne diseases to common viruses."
      },
      {
        "type": "feature_list",
        "id": "sol-cid-challenges",
        "headline": "Common Diagnostic Hurdles",
        "items": [
          { "title": "Overlapping Symptoms", "description": "Differentiating between diseases like Lyme, Anaplasma, and Ehrlichia can be challenging based on clinical signs alone." },
          { "title": "The Need for Speed", "description": "When dealing with highly contagious viruses like Parvovirus, rapid point-of-care results are critical for patient isolation and treatment.
          },
          { "title": "Client Education", "description": "Clearly explaining the risks and realities of vector-borne and infectious diseases is key to owner compliance and prevention."
          }
        ]
      },
      {
        "type": "product_grid",
        "id": "sol-cid-products",
        "headline": "Our Recommended Diagnostic Panel",
        "items": [
          {
            "product_name": "Canine Heartworm, Lyme, Anaplasma, Ehrlichia Combo Test",
            "url": "/products/canine/hw-lyme-ana-ehr",
            "image_url": "/assets/images/products/thumb-canine-combo.jpg"
          },
          {
            "product_name": "Canine Parvovirus Ag Test",
            "url": "/products/canine/cpv-ag",
            "image_url": "/assets/images/products/thumb-cpv.jpg"
          }
        ]
      },
      {
        "type": "related_content_grid",
        "id": "sol-cid-related",
        "headline": "Related Insights",
        "items": [
          {
            "title": "Case Study: Fever of Unknown Origin",
            "url": "/resources/case-studies/feline-fever-unknown-origin",
            "image_url": "/assets/images/resources/thumb-case-fever.jpg"
          }
        ]
      },
      {
        "type": "cta_banner",
        "id": "sol-cid-cta",
        "headline": "Explore Our Full Portfolio",
        "primary_cta": {
          "text": "Go to Product Center",
          "url": "/products"
        }
      }
    ]
  }
}
```
