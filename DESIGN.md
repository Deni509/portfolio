---
name: Denizard François Portfolio
description: A sculptural digital atelier for a bilingual freelance developer portfolio.
colors:
  charcoal: "#131311"
  paper: "#eeece5"
  secondary: "#b4b3aa"
  copper: "#e1a87e"
  divider: "#3c3b35"
  contact-ink: "#211b15"
typography:
  display:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(52px, 6.4vw, 96px)"
    fontWeight: 500
    lineHeight: 1.08
    letterSpacing: "-0.04em"
  headline:
    fontFamily: "Space Grotesk, sans-serif"
    fontSize: "clamp(32px, 3.6vw, 54px)"
    fontWeight: 500
    lineHeight: 1.12
    letterSpacing: "-0.035em"
  body:
    fontFamily: "Manrope, sans-serif"
    fontSize: "16px"
    lineHeight: 1.65
  label:
    fontFamily: "Manrope, sans-serif"
    fontSize: "11px"
rounded:
  window: "12px"
  pill: "50px"
  circle: "50%"
spacing:
  gutter: "5.5%"
  section: "110px"
  section-mobile: "65px"
components:
  button-primary:
    backgroundColor: "{colors.contact-ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.pill}"
    padding: "16px 24px"
  language-selector:
    backgroundColor: "transparent"
    textColor: "{colors.paper}"
    rounded: "{rounded.circle}"
    width: "54px"
    height: "42px"
---

# Design System: Denizard François Portfolio

## Overview

**Creative North Star: "The Sculptural Digital Atelier"**

Warm charcoal frames a living copper mathematical knot. Large, closely tracked typography and generous editorial spacing connect expressive interface work with engineering precision. Native text, links and disclosure controls remain the functional foundation around the decorative canvas.

The system supports Spanish and English without changing its visual identity. Work presentations have distinct material palettes, while the surrounding portfolio retains a quiet charcoal, paper and copper rhythm.

**Key Characteristics:**
- Sculptural copper geometry on warm charcoal.
- Large geometric display type paired with restrained humanist body text.
- Full-width project artwork, open information rows and thin dividers.
- Motion that can be paused and respects reduced motion.

## Colors

### Primary

**Copper** gives the knot, highlighted headline, monogram, disclosure symbols and contact section their warmth. It is the portfolio's signature accent.

### Neutral

**Charcoal** grounds the header, hero, approach section and footer. **Paper** provides the main light text and the inverted work-section surface. **Secondary** supports descriptions and metadata on charcoal. **Divider** separates the dark surfaces without raised panels. **Contact ink** provides readable text and the primary action against copper.

**The Material Context Rule.** Project artwork may use its own green, sage or terracotta presentation palette; those artwork colors do not replace the portfolio's shared interface tokens.

## Typography

**Display Font:** Space Grotesk with sans-serif fallback.

**Body Font:** Manrope with sans-serif fallback.

Display headings use medium weight and tight tracking. Body text is quiet, spacious and readable, with short labels supporting the editorial hierarchy.

- **Display:** The frontmatter defines the desktop hero. At the mobile breakpoint it becomes `clamp(45px, 8.8vw, 67px)` with line height (1.1).
- **Headline:** Section headings use the frontmatter headline role. Project titles use medium display type (32px), falling to (28px) on mobile.
- **Body:** The frontmatter defines the base. Project descriptions use (14px), or (13px) on mobile, with a maximum width of (650px). The approach lead uses (22px), or (19px) on mobile.
- **Label:** Shared metadata finishes at (11px) on both desktop and mobile after the legibility overrides. The artwork's small heading is (10px) on mobile. Navigation is (13px), or (11px) on mobile; primary action text is (12px).

**The Legible Metadata Rule.** Preserve the final shared label sizing overrides; earlier compact artwork and mobile declarations are not the final rendered values.

## Layout

