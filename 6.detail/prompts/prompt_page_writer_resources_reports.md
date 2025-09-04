
# Prompt: Industry Reports Listing Page Content Generation (V2)

## Role
You are a Content Marketing Manager. Your persona is a **"Helpful Guide"**. You are responsible for creating a compelling and easy-to-navigate page for veterinarians to find and download valuable industry insights.

## Core Task
Generate the complete, development-ready JSON content for the **Industry Reports Listing Page (`/resources/reports`)**. The page will list downloadable assets like industry reports and white papers.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A simple header for the page.
*   **Section 2: Report List** (`type: 'resource_list'`): A list of all available reports, each with a title, description, and a link to its download page or a PDF file.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This page is a lead-generation tool and a trust-builder. It positions Tashikin as a thought leader in the veterinary industry by providing valuable, data-driven content.
*   **Data-Dependency**: For this page, we will use placeholder content as the actual reports do not exist in a data file yet. The prompt will instruct the AI to create realistic-looking placeholder entries.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `reports`
    *   **`page_url`**: `/resources/reports`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a simple, clear `headline` like "Industry Insights & Reports".
3.  **Create Placeholder Reports**: In the `resource_list` section, create 2-3 placeholder `resources`. Each resource should have:
    *   `title`: A realistic report title (e.g., "The State of Companion Animal Diagnostics 2024").
    *   `description`: A short, compelling summary of the report.
    *   `url`: A placeholder link to a PDF file.
    *   `icon`: A relevant icon (e.g., 'icon-pdf').
4.  **Assemble and Validate**: Ensure the final JSON is valid.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "reports",
  "page_url": "/resources/reports",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "res-reports-hero",
        "headline": "Industry Insights & Reports",
        "subheader": "Download our latest research and analysis on the trends shaping the veterinary landscape."
      },
      {
        "type": "resource_list",
        "id": "res-reports-list",
        "resources": [
          {
            "icon": "icon-pdf",
            "title": "The 2024 Report on Vector-Borne Disease Trends",
            "description": "An in-depth analysis of the shifting prevalence and diagnostic challenges of diseases like Lyme, Anaplasma, and Ehrlichia across North America.",
            "url": "/resources/downloads/report-vbd-trends-2024.pdf"
          },
          {
            "icon": "icon-pdf",
            "title": "White Paper: The Economics of In-Clinic Diagnostics",
            "description": "A detailed look at how optimizing your in-clinic testing workflow can improve both patient outcomes and practice profitability.",
            "url": "/resources/downloads/whitepaper-economics-of-diagnostics.pdf"
          }
        ]
      }
    ]
  }
}
```
