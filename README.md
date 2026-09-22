# ApplonxAI — one page website

A single page site for **ApplonxAI**: an enquiry intake tracker, a quotation chase board and a
Monday lead digest, built for construction contractors, engineering consultants and industrial
suppliers.

- `index.html` — the whole site. All CSS and the small JavaScript are inside this one file.
- `README.md` — this file.

There is no backend and no build step. The contact section is links only: booking, WhatsApp and
email open in the reader's own apps.

## How to open it

Double-click `index.html`, or from this folder:

```
open index.html
```

Everything lives in this folder, so the page and the pictures must stay together.

## Contact links on the page (used exactly as given)

| Link | Where it points |
| --- | --- |
| Book a 20 minute call | `https://cal.com/arshad9849/20-min-ai-business-discovery-call` |
| Message me on WhatsApp | `https://wa.me/966530950377?text=…` (number `966530950377`, prefilled hello that names Applonxai.com) |
| Email me | `mailto:help@applonxai.com?subject=Enquiry%20from%20Applonxai.com` |

All three appear twice: once in the contact section near the bottom, and again in the footer.

## The lines that are yours to fill in

Search `index.html` for the square brackets. Everything in square brackets is a line for you to
edit, and nothing in the contact links is a slot.

| Slot | Where it sits | What to do |
| --- | --- | --- |
| `[YOUR RESULT]` | the Proof band | one real result you can stand behind |
| `[CLIENT QUOTE]` | the Proof band | a real sentence from a real client |
| `[YOUR TIMELINE]` | the Proof band | the timeline you want to promise |

The name on the page is **Arshad Khan**, beside the round profile picture. No price, fee or rate
appears anywhere on the page: under the three service cards there is one quiet line, "Fixed scope,
agreed before we start.", and a button asking the reader to **Book a discovery call with me**.
Step three of "How it works" says the digest keeps running after the pilot. If you ever want a
figure on the page, add it to that line yourself — it is deliberately absent.

The booking link is already real and points at your cal.com page. If you ever swap it, change the
four `https://cal.com/...` links: the header, the first screen, the line under the service cards
and the footer.

## Pictures used

Taken from this folder, by these names:

| File | Where it appears | Alt text |
| --- | --- | --- |
| `Logo.png` | header, about 40 px tall | ApplonxAI logo |
| `Logo-Dark.png` | footer, small, on Midnight Blue | ApplonxAI logo |
| `Speaking.jpeg` | top of the page, full width behind the headline | Speaking to a room of contractors beside a screen showing quotation chase results |
| `Client Meeting.png` | full width picture band between sections | Presenting the ApplonxAI quotation chase board to a contractor team in a meeting room |
| `Working .png` | beside the "Who I am" section, about a third of the width | Working at a site office desk on the ApplonxAI quotation chase board |
| `Profile.jpeg` | small and round, beside your name | Portrait of the person behind ApplonxAI |

Two things worth knowing:

1. **`Working .png` has a space before the dot.** The page links to it as `Working%20.png`, which
   is the same file. If you rename the file to `Working.png`, change the `src` in `index.html` to
   match.
2. **The logo files are square, with the wordmark in a band across the middle.** The page crops
   that band with CSS (`.logo-frame`), so the logo stands at its real height instead of shrinking
   to a thumbnail. `--logo-aspect` holds each file's wordmark shape, and the three percentages
   inside `.logo-frame img` and `.logo-frame.is-dark img` hold the crop position. The header logo
   also uses `mix-blend-mode: multiply` to drop the file's white background onto the cream page,
   and the footer logo uses `lighten` to drop its navy background onto the Midnight Blue footer.
   If you swap in a new logo with different padding, those are the values to adjust.

Unused pictures in this folder, if you want them on the page later: `Short 2.png`,
`Quotating tracking.png`, `Shot 1.png`, `Desk.png`, `Qoutation Chased.jpeg`,
`Contractor_office_desk_flat_lay.jpeg`, `Contractor_reviewinng.jpeg`,
`Laptop_screen_displaying_results.jpeg` and `Person_working_in_site_office.jpeg`.

If a picture is missing, that section keeps its heading and words and closes up the gap.

## Colour

Every colour is named with its hex code in the `:root` block at the top of `index.html`.

| Name | Hex | Used for |
| --- | --- | --- |
| Soft Cream | `#F7F3EC` | page background |
| Ink Black | `#111111` | body text |
| Deep Teal | `#0F6B6B` | accent only: buttons, one headline word, small rules, icons |
| Teal Dark | `#0A5252` | Deep Teal on press and hover |
| Warm Sand | `#D9C7A7` | labels, hairlines, service card fills, the Proof band |
| Sand Line | `#E3D6BF` | hairlines on cream |
| Midnight Blue | `#14213D` | contact panel and footer |
| Ink Muted | `#4A4A4A` | secondary body text |

Deep Teal is never used as a full width block behind text.

## Type and layout

- Headlines: **Fraunces**. Body: **Inter**. Both loaded from Google Fonts with one `link` tag.
- Body text is 18 px with a line height of 1.6, in a column of about 66 characters, so no line
  runs the full width of a laptop.
- Every section has at least 56 px of padding above and below on a phone and 96 px on a laptop.
- Phone first: one column, tap targets 44 px or taller, nothing scrolls sideways.

## Browser notes

- Needs a live internet connection for the two Google Fonts. Without it the page falls back to
  Georgia and the system sans, and everything still reads.
- `mix-blend-mode` on the two logo images needs a modern browser (Chrome, Safari, Edge, Firefox).
- If JavaScript is switched off, every section, link and picture still works. The only losses are
  the small screen menu and the fade in.
