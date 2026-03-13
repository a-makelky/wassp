# WASSP Visual Brand Audit

Date: March 13, 2026

This document is a current-state audit of the visual branding used by the Wyoming Association of Secondary School Principals (WASSP). It documents what is live today and what appears in the supplied logo files without forcing a canonical system.

Legend:
- `Confirmed`: directly supported by source code, markup, or the supplied asset file.
- `Observed`: visually present in the supplied asset or live page, but not fully specified in code.
- `Inferred`: a reasoned conclusion based on repeated patterns.

## Brand Snapshot

- `Confirmed`: The live site uses a custom SmartSites/ParentSquare skin that consistently applies a dark brown and gold palette with `Poppins` as the primary production typeface. Evidence: [homepage](https://www.wassp.org/), [custom stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Observed`: The supplied local logos are richer and more illustrative than the live site, with leather browns, metallic gold, and a more traditional wordmark treatment. Evidence: [wassp letterhead.png](<wassp letterhead.png>), [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Confirmed`: The live header currently uses only the boot-and-hat icon, not the full organization name inside the logo asset itself. Evidence: [homepage](https://www.wassp.org/), [site header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png).
- `Inferred`: WASSP already has a recognizable Western visual identity, but it does not yet have a single normalized brand system spanning print-style logo art, website chrome, and interface components.

## Source Inventory

| Source | Type | Notes |
| --- | --- | --- |
| [wassp letterhead.png](<wassp letterhead.png>) | Local asset | Circular/stacked emblem treatment with boot, hat, spur, and gold lettering. |
| [wassp horizontal logo.png](<wassp horizontal logo.png>) | Local asset | Horizontal wordmark with full association name and icon. |
| [WASSP Homepage](https://www.wassp.org/) | Live page | Primary reference for header, homepage hero, nav, footer, and live site token usage. |
| [About](https://www.wassp.org/47069_2) | Live page | Reference for internal page title and column layout treatment. |
| [Contact](https://www.wassp.org/13572_1) | Live page | Reference for form controls, social icon treatment, and CTA usage. |
| [Conferences](https://www.wassp.org/13565_1) | Live page | Reference for alternate hero/video usage and stacked content modules. |
| [Custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | CSS source | Main source for WASSP-specific colors, typography, and button/nav overrides. |
| [Live header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png) | Remote asset | Flat brown icon-only web logo used in the site header. |

## Logos

### 1. Letterhead mark

![WASSP letterhead mark](<wassp letterhead.png>)

- `Observed`: This asset is built as a vertically centered emblem: curved `WASSP` text above, `Wyoming` below, and a detailed cowboy boot, hat, and spur in the middle. Evidence: [wassp letterhead.png](<wassp letterhead.png>).
- `Observed`: It uses a black field as provided, metallic-gold lettering, brown leather shading, and silver spur hardware. The mark reads more like a crest, seal, or print graphic than a lightweight UI logo. Evidence: [wassp letterhead.png](<wassp letterhead.png>).
- `Confirmed`: The supplied file is high-detail and portrait-oriented at 1152 x 1472 px, which makes it visually rich but less flexible for tight horizontal spaces. Evidence: local file metadata for [wassp letterhead.png](<wassp letterhead.png>).
- `Inferred`: This is likely strongest for stationery, merchandise, or commemorative graphics rather than a website masthead or compact social avatar.

### 2. Horizontal wordmark

![WASSP horizontal logo](<wassp horizontal logo.png>)

- `Observed`: This treatment pairs a serif `WASSP` wordmark with the spelled-out association name beneath it and a boot-and-hat icon on the right. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Observed`: It feels more institutional and legible than the letterhead mark because it includes the organization name in a standard horizontal lockup. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Observed`: The wordmark color is a warm orange-brown rather than the exact brown-and-gold pairing seen on the website. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: The supplied file is compact and landscape-oriented at 488 x 214 px, which makes it the most naturally adaptable of the two local assets for documents, banners, and email signatures. Evidence: local file metadata for [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Inferred`: If WASSP eventually standardizes a primary logo, this layout is the closest current candidate because it preserves both the iconography and the full association name in one mark.

### 3. Live website header logo

- `Confirmed`: The live site header uses a standalone icon-only asset, not the full horizontal lockup. Evidence: [homepage](https://www.wassp.org/), [site header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png).
- `Observed`: The icon is a simplified brown silhouette of the boot and hat, without the gold lettering, subtitle, or richer leather detail present in the supplied local files. Evidence: [site header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png), [wassp horizontal logo.png](<wassp horizontal logo.png>), [wassp letterhead.png](<wassp letterhead.png>).
- `Confirmed`: The live web asset is wide and transparent at 1200 x 350 px, but the visible graphic occupies only the right side of the image area, effectively behaving like an icon rather than a balanced logo lockup. Evidence: [site header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png).
- `Inferred`: The website prioritizes symbolic recognition over full-name clarity, relying on navigation, footer text, and accessibility labels to carry the organization name.

### Logo conflicts worth keeping visible

- `Confirmed`: There are at least three active WASSP logo treatments: the emblematic letterhead mark, the horizontal wordmark, and the icon-only live header mark. Evidence: [wassp letterhead.png](<wassp letterhead.png>), [wassp horizontal logo.png](<wassp horizontal logo.png>), [homepage](https://www.wassp.org/).
- `Observed`: The live site uses the simplified icon treatment while the strongest full-name identifier exists only in the supplied horizontal logo file. Evidence: [homepage](https://www.wassp.org/), [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Inferred`: The logo system currently behaves as a collection of related marks, not a documented hierarchy with approved primary, secondary, and tertiary usage rules.

## Color System

### Core web palette currently in use

| Swatch | Token | Status | Evidence | Current use | Notes |
| --- | --- | --- | --- | --- | --- |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#492F24;border:1px solid #999;"></span> | `#492F24` | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | Navbar background, footer background, link color, primary button styling, alert modal button | Closest thing to a primary brand color on the live website. |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#9C7129;border:1px solid #999;"></span> | `#9C7129` | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | Link hover, nav hover/active, dropdown hover, several button variants, active list states | Functions as the main accent/highlight color. |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#FCBF2C;border:1px solid #999;"></span> | `#FCBF2C` | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | Animated CTA buttons in featured-video modules, `.btn-danger` remap | Brightest site accent; reads as highlight gold rather than warning red. |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#333333;border:1px solid #999;"></span> | `#333333` | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | Body text, page titles, some labels, dark text on light surfaces | Core text color on the site. |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#FFFFFF;border:1px solid #999;"></span> | `#FFFFFF` | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) | Nav text, footer text, button text, white content wells | Primary contrast color. |
| <span style="display:inline-block;width:1.25em;height:1.25em;background:#545454;border:1px solid #999;"></span> | `#545454` | `Confirmed` | [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css), [Contact](https://www.wassp.org/13572_1) | `.btn-warning` background, including the live contact form submit button | Reads more neutral/charcoal than branded. |

### Logo-only or logo-heavy color variation

- `Observed`: The horizontal logo introduces an orange-brown wordmark tone that is warmer than the website's gold accent and slightly lighter than the site's main brown. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Observed`: The letterhead logo introduces a much broader illustrative palette: metallic gold lettering, black hat/background, leather tan and caramel boot tones, and silver spur detail. Evidence: [wassp letterhead.png](<wassp letterhead.png>).
- `Inferred`: The print-style art direction is broader and more textured than the live web palette, which currently behaves more like a restrained institutional brown/gold UI system.

### Colors that appear to be platform or inherited defaults

- `Confirmed`: `#337ab7`, `#5cb85c`, and `#d9534f` are present in the source, but they appear in generic SmartSites/Bootstrap/admin or utility contexts rather than as stable WASSP brand colors. Evidence: [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Inferred`: These should not be treated as WASSP palette tokens in any future canonical guide unless the organization explicitly chooses to adopt them.

## Typography

### What is confirmed on the live website

- `Confirmed`: The homepage explicitly loads Google Fonts for `Poppins` and `Poppins:700`. Evidence: [homepage](https://www.wassp.org/).
- `Confirmed`: The custom stylesheet sets `body` to `font-family: Poppins, sans-serif`. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: Navigation links, quick links, buttons, page titles, and footer typography are all restyled to use `Poppins`. Evidence: [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: The site uses bold `Poppins` for stronger hierarchy in the footer heading, site title, some navigation states, and module headers. Evidence: [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).

### Current type roles

| Role | Current treatment | Status | Evidence |
| --- | --- | --- | --- |
| Body copy | `Poppins`, 16px baseline | `Confirmed` | [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) |
| Primary nav | `Poppins`, 16px, white on brown, gold active/hover state | `Confirmed` | [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) |
| Page titles | `Poppins`, 28px, dark gray | `Confirmed` | [About](https://www.wassp.org/47069_2), [Contact](https://www.wassp.org/13572_1), [Conferences](https://www.wassp.org/13565_1), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) |
| Footer heading | `Poppins`, 700 weight, 20px, white | `Confirmed` | [homepage](https://www.wassp.org/), inline footer styles |
| Buttons | `Poppins`, mostly 16px to 18px depending on component | `Confirmed` | [homepage](https://www.wassp.org/), [Conferences](https://www.wassp.org/13565_1), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css) |
| Platform fallback | `"proxima-nova", "proxima nova", "Helvetica Neue", Helvetica, Arial, sans-serif` in `.psq_font` helper class | `Confirmed` | [homepage](https://www.wassp.org/) |

### Logo lettering vs website typography

- `Observed`: The horizontal logo uses a classic serif display style for `WASSP`, while the subtitle beneath it is a more neutral sans serif. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>).
- `Observed`: The letterhead mark uses stylized gold lettering as part of an illustrative composition rather than as a reusable text system. Evidence: [wassp letterhead.png](<wassp letterhead.png>).
- `Inferred`: WASSP currently presents itself with a modern sans serif on the web and a more traditional/logo-art voice in its supplied mark files. That split is not inherently wrong, but it is not yet documented as an intentional typography system.

## UI Components

### Navigation

- `Confirmed`: The main nav uses a deep brown background with white text and gold hover/active states. Evidence: [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: Dropdown menus inherit the same brown-and-gold scheme, with brown menu surfaces and gold hover/active treatment. Evidence: [homepage](https://www.wassp.org/), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: The nav also references a background image asset in addition to the brown fill, suggesting an ornamental or textured layer even though access to the image asset itself is restricted. Evidence: [homepage](https://www.wassp.org/), inline nav CSS.
- `Observed`: Quick links sit above the primary nav and repeat key actions such as Home, About Us, Board of Directors, and Contact. Evidence: [homepage](https://www.wassp.org/).

### Buttons and CTA logic

- `Confirmed`: Bootstrap semantic button classes have been remapped into WASSP colors rather than their default meanings. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: `.btn-success` is dark brown with white text, which makes it feel like the site's practical primary CTA style. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: `.btn-primary`, `.btn-info`, and `.btn-default` are all assigned the same gold family rather than clearly distinct button roles. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: `.btn-danger` is reassigned to bright gold with black text, so the semantic label no longer matches the visual meaning. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: `.btn-warning` is charcoal `#545454` with white text, and the live contact form submit button uses `btn btn-warning`, resulting in a neutral rather than brand-forward CTA. Evidence: [Contact](https://www.wassp.org/13572_1), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Confirmed`: Buttons receive a darkening overlay on hover via inset box shadow, which creates a consistent interaction cue across variants. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Observed`: Featured-video modules use a brighter gold animated button with brown text and brown stroke, which reads more intentionally branded than some of the generic Bootstrap button mappings. Evidence: [homepage](https://www.wassp.org/), [Conferences](https://www.wassp.org/13565_1).

### Forms

- `Observed`: Form inputs on the Contact page remain largely standard Bootstrap `form-control` fields inside a white content well. Evidence: [Contact](https://www.wassp.org/13572_1).
- `Inferred`: The visual branding of forms currently depends more on surrounding layout, typography, and the submit button than on heavily customized input styling.

### Media and controls

- `Confirmed`: The homepage and Conferences page both use a featured-video component with autoplay media and branded text/CTA styling layered around it. Evidence: [homepage](https://www.wassp.org/), [Conferences](https://www.wassp.org/13565_1).
- `Observed`: Video play, pause, and mute controls are black circles with white glyphs, which read as platform defaults rather than brand-specific components. Evidence: [homepage](https://www.wassp.org/), [Conferences](https://www.wassp.org/13565_1).

### Footer and social elements

- `Confirmed`: The footer uses dark brown as its base, white text, white icon strokes, and `Poppins` for both label and body text. Evidence: [homepage](https://www.wassp.org/).
- `Observed`: The Contact page uses circular social icon styling for Facebook, which visually aligns with the broader institutional tone but is more generic than distinctive. Evidence: [Contact](https://www.wassp.org/13572_1).

## Layout Patterns

### Header and top-of-page structure

- `Confirmed`: The site header is built in layers: logo area first, quick links next, and primary navigation below. Evidence: [homepage](https://www.wassp.org/).
- `Observed`: The header is highly customized with repeated breakpoint-specific logo spacing rules and utility-link duplication across screen sizes. Evidence: [homepage](https://www.wassp.org/), inline responsive CSS.
- `Inferred`: The visual hierarchy is clear to users, but the implementation is brittle and manually tuned rather than elegantly systematized.

### Homepage pattern

- `Confirmed`: The homepage opens with a full-width featured-video hero directly beneath the navigation. Evidence: [homepage](https://www.wassp.org/).
- `Observed`: The hero currently emphasizes atmosphere and motion more than messaging because the text container is effectively empty while the video carries the visual weight. Evidence: [homepage](https://www.wassp.org/).

### Internal page pattern

- `Confirmed`: Internal pages such as About and Conferences use a visible `page_title` heading followed by stacked content sections, often in column-based layouts. Evidence: [About](https://www.wassp.org/47069_2), [Conferences](https://www.wassp.org/13565_1).
- `Observed`: These layouts feel like SmartSites content modules that have been recolored and typographically aligned, rather than custom page templates built from a bespoke WASSP design system. Evidence: [About](https://www.wassp.org/47069_2), [Conferences](https://www.wassp.org/13565_1).

### Contact page pattern

- `Confirmed`: The Contact page pairs organization/address information and social links with a structured inquiry form in a single wide module. Evidence: [Contact](https://www.wassp.org/13572_1).
- `Observed`: This is the clearest example of a practical, member-facing page pattern and is a strong reference for documenting forms, spacing, and CTA behavior. Evidence: [Contact](https://www.wassp.org/13572_1).

### Footer pattern

- `Confirmed`: The footer combines association name, address, phone, Facebook, important links, utility links, and platform/legal messaging in a wide multi-column composition. Evidence: [homepage](https://www.wassp.org/).
- `Observed`: The footer is one of the most complete branded areas on the site because color, typography, content hierarchy, and social links all align more consistently there than in some mid-page components. Evidence: [homepage](https://www.wassp.org/).

## Imagery and Iconography

- `Observed`: The core iconography is distinctly Western: cowboy boot, hat, and spur. Evidence: [wassp letterhead.png](<wassp letterhead.png>), [wassp horizontal logo.png](<wassp horizontal logo.png>), [site header logo asset](https://files.smartsites.parentsquare.com/4229/design_img__j3ovp3.png).
- `Observed`: The logo art carries the most explicit personality in the brand system; the website UI itself is more restrained and institutional. Evidence: local logo files and [homepage](https://www.wassp.org/).
- `Confirmed`: Font Awesome and platform icon sets are used for search, social, alerts, and utility interactions. Evidence: [homepage](https://www.wassp.org/).
- `Confirmed`: Motion is part of the current website brand presentation through autoplay featured-video sections on key pages. Evidence: [homepage](https://www.wassp.org/), [Conferences](https://www.wassp.org/13565_1).
- `Inferred`: The strongest WASSP personality comes from Western symbolism plus association-level professionalism, not from experimental web interaction patterns.

## Brand Gaps

- `Confirmed`: There is no single visible primary logo standard across the supplied assets and live website. Evidence: [wassp letterhead.png](<wassp letterhead.png>), [wassp horizontal logo.png](<wassp horizontal logo.png>), [homepage](https://www.wassp.org/).
- `Confirmed`: The live site is missing a branded favicon and branded open-graph share image; it currently uses platform defaults. Evidence: [homepage](https://www.wassp.org/).
- `Observed`: The site header logo image uses an empty `alt` attribute, relying on the surrounding link label rather than the image itself to communicate identity. Evidence: [homepage](https://www.wassp.org/).
- `Confirmed`: Button semantics are visually inconsistent because Bootstrap class names no longer map cleanly to role or urgency after the custom color remaps. Evidence: [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css), [Contact](https://www.wassp.org/13572_1).
- `Observed`: The contact form's live CTA is charcoal instead of brown or gold, which weakens the visual hierarchy of a key engagement action. Evidence: [Contact](https://www.wassp.org/13572_1), [custom site stylesheet](https://files.smartsites.parentsquare.com/4229/css2656.css).
- `Observed`: Responsive header behavior appears to rely on many one-off margin and size adjustments for `.site_logo`, which suggests the logo system is not yet dimensionally standardized for the web. Evidence: [homepage](https://www.wassp.org/), inline responsive CSS.
- `Observed`: The brand relationship between the traditional serif logo wordmark and the modern `Poppins` web system is not documented, so the current mix can look intentional in places and accidental in others. Evidence: [wassp horizontal logo.png](<wassp horizontal logo.png>), [homepage](https://www.wassp.org/).
- `Inferred`: WASSP has enough distinct material to build a strong brand guide, but it needs an explicit decision layer above the current asset set.

## Next Decisions

- Choose a canonical primary logo lockup and explicitly define approved alternates for web header, print, merchandise, and social use.
- Decide whether the web's brown-and-gold palette or the richer logo-art palette should become the master color system.
- Define how the serif logo voice should relate to the `Poppins` web system, especially for headlines, printed materials, and branded documents.
- Standardize button hierarchy by role instead of inheriting Bootstrap semantic class names.
- Replace the default favicon and default social share image with WASSP-branded assets.
- Simplify responsive header behavior once the canonical web logo size and clear-space rules are chosen.

