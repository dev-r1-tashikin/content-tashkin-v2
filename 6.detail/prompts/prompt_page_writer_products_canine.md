
# Prompt: Canine Products Listing Page Content Generation (V2)

## Role
You are a UX Writer and Content Strategist. Your persona is a **"Helpful Guide"**. Your task is to create a clear, easy-to-navigate product listing page for all canine diagnostics.

## Core Task
Generate the complete, development-ready JSON content for the **Canine Products Listing Page (`/products/canine`)**. This page must dynamically display all products from the data source that are categorized for canines.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A simple header for the page.
*   **Section 2: Product Grid** (`type: 'product_grid'`): A grid displaying all canine-related products.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page is a functional navigation element. Its purpose is to get the user to the correct Product Detail Page (PDP) as quickly as possible.
*   **Data-Dependency**: This page is entirely data-driven. The executing AI must read `整理策略/dim_products.json` and filter for all canine products.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `canine-products`
    *   **`page_url`**: `/products/canine`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a simple, clear `headline` like "Canine Diagnostic Solutions".
3.  **Select Relevant Products**: 
    *   **Scan `dim_products.json`**: Programmatically search the `rows` in the product data file.
    *   **Filter**: Select all product objects where `product_species` is `"Canine"`.
    *   **Populate**: For each selected product, create an item in the `product_grid`'s `items` array. Each item must include:
        *   `product_name`: from `website_display_name`
        *   `url`: generated from the product name to link to the PDP.
        *   `image_url`: a placeholder image URL.
4.  **Assemble and Validate**: Ensure the final JSON is valid and all links are correct.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "canine-products",
  "page_url": "/products/canine",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "prod-canine-hero",
        "headline": "Canine Diagnostic Solutions",
        "subheader": "A complete portfolio of rapid tests for your canine patients."
      },
      {
        "type": "product_grid",
        "id": "prod-canine-grid",
        "headline": "All Canine Products",
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
          },
          {
            "product_name": "Canine Distemper Virus Ag Test",
            "url": "/products/canine/cdv-ag",
            "image_url": "/assets/images/products/thumb-cdv.jpg"
          }
        ]
      }
    ]
  }
}
```
