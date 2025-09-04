
# Prompt: Resource Center Page Content Generation (V2 - Link-Aware)

## Role
You are an expert Content Strategist and UX Writer, embodying the persona of a **"Sharp Mentor"**. Your tone is that of an **"Empowering Sage"** (赋能的智者), focused on curating and presenting knowledge in a clear, accessible, and engaging way. You are building the content for Tashikin's thought leadership hub.

## Core Task
Generate the complete, development-ready JSON content for the Resource Center page. This page must function as a filterable library for all of Tashikin's educational content, empowering veterinarians to find the knowledge they need to grow professionally.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your final JSON output will be a single object with a `page` object inside. The `page.content.sections` will be an array of objects mapping to this structure:

*   **Section 1: Hero** (`type: 'hero'`): Sets the vision for the Resource Center.
    *   `headline`, `subheader`
*   **Section 2: Featured Content** (`type: 'featured_post'`): Highlights the most important or recent content asset.
    *   `headline`, `post` (an object with `title`, `summary`, and `link` object)
*   **Section 3: Content Library** (`type: 'filterable_grid'`): The main interactive part of the page.
    *   `headline`, `filters` (an array of filter objects), `items` (an array of content card objects)

---

## 2. Input Data & Strategic Context
The executing AI must synthesize the following:

*   **Core Strategy (from `7.0_tashikin_内容与教育引擎战略规划.md`)**:
    *   **Content is the Product**: This page is the "Content Mother-ship." It must showcase our three core content pillars: 
        1.  `《病例解读挑战》` (Case Interpretation)
        2.  `《Tashikin兽医行业洞察报告》` (Data-Driven Management)
        3.  `《与宠物主人沟通的艺术》` (Client Communication)
    *   **Empower, Don't Sell**: The page should feel like an academic or professional resource, not a marketing page.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `resource-center`
    *   **`page_url`**: `/resources`
    *   **Placeholder URLs**: The AI should generate logical placeholder URLs for the content items (e.g., `/resources/case-challenges/feline-jaundice-case`).

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with `page_slug`, `page_url`, and the `content.sections` array.
2.  **Craft Hero Content**: Write an inspiring `headline` and `subheader` for the hero section that communicates the purpose of the Resource Center: to advance clinical knowledge and diagnostic thinking.
3.  **Define Featured Content**: For the `featured_post` section, create a placeholder for the latest flagship content piece. A good default is the most recent `Tashikin兽医行业洞察报告`. The `link` object must have `text` and `url` keys.
4.  **Build the Library**:
    *   **Filters**: In the `filterable_grid` section, define the `filters`. This should be an array of objects for each of our core content pillars (e.g., "Case Challenges," "Industry Reports," "Webinars," "Articles").
    *   **Content Items**: Populate the `items` array with at least 3-4 placeholder content cards. Ensure each card represents a different content type (filter category). Each card must have a `title`, `summary`, `category`, and a `link` object with `text` and `url`.
5.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object that strictly adheres to the schema in Section 5.

---

## 4. Example of High-Quality Output (For Content Tone)

**Hero Headline:** "Advancing Diagnostic Excellence, Together."
**Hero Sub-headline:** "Welcome to the Tashikin Resource Center, a curated library of data-driven insights, clinical case challenges, and communication strategies designed to empower your diagnostic journey."

**Featured Post Summary:** "Our Q3 report, based on anonymized data from over 50,000 cases, reveals a surprising trend in feline upper respiratory infections. Discover the implications for your clinic's diagnostic and treatment protocols this season."

---

## 5. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "resource-center",
  "page_url": "/resources",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "rc-hero",
        "headline": "...",
        "subheader": "..."
      },
      {
        "type": "featured_post",
        "id": "rc-featured",
        "headline": "Featured Insight",
        "post": {
          "title": "Q3 Industry Report: Feline URI Trends",
          "summary": "...",
          "image_url": "/assets/images/report-cover-q3.jpg",
          "link": {
            "text": "Read the Full Report",
            "url": "/resources/reports/feline-uri-trends-q3"
          }
        }
      },
      {
        "type": "filterable_grid",
        "id": "rc-library",
        "headline": "Explore Our Library",
        "filters": [
          { "name": "All", "slug": "all" },
          { "name": "Case Challenges", "slug": "case-challenges" },
          { "name": "Industry Reports", "slug": "industry-reports" },
          { "name": "Webinars", "slug": "webinars" },
          { "name": "Articles", "slug": "articles" }
        ],
        "items": [
          {
            "category": "Case Challenges",
            "title": "Case Challenge #3: A Jaundiced Cat's Diagnostic Puzzle",
            "summary": "A 3-year-old MC DSH presents with acute lethargy and icterus. Navigate the data and share your diagnostic pathway.",
            "link": {
              "text": "Take the Challenge",
              "url": "/resources/case-challenges/jaundiced-cat-puzzle"
            }
          },
          {
            "category": "Webinars",
            "title": "Webinar: Mastering Client Communication for Chronic Kidney Disease",
            "summary": "Learn a 3-step framework for explaining complex CKD diagnoses to pet owners, improving compliance and trust.",
            "link": {
              "text": "Watch Now",
              "url": "/resources/webinars/ckd-client-communication"
            }
          },
          {
            "category": "Articles",
            "title": "The Rise of Point-of-Care NT-proBNP in Feline Cardiology",
            "summary": "How is the increasing availability of in-clinic NT-proBNP changing the way we approach feline cardiac workups? A review of the latest evidence.",
            "link": {
              "text": "Read the Article",
              "url": "/resources/articles/pocr-ntprobnp-feline-cardiology"
            }
          }
        ]
      }
    ]
  }
}
```
