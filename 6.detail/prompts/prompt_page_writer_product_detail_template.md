
# Prompt: Product Detail Page (PDP) Content Generation Template (V2 - Link-Aware)

## Role
You are a technical marketing writer, a master at translating product features into clear customer benefits. You embody the **"Rigorous Expert"** tone, providing precise, reliable information for veterinarians making purchasing decisions.

## Core Task
Generate a complete, development-ready JSON content structure for a **specific product detail page**. This prompt is a template; the final AI will be given a specific product's data as input. Your instructions must guide the AI to populate the page with all necessary technical and marketing information.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your final JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Product Header** (`type: 'product_header'`): Key product info at a glance.
    *   `product_name`, `product_category`, `short_description`
*   **Section 2: Product Overview** (`type: 'text_with_image'`): A marketing overview with a key visual.
    *   `headline`, `body_text`, `image_url`
*   **Section 3: Key Features** (`type: 'feature_list'`): Bullet points highlighting benefits.
    *   `headline`, `items` (array of feature objects)
*   **Section 4: Technical Specifications** (`type: 'data_table'`): Detailed technical data.
    *   `headline`, `table` (object with headers and rows)
*   **Section 5: Resources & Downloads** (`type: 'resource_list'`): Links to manuals, brochures, etc.
    *   `headline`, `resources` (array of resource link objects)
*   **Section 6: CTA** (`type: 'cta_banner'`): A clear call to action.
    *   `headline`, `primary_cta`

---

## 2. Input Data & Strategic Context

*   **Core Strategy (from `plans.md`)**: These PDPs are the "digital ammunition" for the sales team and support the **"Cost Blade"** strategy. They must be factual, comprehensive, and persuasive.
*   **Data-Dependency**: The executing AI will be provided with a single product object from our master product data file.
    *   **Source File**: `整理策略/dim_products.json`
    *   **Input**: A single JSON object from the `rows` array corresponding to one product.

*   **Link & SEO Inputs**:
    *   The `page_slug` and `page_url` will be dynamically generated from the product name (e.g., `/products/canine/hw-lyme-ana-ehr`).
    *   **`contact_us_url`**: `/contact-us` (for the CTA).

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Receive Product Data**: You will be given a single JSON object for one product.
2.  **Structure the JSON**: Create the root JSON object with the `page_slug` and `page_url` derived from the product's `website_display_name` and `product_category_name`.
3.  **Populate the Header**: Fill the `product_name`, `product_category`, and `short_description` from the input product data.
4.  **Write Overview**: In the `text_with_image` section, write a 1-2 paragraph `body_text` that introduces the test, the diseases it covers, and its primary benefit (e.g., speed, accuracy, confidence).
5.  **Extract Key Features**: From the input product data (e.g., `feature_bullets` field), populate the `items` in the `feature_list` section.
6.  **Format Specifications**: In the `data_table` section, transform the key-value pairs from the product's `technical_specifications` field into a structured table with `rows`.
7.  **List Resources**: In the `resource_list` section, create placeholder `resources` for essential documents like 'Instructions for Use (IFU)' and 'Product Brochure', creating placeholder URLs for them.
8.  **Create CTA**: In the `cta_banner`, write a clear headline and a `primary_cta` that directs the user to contact sales for purchasing info. The CTA object must contain `text` and the `url` `/contact-us`.
9.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "hw-lyme-ana-ehr",
  "page_url": "/products/canine/hw-lyme-ana-ehr",
  "content": {
    "sections": [
      {
        "type": "product_header",
        "id": "pdp-header",
        "product_name": "Canine Heartworm, Lyme, Anaplasma, Ehrlichia Combo Test",
        "product_category": "Canine Infectious Disease",
        "short_description": "A single, rapid test for the detection of four common vector-borne diseases."
      },
      {
        "type": "text_with_image",
        "id": "pdp-overview",
        "headline": "Confidence in a Single Sample",
        "body_text": "...",
        "image_url": "/assets/images/products/pdp-canine-combo.jpg"
      },
      {
        "type": "feature_list",
        "id": "pdp-features",
        "headline": "Key Features & Benefits",
        "items": [
          { "title": "Multi-Analyte Detection", "description": "Simultaneously tests for Dirofilaria immitis, Borrelia burgdorferi, Anaplasma, and Ehrlichia from one sample." },
          { "title": "Rapid Results", "description": "Actionable insights in under 10 minutes, right at the point of care." }
        ]
      },
      {
        "type": "data_table",
        "id": "pdp-specs",
        "headline": "Technical Specifications",
        "table": {
          "headers": ["Parameter", "Specification"],
          "rows": [
            [ "Sample Type", "Whole Blood / Serum / Plasma" ],
            [ "Time to Result", "10 minutes" ],
            [ "Storage", "Room Temperature (2-30°C)" ]
          ]
        }
      },
      {
        "type": "resource_list",
        "id": "pdp-resources",
        "headline": "Resources & Downloads",
        "resources": [
          { "title": "Instructions for Use (IFU)", "url": "/resources/downloads/ifu-hw-lyme-ana-ehr.pdf" },
          { "title": "Product Brochure", "url": "/resources/downloads/brochure-hw-lyme-ana-ehr.pdf" }
        ]
      },
      {
        "type": "cta_banner",
        "id": "pdp-cta",
        "headline": "Ready to Add to Your Clinic?",
        "primary_cta": {
          "text": "Contact Sales for Pricing",
          "url": "/contact-us"
        }
      }
    ]
  }
}
```
