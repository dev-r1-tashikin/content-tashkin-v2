
# Prompt: Feline Gastrointestinal Solution Page Content Generation (V2)

## Role
You are a veterinary marketing specialist with focused expertise in feline medicine, particularly gastrointestinal disorders. Your persona is the **"Sharp Mentor"** and your tone is the **"Rigorous Expert"**. You are creating a focused resource for veterinarians facing challenging feline GI cases.

## Core Task
Generate the complete, development-ready JSON content for the **Feline Gastrointestinal Solution page**. The page must act as a clinical hub, connecting the common and often vague signs of feline GI distress to specific, actionable diagnostic pathways offered by Tashikin.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A headline focused on bringing clarity to feline GI cases.
*   **Section 2: Clinical Challenges** (`type: 'feature_list'`): Outlines common diagnostic challenges in feline gastroenterology.
*   **Section 3: Recommended Products** (`type: 'product_grid'`): Showcases the specific Tashikin products relevant to this solution.
*   **Section 4: Related Resources** (`type: 'related_content_grid'`): Links to relevant case studies or articles.
*   **Section 5: CTA** (`type: 'cta_banner'`): A clear call to action to explore the products.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page reinforces our commitment to specific clinical fields. It demonstrates that we understand the nuances of feline medicine and have developed targeted tools to address them.
*   **Data-Dependency**: The executing AI must reference `整理策略/dim_products.json` to identify and select the products that are specifically categorized under **"Feline Gastrointestinal"**.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `feline-gastrointestinal`
    *   **`page_url`**: `/solutions/feline-gastrointestinal`
    *   **`product_center_url`**: `/products`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a `headline` that resonates with veterinarians who treat cats with non-specific signs like vomiting or diarrhea.
3.  **Define Clinical Challenges**: In the `feature_list` section, create 3-4 `items` describing common issues in feline GI cases (e.g., "Vague and Non-Specific Symptoms", "Differentiating Pancreatitis from Other Causes", "The Challenge of In-Clinic Fecal Testing").
4.  **Select Relevant Products**: 
    *   **Scan `dim_products.json`**: Programmatically search the `rows` in the product data file.
    *   **Filter**: Select all product objects where `product_category_name` is equal to `"Feline Gastrointestinal"`.
    *   **Populate**: For each selected product, create an item in the `product_grid` section, including its `website_display_name` and a generated URL to its future product detail page.
5.  **Link to Resources**: In the `related_content_grid`, create a placeholder link to a relevant case study.
6.  **Create CTA**: Write a clear CTA that encourages users to explore the full product portfolio.
7.  **Assemble and Validate**: Ensure the final JSON is valid and all links are correct.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "feline-gastrointestinal",
  "page_url": "/solutions/feline-gastrointestinal",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "sol-fgi-hero",
        "headline": "From Vague Symptoms to Clear Answers in Feline GI Cases",
        "subheader": "Reliable, rapid diagnostics for common feline gastrointestinal and pancreatic issues."
      },
      {
        "type": "feature_list",
        "id": "sol-fgi-challenges",
        "headline": "The Frustration of Feline GI Diagnostics",
        "items": [
          { "title": "Non-Specific Symptoms", "description": "Lethargy, anorexia, and intermittent vomiting can point to a dozen different conditions. You need data to narrow the differentials." },
          { "title": "The Pancreatitis Puzzle", "description": "Feline pancreatitis is notoriously difficult to diagnose. A reliable, species-specific lipase test is essential."
          },
          { "title": "Client-Friendly Testing", "description": "In-clinic fecal testing for common pathogens like Giardia and Panleukopenia allows for immediate treatment and biosecurity protocols."
          }
        ]
      },
      {
        "type": "product_grid",
        "id": "sol-fgi-products",
        "headline": "Our Recommended Diagnostic Panel",
        "items": [
          {
            "product_name": "Feline Pancreatic Lipase (fPL) Test",
            "url": "/products/feline/fpl",
            "image_url": "/assets/images/products/thumb-fpl.jpg"
          },
          {
            "product_name": "Feline Giardia Ag Test",
            "url": "/products/feline/gia-ag",
            "image_url": "/assets/images/products/thumb-fgia.jpg"
          }
        ]
      },
      {
        "type": "related_content_grid",
        "id": "sol-fgi-related",
        "headline": "Related Insights",
        "items": [
          {
            "title": "Case Study: A Challenging Case of Feline Fever of Unknown Origin",
            "url": "/resources/case-studies/feline-fever-unknown-origin",
            "image_url": "/assets/images/resources/thumb-case-fever.jpg"
          }
        ]
      },
      {
        "type": "cta_banner",
        "id": "sol-fgi-cta",
        "headline": "See All Feline Diagnostics",
        "primary_cta": {
          "text": "Go to Product Center",
          "url": "/products"
        }
      }
    ]
  }
}
```