The shared outer gutter is defined in frontmatter. Header height is (94px). The hero uses `calc(100svh - 94px)` with a minimum height of (760px) and maximum of (1100px). Its text anchors near the bottom, leaving the upper-right area to the knot. The work section uses full-width artwork followed by open title, description and link rows. The approach section uses two equal columns with a (12%) gap.

At viewport widths up to (760px), the header becomes (78px), the hero becomes `calc(100svh - 78px)` with a (690px) minimum, section spacing uses the mobile token, and project information, approach content and contact details stack. Navigation remains visible. The hero action moves below the introduction. Artwork retains its own responsive composition rather than being cropped into a generic card.

At widths from (1600px), header, footer and ordinary sections use `max(5.5%, calc((100vw - 1440px)/2))` side padding. Hero gutters retain (5.5%). Do not claim a universal fixed-width container.

## Elevation & Depth

Most of the interface is flat. Alternating surface colors, typography and dividers define structure. Depth belongs to the artwork: a perspective-tilted AJAX window and the layered translucent strokes of the canvas knot. The application window has an ambient shadow (`0 28px 65px -20px #17251c55`) and straightens on hover. Standard content rows do not inherit this shadow.

## Shapes

Artwork containers and editorial sections have square edges. Rounded forms are reserved for the application window, its small internal demonstration elements, the pill contact action, circular arrow controls and the oval language selector. The displayed knot is an ornamental mathematical form rather than a container or navigation target.

## Components

### Primary action

A compact, dark pill on the copper contact surface. Its padding and colors are normative in frontmatter. Hover shifts its background to warm brown (`#4d3829`) over (0.3s). Shared keyboard focus uses a copper outline (2px) with (7px) offset.

### Navigation and text links

Simple text without a surrounding panel. Hover reveals a one-pixel underline from the left over (0.4s). The language selector is an outlined oval with a transparent background; hover inverts to paper with charcoal text. It becomes (43px) wide and (35px) high on mobile. The selected language persists locally and updates the document language.

### Project presentation

Large artwork with a separate information row rather than an enclosing card. Tags are plain inline labels without filled chips. Linked artwork has a paper circular arrow that rotates on hover. AJAX and ANACAPTEC artwork carry their conceptual presentation labels; keep those labels visually readable.

### Service disclosures

Native details and summary controls use horizontal dividers, an open text layout and a copper plus/minus marker. Expanded explanatory copy stays in secondary text. No custom modal or form styling is established.

### Signature mathematical knot

A decorative canvas renders 56 copper loops with perspective and restrained pointer response. Its resolution multiplier is capped at (1.7). Composition changes below canvas width (760px); this is a strict less-than check, while the CSS mobile layout includes (760px).

The hero copy arrives with a clipped reveal and vertical movement over (1s), using `cubic-bezier(.16,1,.3,1)`. The canvas has an explicit pause/play control. It starts paused for reduced motion, stops when offscreen or the document becomes hidden, and restarts when eligible. Reduced motion also removes CSS transitions and animations and disables smooth scrolling. Keep content available immediately, without a gated loader.

## Do's and Don'ts

### Do:
- **Do** keep the charcoal, paper and copper identity around project-specific artwork.
- **Do** retain native HTML content and controls around the decorative canvas.
- **Do** preserve the visible pause control and reduced-motion behavior.
- **Do** verify both language versions at the mobile breakpoint.
- **Do** retain the final legibility overrides for metadata.

### Don't:
- **Don't** spread the artwork window shadow to ordinary content rows.
- **Don't** replace open project presentations with generic rounded cards.
- **Don't** gate content behind a loading animation.
- **Don't** imply conceptual artwork is a product screenshot.

## Portrait hero update
The owner portrait now occupies the lower right of the hero with transparent background, a charcoal tonal treatment and bottom fade. The live copper sculpture sits above the portrait (z-index -1 versus -2) while heading and controls sit in front at z-index 2/3. Desktop copy occupies the left area; mobile places copy first and portrait beneath. The old about-section portrait card is removed. Original supplied photo is retained separately.

