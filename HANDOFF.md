# Higgins Hardwood Flooring — handoff at ~60%

**Live:** https://10elizabethbell.github.io/higginsHardwoodFlooring/ · **Repo:** https://github.com/10elizabethbell/higginsHardwoodFlooring · **Built:** 2026-10-20 from Muse brief 2026-10-20 · **Call Sheet:** site URL set (the script added a new minimal entry; Muse hadn't made one)

## What's built
- One page, phone first: header (logo's H mark and wordmark, "Message me" top right), hero, What I do (4 service rows that pre-select the form), care section with the Facebook link, How it works (3 steps), free-estimate form, close band with the full logo, footer.
- Calm band style coloured from the **real logo** (pulled from the Facebook page's og:image): deep navy `#0f132e`, mid navy `#1b2352`, gold `#c9a24a` as a fill (text on it is navy), `#7a5a12` for gold text on light, paper `#f6f5f1`.
- Hero: a **generated** example floor (see image table) under a navy overlay; white text is 8.6:1 or better on it (sampled at 360, 390 and 1440px). H1 bounce-in, 12px fade-up, floating contact circle all working; plain heading and all content show at once under reduced motion and with no JS.
- **Contact is Facebook Messenger only** (`m.me/HigginsHardwoodFlooring`), because the brief has no phone or email. The form writes the message, copies it, and shows "Open Messenger" + "Copy message" (Messenger can't take a pre-filled message).
- **One switch for a phone number:** set `CONFIG.PHONE` and `CONFIG.PHONE_SHOWN` at the top of the script. The header and close band then show a tap-to-call number, the circle becomes a pre-filled text, the form texts the message, and the footer gets the number. `CONFIG.EMAIL` adds the footer email.
- Favicon, home-screen icon and og image (1200x630) are made from the logo.

## Assumptions I made
- The owner is one person ("I'm starting my own…"), so the copy is first person "I".
- `facebook.com/HigginsHardwoodFlooring` is the brief's page: the brief's `profile.php?id=100028121125506` reports that as its og:url, and the vanity page points back to profile 100028121125506. m.me redirects to Messenger thread id 102449481613555 (the page's page-ID). I checked the redirect, not a real conversation.
- Services named from his caption plus the Facebook category ("Refinishing & Installation"): Sanding & refinishing, Buff & coat, Floor repairs, Replacing & installing.
- "Around Philly" in the H1; the full area (Philadelphia, New Jersey, Delco, Delaware) is in the form eyebrow, close and footer.
- Step 3, "Sanded, fixed or coated, start to finish." and "I'll … tell you straight what they need" are my wording of his offer, not his words.

## Placeholders and gaps
- **No phone, no email** (the top gap). Site runs on Messenger until `CONFIG.PHONE` is filled.
- **No real photos.** The hero and care photo are generated examples; swap in his jobs as soon as he has any. No reviews, owner name, hours, years, insurance or home town, so none are on the page.
- I didn't use the calm style's plain navy hero, because the skill says to generate a photo when the client hasn't supplied one. The finish reviewer read the house rules the other way (plain textured navy, and no non-client photo beside "Find me on Facebook"). Your call; deleting the `<picture>` and `.shade` in the hero gives the DPG look.

| File | Shows | Source | Prompt (short) | Licence |
|---|---|---|---|---|
| img/hero.webp, img/hero-phone.webp | Empty rowhome front room, refinished red oak | generated with gpt-image-1, 2026-10-20 | "real-estate photograph… freshly sanded and refinished red oak floor… Philadelphia rowhome… satin finish" | generated; OpenAI terms assign output to the user |
| img/finish.webp | Low close view of a white-oak floor with a fresh satin coat | generated with gpt-image-1, 2026-10-20 | "close view at a low angle across a white oak floor just buffed and given a fresh coat of satin finish, morning daylight" | same |
| img/logo.webp, img/mark.png, favicon.png, apple-touch-icon.png, og.jpg | His logo / H mark | Facebook profile image, fetched 2026-10-20 | — | owner's |

## Questions for the owner
- Phone number, and does it take texts? Email for the footer?
- Your first name, so the page can say who's coming out.
- Photos of your jobs, especially before/after sanding pairs.
- Which towns or counties you most want work in; where you're based.
- Which job you want more of (full sands vs buff and coat vs installs)? That can lead the services list.
- Insured? Years doing floors? Anything you're proud of? (Only if true; none of it is on the page now.)
- Hours, or "evenings and weekends" for estimates?

## Ideas not built (yours to pick)
- **Signature motion (opt-in), best world: a sander pass.** Drag across a dull, scuffed floor in the hero and leave fresh, sheened boards behind it, with the grime growing back slowly (Above All's wash recipe, in wood). Runners-up: satin coat drying in a sheen sweep; wood grain lines that part around the finger; sawdust motes in window light; a finish swatch picker (natural, golden oak, dark walnut).
- Before/after slider pairs once he has photos (the care section's photo spot is ready for them).
- A "Finishes" strip (natural, honey, espresso) as quick choices in the form.
- Self-host Cal Sans (woff2 in `fonts/`, OFL) to drop the two Google Fonts round trips on slow cellular; the skill currently says Google Fonts, so I left it.
- A metric-matched fallback font to stop the hero's small jump when Cal Sans arrives.
- Cut "Thanks for supporting a local business." (his own line, kept for voice; the distill pass called it optional).
- Impeccable findings I kept on purpose because they're house-style choices: eyebrow pills (craft floor's kicker ban) and the faint diagonal band texture (detector `repeating-stripes-gradient`, suppressed for index.html in `.impeccable/config.json`). The detector's `flat-type-hierarchy` was fixed by collapsing to 14/16/18/20 UI tiers, then the remainder suppressed (it doesn't count the clamp() headings).

## Not verified
- A real Messenger conversation from m.me inside Facebook's in-app browser (iOS and Android), and whether clipboard copy is allowed there (the copy button falls back to selecting the text).
- Real-device touch, and the `sms:`/`tel:` path (only active once a phone is set).
- Landscape phones (844x390): the estimate button sits about 75px below the first screen even after tightening.
- Frame rate on old phones (motion is CSS-only, so it should be fine).
