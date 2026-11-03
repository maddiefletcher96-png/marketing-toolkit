# Menu builder skill

An AI workflow for the job every restaurant marketer knows: the kitchen changes the menu, and someone has to get it into the house design, proofread it, check every price and put it on the website by Friday.

The skill copies a Canva house template, swaps in dishes, prices and photos, proofreads in UK English, checks everything against the kitchen's source line by line, and can publish to the website through a site builder. It asks for approval before it saves or publishes anything.

## What it's careful about

- **It never edits the original template.** It always works on a copy.
- **It never changes dishes or prices while proofreading.** Corrections are shown as a before-and-after list first.
- **It never quietly fixes proper nouns.** Supplier and farm names get flagged, not "corrected".
- **Photos have to match the menu.** If the picture shows a dish that isn't on it, the skill says so.

## Set it up

1. Add your house templates to the table in section 2 of [`SKILL.md`](SKILL.md), with Canva design IDs and a line on each layout.
2. Fill in your house style rules in section 3.
3. Connect Canva (and a site builder like Lovable, if you want the website step).
4. Save the folder as a Claude skill and ask for "a new brunch menu".
