# Orya Mark

Portfolio site for Orya Mark, a creative studio and digital marketing agency in Hyderabad.

It is a static site: one `index.html`, images in `assets/`, two small libraries in `vendor/`. There is no build step.

## Run it locally

```
npx serve .
```

Then open the address it prints. Opening `index.html` directly also works.

## Deploy on Vercel

Import this repository in Vercel, choose the "Other" framework preset, leave the build command empty and deploy.
After the first deploy, put the site address into the `og:image` tag in `index.html` so link previews show the image.

## Where things live

- Clients in the reel: the `D` array near the top of the script in `index.html`. One row per client, with the image in `assets/`.
- Case studies: the `CASES` object just below it. Each case lists its images, palette and typefaces.
- Phone numbers and the WhatsApp number: search `index.html` for `9701125654`.
- Colours, type and components: see `DESIGN.md`.

## Pages

- `/` the home page
- `/#enquiry` the enquiry page
- `/#case-anha`, `/#case-elite` the case studies
