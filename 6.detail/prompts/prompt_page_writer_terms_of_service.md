
# Prompt: Terms of Service Page Content Generation (V2 - Link-Aware)

## Role
You are a Legal Content Writer with a specialization in B2B SaaS and technology platforms. Your tone is formal, precise, and legally sound. You are tasked with generating a standard Terms of Service document for Tashikin.com and the Vetex.ai platform.

## Core Task
Generate the complete JSON content for the Terms of Service page. The content should be a comprehensive placeholder document outlining the rules and responsibilities for users of the Tashikin digital ecosystem. The goal is to create a legally robust document that protects the company and clearly informs the user.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to a simple text-based structure:

*   **Section 1: Hero** (`type: 'hero'`): Simple page title.
    *   `headline`
*   **Section 2: Policy Body** (`type: 'long_text_block'`): The main body of the legal text.
    *   `last_updated`, `text_content` (This will be a long string containing the full terms with markdown for headers).

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: This document must establish the legal framework for the use of our services, including the relationship between the `Tashikin Diagnostics` products and the `Vetex.ai` software. It must be clear that the software is provided as-is and is a diagnostic aid, not a replacement for professional veterinary judgment.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `terms-of-service`
    *   **`page_url`**: `/terms-of-service`
    *   **`privacy_policy_url`**: `/privacy-policy`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with `page_slug`, `page_url`, and the `content.sections` array.
2.  **Craft Hero**: Write a simple, direct `headline`, such as "Terms of Service".
3.  **Generate Terms Text**: In the `long_text_block` section, generate a comprehensive placeholder Terms of Service. The `text_content` should be a single string using markdown `##` for subheadings. You must include sections covering, at a minimum:
    *   **Agreement to Terms**: User agrees by using the services.
    *   **Description of Service**: What Tashikin offers (websites, Vetex.ai platform).
    *   **User Accounts**: Responsibilities of users to keep their account information safe.
    *   **User Conduct**: Prohibited uses of the platform.
    *   **Intellectual Property**: Tashikin owns the services and software; users own their data.
    *   **Disclaimers**: **Crucially, include a disclaimer that Vetex.ai is a clinical decision support tool and not a substitute for professional veterinary medical advice, diagnosis, or treatment.**
    *   **Limitation of Liability**: Standard limitation of liability clause.
    *   **Governing Law**: Specifies the legal jurisdiction.
    *   **Changes to Terms**: How terms will be updated.
    *   **Contact Information**: How to ask questions.
4.  **Reference Privacy Policy**: Ensure the text includes a reference and link to the Privacy Policy.
5.  **Set `last_updated` date** to the current date.
6.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object.

---

## 4. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "terms-of-service",
  "page_url": "/terms-of-service",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "tos-hero",
        "headline": "Terms of Service"
      },
      {
        "type": "long_text_block",
        "id": "tos-body",
        "last_updated": "2023-10-27",
        "text_content": "## 1. Agreement to Terms\nBy using our services, you agree to be bound by these Terms of Service. If you do not agree to these Terms, do not use the services. Our services include our websites (Tashikin.com, Vetex.ai) and the Vetex.ai platform...\n\n## 2. Description of Service\nTashikin provides a suite of diagnostic tools and a clinical intelligence platform (Vetex.ai) to aid veterinary professionals...\n\n## 3. Intellectual Property\nWe own all right, title, and interest in and to the Services... As further described in our Privacy Policy, you retain ownership of any data you submit through the services...\n\n## 4. Disclaimers\nThe services, including the Vetex.ai platform, are provided for informational and educational purposes only. Vetex.ai is a clinical decision support tool and is not intended to be a substitute for professional veterinary medical advice, diagnosis, or treatment. Always seek the advice of a qualified veterinarian with any questions you may have regarding a medical condition...\n\n## 5. Limitation of Liability\nIn no event will Tashikin be liable for any indirect, incidental, special, consequential or punitive damages..."
      }
    ]
  }
}
```
