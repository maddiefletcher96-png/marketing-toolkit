---
name: menu-builder
description: Build a new or updated food or drinks menu in Canva from an existing house design - swap in dishes, prices and photos, proofread it, check it against the kitchen's source, then optionally publish it to the website. Use for any menu - brunch, seasonal, set, sharing, drinks, kids or room service.
---

# Menu builder (Canva + website)

Output: a Canva design (cover and inside pages) built from a house template, proofread and checked line by line against the source, then optionally published to the website.

Needs the Canva connector. The website step works with any AI site builder that has a connector (Lovable, for example), or falls back to a paste-ready prompt.

---

## 1. Intake

Ask in a few short rounds. Skip anything already answered.

**Round 1: content**

1. Which venue and which menu? (e.g. brunch, autumn à la carte, Christmas set)
2. How will you give me the menu? Upload a file (PDF, Word, a photo of the kitchen sheet), paste it into the chat, or send a link. If pasting, use this format:
   ```
   SECTION NAME
   Dish name - description - £price
   ```
   Confirm it's the final, kitchen-approved version.
3. Which sections are in? Any to drop, merge or rename?
4. Prices per dish, or one price for the whole menu?

**Round 2: layout**

Show each house design as a thumbnail plus a simple text sketch, and ask which to use:

```
COVER                     INSIDE
  [logo]                    Brunch    | Coffee
        [photo]             - dish    | - list
  Brunch                    - dish    |---------
  [photo]   Menu            ----------| Tea
  [Book again + QR]         Cocktails | [allergy]
```

Also ask for the cover title words (e.g. "Brunch / Menu").

**Round 3: images**

5. Which photos? Upload them now, point to a Drive folder, or ask me to pick from your usual folders and show you a contact sheet first. Cover photos must show dishes that are on this menu.
6. Footer: allergy line (always), service charge line (yes or no), dietary tags (only if the kitchen has confirmed them).

**Round 4: output**

7. Canva only, print PDF, or also on the website? Which page?
8. Who signs off, and by when?

---

## 2. House designs

Keep a table of your templates so the skill can find them:

| Layout | Canva design ID | Use for | Structure |
|---|---|---|---|
| [Two-column with drinks] | [ID] | [Brunch, breakfast] | [What's on the cover and each column] |
| [Two-column à la carte] | [ID] | [Seasonal] | [...] |
| [Single centred column] | [ID] | [Set or sharing menus] | [...] |
| [Single page, no cover] | [ID] | [Simple one-pager] | [...] |

Note the shared rules: logo position, text colour hex, heading and body fonts.

---

## 3. Proofread (before building and again before saving)

UK English spelling, grammar and consistency pass:

- Typos ("serverd" to "served", "Camomille" to "Camomile")
- Dish names in Title Case, descriptions in sentence case
- Descriptions either all end in a full stop or none do
- "&" or "and", one or the other, throughout
- Curly apostrophes, correct accents (crème fraîche, purée), £ before prices, one price format (£3.50 not £3.5)
- House style: [e.g. commas not "|", no em dashes, drinks lists without descriptions]
- **Proper nouns** (suppliers, farms, cheeses, brands): never correct silently. Flag anything that looks wrong and ask.

Show a short before-and-after list of every correction and wait for a yes. Never change dishes, ingredients or prices while proofreading.

---

## 4. Build in Canva

1. Never edit the original. Copy the template and rename the copy.
2. Read the design to get element IDs.
3. **Cover:** change only the title words and swap photos into the existing frames. Don't move logos, QR codes or footer bands.
4. **Inside:** reuse existing text boxes so fonts stay on brand.
   - Dish boxes: find-and-replace the name and description separately. Match only visible words, since a replacement takes the formatting of the character before it.
   - Simple lists (coffee, tea, soft drinks): replace the whole box, then set the size.
   - Delete unused boxes, tags and dividers. Reposition what's left.
5. Tell the user about the limits: resizing a text box doesn't scale its text, and new text boxes use an off-brand default font, so drag-resizing is sometimes quicker by hand.
6. Check the thumbnail after every edit and fix overlaps.

## 5. Getting photos into Canva

- **Uploaded in the chat:** resize anything over about 5MB, then upload.
- **From Drive:** list the folder, make a contact sheet, let the user pick, then import only the picks. If a file has to be made link-shareable for the import, switch sharing back off straight afterwards and say so.
- Flag any photo that doesn't match the dish as written (the photo shows sourdough, the menu says potato bread).

## 6. Verify and save

- Check every name, description and price against the source, line by line. List anything left out and why.
- Run the proofread again on the final Canva text.
- Confirm logos, QR code and footer haven't moved.
- Show the preview and get an explicit yes before saving. Never save without it.

---

## 7. Publish to the website (optional)

Never publish without explicit approval.

1. Export the menu from Canva as a PDF (for a download button) and the cover photos as images.
2. **If a site-builder connector is available:** find the right project and page, confirm them with the user, send the build prompt below with the exports, check the preview against the approved menu, then ask "Publish this to the live site?" before deploying.
3. **If not:** save the prompt as a file and tell the user to paste it into their site builder with the exports.

**Build prompt template** (fill every bracket from the approved menu, never invent items):

```
Add a new page at /[venue]/[menu-slug] titled "[Menu name] | [Venue]". Don't change other pages, navigation, logos or global styles.

Layout (mirror the printed menu):
- Header: existing logo, centred, unchanged.
- Hero: "[Cover title]", with photos [photo-1] (alt: "[dish]") and [photo-2] (alt: "[dish]"), stacked on mobile.
- Sections in this order, [two columns / one column] on desktop, one on mobile: [sections].
- Footer: "Please let us know if you have any allergies or dietary requirements." [+ service charge line]
- "Download menu (PDF)" button linking to [menu.pdf].

Style: [background colour], text [hex], site heading font for dish names and section titles, body font for descriptions. UK spelling.

[Full menu text, exactly as approved]

Show me a preview. Don't publish until I confirm.
```

---

## 8. Hand-off

- Canva link, and what changed from the template
- Proofreading corrections made, and anything flagged but left alone
- Anything left out or merged, and any photo mismatches
- Website status: preview link, live link, or where the prompt is saved
