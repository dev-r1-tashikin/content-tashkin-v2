
# Prompt: Feline Products Listing Page Content Generation (V2)

## Role
You are a UX Writer and Content Strategist. Your persona is a **"Helpful Guide"**. Your task is to create a clear, easy-to-navigate product listing page for all feline diagnostics.

## Core Task
Generate the complete, development-ready JSON content for the **Feline Products Listing Page (`/products/feline`)**. This page must dynamically display all products from the data source that are categorized for felines.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A simple header for the page.
*   **Section 2: Product Grid** (`type: 'product_grid'`): A grid displaying all feline-related products.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page is a functional navigation element. Its purpose is to get the user to the correct Product Detail Page (PDP) as quickly as possible.
*   **Data-Dependency**: This page is entirely data-driven. The executing AI must read `整理策略/dim_products.json` and filter for all feline products.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `feline-products`
    *   **`page_url`**: `/products/feline`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a simple, clear `headline` like "Feline Diagnostic Solutions".
3.  **Select Relevant Products**: 
    *   **Scan `dim_products.json`**: Programmatically search the `rows` in the product data file.
    *   **Filter**: Select all product objects where `product_species` is `"Feline"`.
    *   **Populate**: For each selected product, create an item in the `product_grid`'s `items` array. Each item must include:
        *   `product_name`: from `website_display_name`
        *   `url`: generated from the product name to link to the PDP.
        *   `image_url`: a placeholder image URL.
4.  **Assemble and Validate**: Ensure the final JSON is valid and all links are correct.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "feline-products",
  "page_url": "/products/feline",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "prod-feline-hero",
        "headline": "Feline Diagnostic Solutions",
        "subheader": "A complete portfolio of rapid tests for your feline patients."
      },
      {
        "type": 'product_grid',
        "id": "prod-feline-grid",
        "headline": "All Feline Products",
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
          },
          {
            "product_name": "Feline Immunodeficiency Virus (FIV) Ab / Feline Leukemia Virus (FeLV) Ag Combo Test",
            "url": "/products/feline/fiv-felv-combo",
            "image_url": "/assets/images/products/thumb-fiv-felv.jpg"
          }
        ]
      }
    ]
  }
}
```
