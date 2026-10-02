# Persel Group: adapted design direction

Working visual specification derived from supplied Vanta reference files, Persel homepage screenshot, strategy PDF and explicit typography instructions. This supersedes the Vanta design rules for the Persel implementation. Content order is governed by content-brief.md.

## Character

An editorial executive advisory site: confident display typography, spacious composition, restrained color, real people and clear audience paths. Borrow Vanta's hierarchy, section rhythm, photography arrangements and simple bordered surfaces. Adapt the layouts to Persel's content lengths and service model.

The supplied screenshots are the composition reference. The Refero Markdown contains interpreted measurements and homepage-centric rules; it is not source code. Its prohibition on photography conflicts with the About/Careers screenshots and the user's request. This specification resolves that conflict in favor of photography.

## Reference translation

| Vanta element | Persel adaptation |
|---|---|
| Centered display hero and large visual | Short strategic headline, two audience CTAs, editorial image |
| Violet hero wash | Pale light-blue hero surface |
| Violet filled buttons | Navy filled controls; orange reserved for selected emphasis |
| Product feature grid | Audience-grouped service cards with descriptors and meaningful photos |
| Large product dashboard | Leadership/advisory photography; no simulated product UI |
| About history split | Persel story, perspective and verified founder information |
| Careers photo with overlapping text panel | Suitable editorial split for advisor expertise or service explanation |
| Dark audience/proof bands | Deep-navy Why Persel/proof sections where useful |
| Portrait proof cards | Actual approved testimonial or engagement evidence |
| Globe, investor logos, compliance badges | Include only relevant, verified Persel material; none by default |
| Email capture / demo / login / chat widget | Audience navigation and approved inquiry/booking actions |

Do not import Vanta's product copy, mascots, violet palette, neon green About-page accents, decorative compliance widgets, invented trust marks or SaaS navigation.

## Colors

Exact original CSS colors could not be retrieved. The compressed screenshot's dominant dark surface is approximately #2B2D41; lighter sections are approximately #EDF1F4 and #E9EDF0; the accent family visually reads coral orange and cyan blue. These are observations, not authoritative brand values.

The following refined palette is proposed for implementation review, preserving navy, blue and orange identities:

| Token | Proposed value | Role |
|---|---|---|
| --color-navy | #202638 | Headings, primary buttons, dark bands |
| --color-navy-deep | #171D2B | Footer, darker anchors |
| --color-blue | #087E9A | Links, focus treatment, selected accents |
| --color-blue-light | #CFEAF1 | Light-blue feature surfaces |
| --color-blue-wash | #E9F3F6 | Hero/background tint |
| --color-orange | #EE8567 | Accent lines, small highlights, limited CTA band |
| --color-orange-wash | #FBEAE3 | Subtle warm panels |
| --color-canvas | #F7F8F7 | Main light canvas |
| --color-white | #FFFFFF | Cards, inverse text |
| --color-text | #202638 | Main light-surface text |
| --color-text-muted | #515D6A | Supporting copy |
| --color-border | #D8DFE3 | Quiet dividers and card borders |

Use navy text on orange and pale-blue surfaces. Orange is not a small-text color on white. Blue links require contrast verification for actual size/weight. Dark bands use white main text and a tested muted light color. Ensure 4.5:1 contrast for ordinary text, 3:1 for large text and applicable non-text controls. Never treat the palette proposal as extraction of the existing site's exact tokens.

Prefer large calm light surfaces with selective navy sections. Avoid the old repeated navy-to-cyan gradient title bars. Color should mark hierarchy or section purpose rather than decorate every block. Do not give one audience stronger priority simply through larger buttons or more space.

## Typography

User-selected final families: Fraunces for headings; Work Sans for body, supportive text and UI. Replace every reference to SC Ripley, Soehne, Reckless and Inter in the implementation design rules.

Use locally supplied webfont files when available. Inspect their actual metadata and weight ranges before configuring font faces. If files are absent, use a framework-supported Google Fonts integration when the build can fetch it; record that dependency. Do not silently ship system-font fallbacks as final typography. Prevent synthetic bold/italic when those styles are unavailable.

Recommended starting settings: Fraunces regular or medium, roman, restrained display treatment; Work Sans regular and medium, semibold only where useful. If variable Fraunces files provide optical-size, softness and wonk axes, inspect the file first and tune with actual copy. Do not assume every supplied file has every axis. Avoid overtly playful display styling.

| Role | Font | Desktop starting size | Mobile starting size | Leading |
|---|---|---|---|---|
| Hero | Fraunces | 64-80px | 40-48px | 1.05-1.12 |
| Section heading | Fraunces | 40-52px | 30-36px | 1.12-1.20 |
| Card heading | Fraunces | 26-32px | 24-28px | 1.18-1.25 |
| Lead body | Work Sans | 20px | 18px | 1.5 |
| Body | Work Sans | 17-18px | 16-18px | 1.55-1.65 |
| Navigation/button | Work Sans | 14-16px | 16px | 1.3-1.5 |
| Caption/eyebrow | Work Sans | 12-14px | 12-14px | 1.4 |

Use fluid sizing and a 1rem body floor. Heading tracking starts near -0.015em and must be adjusted visually; do not mechanically reuse Reckless's pixel tracking. Body tracking starts normal. Keep body lines around 55-70 characters. Hero copy may wrap to 2-3 lines. Avoid forced line breaks that damage mobile composition. Use Fraunces for meaningful headings throughout, not only page titles.

