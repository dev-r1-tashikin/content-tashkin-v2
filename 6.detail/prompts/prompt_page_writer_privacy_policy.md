
# Prompt: Privacy Policy Page Content Generation (V2 - Link-Aware)

## Role
You are a Legal Content Writer with a specialization in technology and healthcare. Your tone is professional, clear, and unambiguous. You are tasked with generating a standard Privacy Policy for Tashikin.com and the Vetex.ai platform.

## Core Task
Generate the complete JSON content for the Privacy Policy page. The content should be a comprehensive, well-structured placeholder policy that covers standard topics like data collection, usage, sharing, and user rights. The primary goal is to provide a legally sound and trustworthy document.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to a simple text-based structure:

*   **Section 1: Hero** (`type: 'hero'`): Simple page title.
    *   `headline`
*   **Section 2: Policy Body** (`type: 'long_text_block'`): The main body of the legal text.
    *   `last_updated`, `text_content` (This will be a long string containing the full policy with markdown for headers).

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: The Privacy Policy is a trust-building document. It must be clear and transparent, especially regarding the use of clinical data within the Vetex.ai platform. It needs to reassure users that they own their data.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `privacy-policy`
    *   **`page_url`**: `/privacy-policy`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with `page_slug`, `page_url`, and the `content.sections` array.
2.  **Craft Hero**: Write a simple, direct `headline`, such as "Privacy Policy".
3.  **Generate Policy Text**: In the `long_text_block` section, generate a comprehensive placeholder Privacy Policy. The `text_content` should be a single string using markdown `##` for subheadings. You must include sections covering, at a minimum:
    *   **Introduction**: Who we are (Tashikin Inc.) and what this policy covers.
    *   **Information We Collect**: Differentiate between personal data (e.g., for account registration) and clinical data (patient/diagnostic data processed by Vetex.ai).
    *   **How We Use Your Information**: Explain usage for providing services, communication, and for R&D (mentioning that clinical data is only used in an **anonymized and aggregated** form for improving the AI).
    *   **How We Share Your Information**: Standard clauses about service providers, legal requirements, etc. Reassure users that personally identifiable clinical data is not sold.
    *   **Data Ownership and User Rights**: **Crucially, include a clause that explicitly states the user (the clinic) retains full ownership of their data.** Outline user rights like access, correction, and deletion.
    *   **Data Security**: How we protect the data.
    *   **Changes to This Policy**: Standard clause.
    *   **Contact Information**: How to ask questions about the policy.
4.  **Set `last_updated` date** to the current date.
5.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "privacy-policy",
  "page_url": "/privacy-policy",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "pp-hero",
        "headline": "Privacy Policy"
      },
      {
        "type": "long_text_block",
        "id": "pp-body",
        "last_updated": "2023-10-27",
        "text_content": "## 1. Introduction\nWelcome to Tashikin. This Privacy Policy explains how Tashikin Inc. (\"Tashikin\", \"we\", \"us\", or \"our\") collects, uses, and discloses information about you when you use our websites, including Tashikin.com and Vetex.ai, and our related services...\n\n## 2. Information We Collect\nWe collect information in a few different ways...\n\n### Information You Provide to Us\nThis includes account registration information such as your name, clinic name, email address...\n\n### Clinical & Diagnostic Data\nWhen you use the Vetex.ai platform, you may upload or input clinical data... **You and your clinic retain ownership of this data at all times.**\n\n## 3. How We Use Your Information\n...We may use anonymized and aggregated Clinical & Diagnostic Data to improve our AI models and for research purposes...\n\n## 4. Data Ownership and Your Rights\nWe believe in a simple principle: your data is your data. You retain full ownership of all data you submit to our services. You have the right to access, correct, or delete your data at any time..."
      }
    ]
  }
}
```
