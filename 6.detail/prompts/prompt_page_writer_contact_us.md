
# Prompt: Contact Us Page Content Generation (V2 - Link-Aware)

## Role
You are a UX Writer and Communications Specialist, operating under the persona of a **"Helpful Guide"**. Your tone is clear, friendly, and efficient. You are creating the content for the "Contact Us" page.

## Core Task
Generate the complete, development-ready JSON content for the "Contact Us" page. The goal is to make it as easy as possible for users to find the information they need or get in touch with the correct department.

---

## 1. Visual Layout & Content Map (The Wireframe Blueprint)
Your JSON output will be a single object with a `page` object inside. The `page.content.sections` array will map to this structure:

*   **Section 1: Hero** (`type: 'hero'`): A simple, clear header.
    *   `headline`, `subheader`
*   **Section 2: Contact Options** (`type: 'contact_cards'`): A set of cards directing users to different contact methods.
    *   `headline`, `cards` (an array of card objects for different departments)
*   **Section 3: Contact Form** (`type: 'form_module'`): A general inquiry form.
    *   `headline`, `form_fields`, `submit_button`
*   **Section 4: Location** (`type: 'map_with_address'`): Displays office location.
    *   `headline`, `address`, `map_coordinates`

---

## 2. Input Data & Strategic Context

*   **Core Strategy**: The page should be highly functional and user-centric. It should efficiently route inquiries to the correct channel to reduce internal workload and improve user satisfaction.

*   **Link & SEO Inputs**:
    *   **`page_slug`**: `contact-us`
    *   **`page_url`**: `/contact-us`
    *   **`partners_url`**: `/partners` (for the partnership inquiries card)
    *   **`form_submission_endpoint`**: `/api/contact-inquiry`

---

## 3. Step-by-Step Execution Plan for the AI

1.  **Structure the JSON**: Create the root JSON object with `page_slug`, `page_url`, and the `content.sections` array.
2.  **Craft Hero Content**: Write a welcoming `headline` and a `subheader` that reassures the user they are in the right place.
3.  **Build Contact Cards**: In the `contact_cards` section, create 3-4 distinct `cards`. Each card should be for a specific inquiry type and provide the right information or link:
    *   **General/Sales Inquiry**: Provide a phone number and email address.
    *   **Technical/Product Support**: Provide a dedicated support email.
    *   **Partnership Inquiry**: Do not provide an email. Instead, write text that directs them to the Partners page and include a link object pointing to `/partners`.
4.  **Build the Form**: In the `form_module` section, define the necessary `form_fields` for a general inquiry (e.g., Name, Email, Subject, Message) and a clear `submit_button` text.
5.  **Add Location Details**: For the `map_with_address` section, provide placeholder company address details and map coordinates.
6.  **Assemble and Validate**: Ensure the final output is a single, valid JSON object with correct link objects (`text` and `url`).

---

## 4. Example of High-Quality Output (For Content Tone)

**Card Title:** "Partnership Inquiries"
**Card Description:** "Interested in becoming a distributor for Tashikin Diagnostics? We have a dedicated process for new partners. Please visit our Partners page to learn more and submit an inquiry."
**Card CTA Text:** "Go to Partners Page"

---

## 5. Final Output Format (Strictly Adhere to this JSON Structure)
```json
{
  "page_slug": "contact-us",
  "page_url": "/contact-us",
  "content": {
    "sections": [
      {
        "type": "hero",
        "id": "cu-hero",
        "headline": "Get in Touch",
        "subheader": "We're here to help. Find the best way to reach us below."
      },
      {
        "type": "contact_cards",
        "id": "cu-cards",
        "headline": "How can we help you today?",
        "cards": [
          {
            "icon": "icon-sales",
            "title": "Sales & General Inquiries",
            "lines": [
              "For questions about our products or pricing, contact our sales team.",
              "Email: sales@tashikin.com",
              "Phone: +1 (800) 555-1234"
            ]
          },
          {
            "icon": "icon-support",
            "title": "Technical & Product Support",
            "lines": [
              "For assistance with our diagnostic tests or the Vetex.ai platform, reach out to our support specialists.",
              "Email: support@tashikin.com"
            ]
          },
          {
            "icon": "icon-partners",
            "title": "Partnership Inquiries",
            "lines": [
              "Interested in becoming a distributor? Please visit our Partners page to submit an inquiry through the proper channel."
            ],
            "cta": {
              "text": "Go to Partners Page",
              "url": "/partners"
            }
          }
        ]
      },
      {
        "type": "form_module",
        "id": "cu-form",
        "headline": "Send Us a Message",
        "form_fields": [
          { "name": "full_name", "label": "Full Name", "type": "text", "required": true },
          { "name": "email", "label": "Email Address", "type": "email", "required": true },
          { "name": "subject", "label": "Subject", "type": "text", "required": true },
          { "name": "message", "label": "Your Message", "type": "textarea", "required": true }
        ],
        "submit_button": {
          "text": "Send Message"
        },
        "form_action_url": "/api/contact-inquiry"
      },
      {
        "type": "map_with_address",
        "id": "cu-location",
        "headline": "Our Headquarters",
        "address": "123 Innovation Drive, Suite 456, Metropolis, CA 90210, USA",
        "map_coordinates": {
          "latitude": 34.052235,
          "longitude": -118.243683
        }
      }
    ]
  }
}
```