## Layout and rhythm

Centered maximum content width: 1200px as a starting point. Desktop gutters 40-64px, tablet 32px, mobile 20-24px. Base spacing 8px with 16, 24, 32, 40, 48, 64, 80, 104 and 128px steps.

Section padding: 88-112px desktop, 64-80px tablet, 48-64px mobile. Card padding: 28-32px desktop, 24px mobile. Gaps: 24-32px. Two audience cards share width and visual importance. Company service grid: two columns; executive service grid: two or four columns when readable. Stack at mobile. Avoid a generic six-card grid before visitors choose an audience.

Alternate editorial arrangements: centered intro; large image; split copy/photo; compact metrics; evidence cards; closing action band. Preserve strategy order. Do not replicate Vanta's entire homepage section inventory.

## Components

Header: supplied Persel logo, readable service groups, About and booking action. Sticky only if useful; light solid surface on scroll. Mobile menu supports keyboard access, visible close control and appropriate focus behavior. Never recreate the logo as plain text when an original asset exists.

Hero: strategy headline, concise description, equally clear audience CTAs. Light-blue field is the default proposed direction. A strategic text-first hero and image below can use Vanta's centered composition; a split hero is acceptable if photography supports it. Do not reduce the strategy headline to accommodate decorative imagery.

Buttons: pill shape, minimum 44px interactive height, 20-24px horizontal padding. Navy fill/white text for main action on light surfaces; outline secondary where appropriate. On dark surfaces use pale blue or orange with navy text. Hover should be subtle; keyboard focus must be visible. Arrow icons are optional navigational cues, not mandatory decoration.

Audience cards: 16px radius, substantial heading, one-sentence purpose, correctly grouped service descriptors and a visible route. Use a navy company card and pale-blue executive card as a starting proposal; stacking order follows reading order. Keep comparable emphasis. Make embedded link behavior explicit rather than nesting interactive controls.

Service cards: 16px radius, quiet 1px border, no heavy shadows. Plain descriptor close to branded name. Photography may sit below text. Avoid miniature product mockups and arbitrary icons added merely to fill space.

Proof: metrics with exact labels, followed by genuine engagement stories or approved quotes. No animated fabricated counters. Do not present empty proof cards as final content. A dark-navy band may provide a visual anchor.

Expertise: image/text split, concise verified bio, methodology summary and relevant link. Keep headshots proportional and avoid excessive circular portrait carousels when there is only one verified advisor.

Forms: Work Sans labels above fields, 8-12px field radius and 16px textarea radius; buttons remain pill-shaped. The Vanta requirement for pill-shaped inputs is replaced for usable multiline/contact forms. Minimum readable 16px field text. Display actual validation and submission state.

Footer: concise confirmed navigation and contact/legal information. Do not copy Vanta's sprawling product footer. Closing CTA supports both audience paths.

## Photography

Use authentic leadership, advisor, meeting and portrait assets appropriate to Persel. Request founder imagery and real assets first. Temporary stock images must be clearly identified in the asset inventory; stock people must never be labeled as staff or clients. No generated identity or testimonial imagery unless explicitly requested.

Visual treatment: natural light, considered business environments, relaxed confident expressions, consistent restrained color grading, sufficient negative space. Avoid staged handshakes, generic smiling boardroom stock and heavy blue overlays.

Suggested aspect ratios: hero 16:9 or 3:2; split images 4:3; advisor portraits 3:4. Specify focal points per asset. Use responsive crops; never crop faces behind text. Give meaningful image alt text and empty alt text for purely decorative imagery. Allocate image space to avoid layout shifts.

## Responsive behavior and motion

Verify at 390, 768 and 1440px plus a 320px overflow check. Stack split sections and cards cleanly. Preserve readable headings and both hero actions. Replace desktop dropdown navigation with accessible mobile controls. No carousels required unless content justifies them.

Use short 150-250ms interactive transitions. Optional restrained section entrances must respect reduced motion. No scroll hijacking, autoplay background video or elaborate dashboard animation.

## CSS token starter

```css
:root {
  --color-navy: #202638;
  --color-navy-deep: #171D2B;
  --color-blue: #087E9A;
  --color-blue-light: #CFEAF1;
  --color-blue-wash: #E9F3F6;
  --color-orange: #EE8567;
  --color-orange-wash: #FBEAE3;
  --color-canvas: #F7F8F7;
  --color-white: #FFFFFF;
  --color-text: #202638;
  --color-text-muted: #515D6A;
  --color-border: #D8DFE3;
  --font-heading: 'Fraunces', Georgia, serif;
  --font-body: 'Work Sans', Arial, sans-serif;
  --page-max-width: 1200px;
  --radius-card: 16px;
  --radius-input: 10px;
  --radius-button: 999px;
}
```

These family names are conceptual tokens. Bind them to the actual local/framework font variables in the build. Do not overwrite a framework font loader's generated variables with hard-coded names that bypass it.

## Visual acceptance

Fraunces and Work Sans actually load. Both audience paths are obvious. Photography replaces SaaS visualizations. Navy, light blue and orange remain recognizable. No Vanta purple/green remnants or SaaS copy remain. Spacing supports actual content. Text and interactive states pass contrast checks. Desktop and mobile screenshots are reviewed in the real browser before calling the page finished.
