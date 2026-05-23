# EkaFlow Design System: Alpha v1.1

This document outlines the core visual and interactive standards for EkaFlow, ensuring design continuity for future developments and feature expansions.

---

## 1. Visual Language: "Sophisticated Glassmorphism"
EkaFlow uses a high-end, futuristic dark-mode aesthetic. Elements are layered using **frosted glass** effects with **glowing neon accents**.

### Atmosphere (The "Vibe")
- **High Contrast**: Neon on deep charcoal.
- **Micro-interactions**: Subtle, fluid animations that respond to scroll or hover.
- **Glass Stack**: Objects should feel like they are floating over a deep space.

---

## 2. Color Palette & Tokens
Consistency in color is critical. Use CSS variables defined in [style.css](file:///c:/Users/nikhi_ljq/OneDrive/Desktop/EkaFlow/EkaFlow%20website/style.css).

| Token | Color | Hex Code | Use Case |
| :--- | :--- | :--- | :--- |
| **`--bg-dark`** | Deep Charcoal | `#121212` | Main background |
| **`--primary-orange`** | Sunset Glow | `#FF9653` | Primary CTA, Hero highlight |
| **`--primary-blue`** | Electric Azure | `#5FCAFF` | Secondary accents, Process icons |
| **`--text-main`** | Pure White | `#FFFFFF` | Headings, Primary labels |
| **`--text-light`** | Slate Grey | `#A0A0A0` | Body copy, Secondary descriptions |

---

## 3. Typography
- **Primary Typeface**: [Nunito (Google Fonts)](https://fonts.google.com/specimen/Nunito)
- **Weights**:
  - `900` (Black): Hero titles.
  - `800` (Extra Bold): Section headers.
  - `700` (Bold): Card titles and Subheadings.
  - `400` (Regular): Secondary text.
  - `300` (Light): Main body text for an elegant, tech-forward feel.

---

## 4. Glassmorphism Design Specs
Every "card" or container must follow these specifications:

- **Background**: `rgba(255, 255, 255, 0.03)`
- **Blur**: `backdrop-filter: blur(20px);`
- **Border**: `1px solid rgba(255, 255, 255, 0.08);`
- **Border Radius**: Use `16px` or `24px` for cards.
- **Hover Transitions**: `0.4s cubic-bezier(0.16, 1, 0.3, 1)` (The "Ease-Out" effect).

---

## 5. Layout & Spacing System
EkaFlow uses a centralized container system (`max-width: 1280px`).

- **Grid System**: Use `display: grid` with `gap: 2rem` for card sections.
- **Mobile Spacing**:
  - Always maintain a `10rem` padding-top for sections below a fixed header.
  - Header height should be exactly `48px` on mobile for both logo and buttons.

---

## 6. Motion & Animations
Animations should be performant (CSS-only where possible).

- **`scanner-line`**: A horizontal bar moving vertically to represent "Vision AI".
- **`float`**: A subtle vertical drift (`±10px-20px`) for hero assets.
- **`drift`**: Background orbs that move very slowly in the background.
- **`pulse`**: Glow intensity changes (0.4 to 0.9 opacity) on active icons.

---

## 7. Interactive Elements
- **Buttons**:
  - `btn-primary`: Orange background, black text. Requires a `box-shadow` of `rgba(255, 150, 83, 0.6)`.
  - `btn-outline`: Transparent, orange border.
- **Forms**:
  - Focused inputs must have a **Blue** (`#5FCAFF`) glow and a `2px` inset box shadow.

---

## 8. Integration Architecture (Lead Flow)
- **Data Capture**: Standard POST to an n8n webhook.
- **Lead Enrichment**: Cross-correlated via Supabase `leads` table.

Built for founders by EkaFlow. MSME Registered.
