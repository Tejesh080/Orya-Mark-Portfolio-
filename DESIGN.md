# Orya Mark design system

Written from the built site, so every value below is in use. Direction: the Orya Mark
sunburst is the organising idea. Sun yellow, black and bone carry the studio. Client
colours are allowed to take over the page, and only there.

This direction comes from Orya Mark's own deck and logo. It was not benchmarked against
other agency sites.

## Colour

| Token | Value | Role |
|---|---|---|
| `--ink` | `#000000` | Hero, reel base, founders text on yellow, primary buttons |
| `--paper` | `#FFFFFF` | Text on black |
| `--sun` | `#FFC72C` | Brand colour. Entrance, contact section, enquiry page, action discs |
| `--oxblood` | `#360A0A` | Founders section, branding card, accent on yellow |
| `--bone` | `#F1E7D8` | Studio section, film card, text on oxblood |
| `--ember` | `#8A3410` | Small labels and accents on bone and on the enquiry card |
| `--card` | `#FFFAF0` | Enquiry card surface |
| `--well` | `#F3EADB` | Form fields and service tiles on the card |
| `--flare` | `#FF7A59` | Reserved. Error red on the card is `#A3210F` |

Live colours: `--bg`, `--fg` and `--ac` are set by script. In the reel they blend to the
colours of the client at the centre. Between sections they blend from one section's
palette to the next. Components read these three, never raw values.

Client colour pairs live in the `D` array in the script. Each pair must reach 4.5:1.
Case pages take their background, text and glow from the client's own brand palette.

The hero headline says what the studio does. The deck's tagline, "Your partner in
digital transformation", is the supporting line under it.

## Typography

| Role | Face | Use |
|---|---|---|
| Display | Gloock 400, tracking -0.02em, line height 0.98 | Headlines, client names, service statements, tile labels |
| Text | Anek Latin 400, 500, 600 | Body, labels, buttons, phone numbers |

Chopard from the deck is the intended display face if the licence is available.
Phone numbers are always Anek Latin 600 with tabular numerals, never the display face.

Scale (fluid, phone to desktop):

- Hero and enquiry headline: 2.7rem to 7rem
- Fitted lines ("Let's connect.", client names): sized by script to the container width
- Statement: 2.35rem to 6.4rem
- Service statement: 2rem to 5.1rem
- Founder name: 2.1rem to 4rem
- Body: 16px to 19px, line height 1.5
- Label (`.h2`): 1.05rem to 1.25rem, weight 500, in `--ac`
- Small: 0.88rem to 0.95rem

Sentence case everywhere. Client names keep the spelling from the deck.

## Spacing and layout

- Side gutter `--g`: 20px to 64px, and never below the phone safe area
- Section padding: 84px to 190px top and bottom
- Content width: 1500px, enquiry stage 1220px
- The stage (hero and reel) is centred and radial. Everything after it is left aligned.

## Shape and depth

| Element | Radius |
|---|---|
| Buttons, dock, tags, chips | 999px |
| Client tiles | 8% of the tile |
| Service cards, enquiry card | 22px to 38px |
| Service tiles in the form | 16px |
| Form fields | 14px |

Shadows are used on things that float: client tiles, the enquiry card, the dock and the
WhatsApp button. Sections and cards in the flow have none. A film grain sits over the
whole page at low opacity.

## Components

- **Primary action (`.cta`)**: black or white pill with a sun yellow disc. Used for
  "Start an enquiry" everywhere. `.cta.sm` in the hero.
- **Secondary (`.btn.ghost`)**: outlined pill. Fills on hover.
- **WhatsApp (`.wa`)**: black pill with the WhatsApp icon, pulse rings and a yellow arrow.
  Only for sending on WhatsApp.
- **Quiet (`.link`)**: underlined text.
- **Dock (`.dock`)**: black bar fixed at the bottom centre after the reel. Work, Studio,
  Services, Enquire. Hidden in the services and contact sections.
- **Reel controls (`.rbtn`, `.dial`)**: round outlined buttons and a 33 tick dial.
- **Service card (`.sv`)**: full width card that sticks and stacks, with a fan of tiles.
- **Form**: filled fields in `--well`, black border and yellow glow on focus, red border
  and a message under the field on error.
- **Service tile (`.tile`)**: icon, serif label and a tick. Turns black when chosen.
- **Case tag (`.card .tag`)**: small black "Case study" label on a client tile that has a
  case. Clicking that tile when it is at the centre opens the case.
- **Case index (`.case-row`)**: full width rows with the client name in display type.
  A row floods with the client's colour on hover.
- **Case page (`#view-case`)**: runs in the client's own palette. Fitted client name, one
  sentence, three facts, image plates (`.plate`, wide or two up), palette swatches
  (`.swatch`, click to copy) and a link to the next case. Cases are data in the `CASES`
  object and use only material from the client's brand files.

## Motion

- Entrance: logo assembles, the O opens onto the page. Plays once per visit.
- Reel: scroll, drag, arrow keys or buttons. Advances on idle. Can be paused.
- Text: headlines rise by word, the statement inks in with scroll.
- Page change: a curtain of six client colours.
- Hover: buttons pull toward the cursor, the centre tile tilts.
- 3D wheel (enquiry page): rests at an angle and sways, leans toward the pointer anywhere
  on the page, tips back with scroll, and can be grabbed and spun by mouse or finger.
- All of it is off under `prefers-reduced-motion`.

## Imagery and icons

- Client tiles are square crops of client work, 640px.
- Icons are 1.5px line icons drawn for this site. The WhatsApp icon is the supplied file.
- The sunburst is the only ornament: bullets, dividers, loader and the 3D wheel.
