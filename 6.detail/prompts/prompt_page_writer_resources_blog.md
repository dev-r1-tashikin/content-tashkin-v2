
# Prompt: Blog Listing Page Content Generation (V2)

## Role
You are a Content Strategist and UX Writer. Your persona is a **"Helpful Guide"**. You are creating the main landing page for the company's blog, which will feature a variety of articles on clinical topics, practice management, and company news.

## Core Task
Generate the complete, development-ready JSON content for the **Blog Listing Page (`/resources/blog`)**. The page will serve as a browsable and filterable archive of all blog posts.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A simple header for the blog.
*   **Section 2: Featured Post** (`type: 'featured_article'`): Highlights the most recent or important post.
*   **Section 3: Article Grid** (`type: 'article_grid'`): A grid of all other blog posts, which would ideally be paginated.
*   **Section 4: Filter/Search Bar** (`type: 'filter_bar'`): UI elements to filter posts by category.

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: The blog is a key part of the "Content & Education Engine." It drives organic traffic, nurtures leads, and establishes brand authority. This page is the central hub for that engine.
*   **Data-Dependency**: This page will be populated by a CMS in the future. For now, the prompt will instruct the AI to create realistic placeholder blog post entries.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `blog`
    *   **`page_url`**: `/resources/blog`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with the correct `page_slug` and `page_url`.
2.  **Craft Hero Content**: Write a welcoming `headline` for the blog, like "Tashikin Insights".
3.  **Create Placeholder Posts**: Create 4-5 realistic placeholder articles. Designate one as the `featured_post`. The others will go into the `article_grid`. Each post needs:
    *   `title`: A compelling blog post title.
    *   `url`: A placeholder link to the full article page.
    *   `summary`: A brief teaser of the article's content.
    *   `category`: A relevant category (e.g., "Clinical Insights", "Practice Management").
    *   `date`: A publication date.
    *   `image_url`: A placeholder image URL.
4.  **Define Filter Categories**: In the `filter_bar` section, create a list of categories based on the placeholder posts you created.
5.  **Assemble and Validate**: Ensure the final JSON is valid.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "blog",
  "page_url": "/resources/blog",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "res-blog-hero",
        "headline": "Tashikin Insights Blog",
        "subheader": "Expert perspectives on diagnostics, clinical challenges, and practice growth."
      },
      {
        "type": "featured_article",
        "id": "res-blog-featured",
        "post": {
          "title": "Decoding Canine Cough: A Guide to Differential Diagnosis",
          "url": "/resources/blog/decoding-canine-cough",
          "summary": "Canine Infectious Respiratory Disease (CIRD) is complex. Learn how to approach these cases systematically and which diagnostics can give you the clearest answers.",
          "category": "Clinical Insights",
          "date": "2023-11-20",
          "image_url": "/assets/images/blog/featured-canine-cough.jpg"
        }
      },
      {
        "type": "filter_bar",
        "id": "res-blog-filters",
        "categories": [
          "All Posts",
          "Clinical Insights",
          "Practice Management",
          "Company News"
        ]
      },
      {
        "type": "article_grid",
        "id": "res-blog-grid",
        "posts": [
          {
            "title": "5 Ways to Improve Your Clinic's Curbside Workflow",
            "url": "/resources/blog/curbside-workflow-tips",
            "summary": "Make your drop-off appointments smoother and more efficient for your team and your clients with these simple tips.",
            "category": "Practice Management",
            "date": "2023-11-10",
            "image_url": "/assets/images/blog/thumb-curbside.jpg"
          },
          {
            "title": "Welcoming Dr. Anya Sharma as our new Chief Medical Officer",
            "url": "/resources/blog/welcome-dr-sharma",
            "summary": "We are thrilled to announce that Dr. Anya Sharma, a board-certified veterinary internist, has joined the Tashikin leadership team.",
            "category": "Company News",
            "date": "2023-11-05",
            "image_url": "/assets/images/blog/thumb-dr-sharma.jpg"
          }
        ]
      }
    ]
  }
}
```
