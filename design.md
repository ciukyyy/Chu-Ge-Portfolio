# Vibe coding Personal Website Design Specification (design.md)

## 1. Vision & Concept Definition

### Core Concept: "Corkboard & Interactive Desk Collage" (毛 felt/软木告示板复古贴纸风格)
This design breaks away from conventional grid-based personal websites by creating a warm, tactile, hands-on physical desktop environment. The canvas represents a real corkboard/felt board pinning board featuring interactive objects (ID cards, Polaroid photos, post-it notes, tickets, stickers, instant cameras) that serve as navigational entry points to different sections of the portfolio.

---

## 2. Visual Style & Aesthetic System

### 2.1 Background & Textures
- **Main Canvas Background**: Soft corkboard texture / warm beige felt (`#D5C2AD` to `#C8B49C`), giving an organic, physical felt texture with soft shadows.
- **Sub-panels / Shelf**: Light grey/oatmeal felt panel (`#E3DFD8`) mounted with subtle inner shadows and rounded corners (border-radius: 16px).

### 2.2 Typography
- **Handwritten / Sketch Annotations**: Script/Doodle style font (e.g., *Caveat*, *Indie Flower*, or custom SVG path text) for directional arrows and labels like `about me (click)`, `my photography (click)`, `little notes (click)`.
- **System / Formal Text**: Clean sans-serif (`Inter`, `Helvetica Neue`, `PingFang SC`) for structured document areas (like the Creative License ID card).
- **Type Colors**: Charcoal/Dark Graphite (`#2B2B2B`), Sepia/Warm Brown (`#4A3E3B`), Off-white (`#FBF9F5`).

### 2.3 Color Palette
- **Base Background**: Cream / Linen Beige (`#EFECE6`, `#D8CBBC`)
- **Accent Red / Coral**: Retro Cherry (`#E63946`, `#C0392B`)
- **Accent Yellow / Ticket**: Warm Ochre / Vintage Yellow (`#F4A261`, `#E9C46A`)
- **Accent Teal / Mint**: Soft Turquoise (`#2A9D8F`, `#76C8B4`)
- **Dark Neutral**: Deep Charcoal (`#222222`)

### 2.4 Shadows, Rotations & Layering
- **Layer Depth**: Layered stacking using `z-index` and subtle CSS drop-shadows (`box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15)`).
- **Physical Realism**: Slight random tilts (`transform: rotate(-3deg)`, `rotate(4deg)`, `rotate(-8deg)`) applied to elements to simulate hand-pinned items.
- **Physical Pins/Clips**: Rendered push pins (black push pin, blue paper clip, red binder clip) holding items onto the board.

---

## 3. Interactive Component Map & Navigation Strategy

| Desktop Element | Visual Representation | Target Action / Link | Annotation Label |
| :--- | :--- | :--- | :--- |
| **ID Card** | "Creative License" with Avatar, Title, Badges | Opens Bio / "About Me" modal or page | `about me (click)` |
| **Gingham Note** | Yellow checkered Post-it with quote & push pin | Opens Blog / Thoughts / "Little Notes" | `little notes (click)` |
| **Polaroid Photo** | Instant print framed photo with "A moment ♡" | Contact / Social Links / "Find Me" | `find me (click)` |
| **Art Print / Sketch Sheet**| Red/white illustration paper clipped at top | Portfolio / Graphic & UI Design Showcase | `my design (click)` |
| **Instant Camera** | Retro Polaroid camera resting on felt shelf | Photography Gallery / Photo Albums | `my photography (click)` |
| **Apple Sticker with Ribbon**| Glossy red apple with lace ribbon sticker | Interactive Easter Egg / "Little Surprise" | `a little surprise (click)` |
| **Circus Tickets** | Stacked vintage tickets with decorative borders | Video Showcase / Motion Projects / Reel | `my videos (click)` |

---

## 4. Layout Architecture & Responsive Rules

### Desktop (Viewport > 1024px)
- **Absolute / Pinboard Free-Layout**: Elements are placed via responsive percentage offsets (`top`, `left`, `transform`) relative to a max-width container (e.g. 1100px × 800px) maintaining a fixed aspect ratio (16:10 or 4:3).

### Mobile / Tablet (Viewport < 768px)
- **Dynamic Re-stacking**: Converts into a dynamic vertical grid/board layout while preserving the rotated aesthetic and pin/clip details.
- Touch-friendly tap targets with subtle pop-out scaling (`transform: scale(1.05) rotate(0deg)` on touch/hover).

---

## 5. UI Hover & Micro-interactions
- **Hover Motion**: Hovering over any element applies a gentle hover lift (`transform: translateY(-6px) scale(1.03)`), increases drop-shadow density, and highlights the corresponding handwriting arrow tag.
- **Click Feedback**: Tactile click compression (`transform: scale(0.98)`).
- **Camera Flash Effect**: Clicking the Polaroid camera triggers a fast white screen flash and audio shutter effect (optional toggle).
