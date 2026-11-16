# Design system

This document describes the visual conventions for the Max & Natalie wedding site. Follow it when creating or changing site pages and components. The implementation lives in [`assets/css/style.css`](assets/css/style.css); update the stylesheet and this document together when intentionally changing the system.

## Design direction

Keep the site warm, welcoming, personal, and easy to read. Pair restrained editorial typography with a soft, natural palette, generous whitespace, and photography that feels intimate and celebratory. Prefer simple page-specific layouts over introducing a general-purpose component framework.

## Colors

Use the CSS custom properties in `:root` rather than repeating color values.

| Token | Value | Use |
|---|---|---|
| `--paper` | `#f4f1eb` | Page background |
| `--ink` | `#25342e` | Primary text |
| `--muted` | `#68756c` | Supporting text, captions, and inactive navigation |
| `--leaf` | `#55725c` | Eyebrow labels and natural accents |
| `--coral` | `#c65e4d` | Links, active navigation, and small expressive accents |
| `--line` | `#d8d6cd` | Subtle separators |

Keep the background light and the overall contrast comfortable. Use coral as an accent, not for large text-heavy areas.

## Typography

- **Body and interface:** DM Sans, with a sans-serif fallback.
- **Headings:** Playfair Display, with a Georgia fallback; use a light, editorial weight.
- **Page title:** Large and expressive on wide screens; reduce it for mobile. The home hero title may use the coral italic ampersand accent.
- **Section heading:** Use the serif heading style, with a restrained size and clear hierarchy below the page title.
- **Eyebrow:** Small, bold, uppercase sans-serif text with generous letter spacing in `--leaf`.
- **Body copy:** Usually 16px with relaxed line height. Use `--muted` for explanatory text and `--ink` for primary content.
- **Navigation, captions, and metadata:** Keep smaller and quiet, but readable.

Avoid adding font families or decorative type styles without a clear need.

## Layout and spacing

- Center the shared header and footer in a container no wider than 1280px.
- Keep reading-focused pages and sections around 850px wide; constrain individual text blocks further where helpful.
- Give sections generous vertical padding and use consistent side gutters. Existing desktop layouts use `6vw`; mobile layouts use 22px.
- Use whitespace to distinguish sections rather than adding heavy borders, cards, or shadows.
- The home hero uses a two-column text-and-photo layout on wide screens, with the photo slightly more prominent. Stack it on narrow screens.

## Components and imagery

- **Header:** Site wordmark on one side and concise navigation on the other. Highlight the current page and provide a hover state.
- **Links:** Keep links recognizable. Text links use the coral accent and an underline or other clear affordance.
- **Images:** By default, content images fill their container, use a portrait 4:5 crop with `object-fit: cover`, and have subtly rounded 6px corners for a restrained, formal finish. Use the `image-natural` class for logos, icons, or other images that should keep their natural aspect ratio and have no rounded corners. Provide meaningful alternative text.
- **Story and information pages:** Use readable text widths, clear headings, and left-aligned prose where appropriate.
- **RSVP:** Keep the introduction and form within the reading-width content area. Give third-party embeds enough height to avoid clipping their content, especially on narrow screens. If an embed is too wide to fit a very narrow screen without horizontal scrolling, hide the embed and provide a clear link to open the form separately.
- Prefer semantic HTML and the existing shared layout rather than recreating site-wide navigation or footer markup on individual pages.

## Responsive behavior and accessibility

- The current mobile breakpoint is 700px. At or below it, stack multi-column content, reduce heading sizes and navigation gaps, and use the 22px side gutter.
- Prevent horizontal scrolling at small viewport widths. Embedded content should fit its container and remain usable on mobile.
- Use a logical heading hierarchy, descriptive link text, and appropriate labels for embedded or interactive content.
- Preserve visible keyboard focus and sufficient text contrast when adding or changing interactive elements.
- Do not convey meaning through color alone.

## Content

- Write visitor-facing copy in Norwegian Bokmål, consistent with the site's `lang: nb` setting.
- Keep the tone warm, direct, and personal. Prefer concise, helpful wording over placeholder-like or overly formal copy.
- Use real event details when available; do not invent dates, locations, or RSVP requirements.
