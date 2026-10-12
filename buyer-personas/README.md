# Listing Persona Builder

A reusable tool for real estate agents: enter a listing's features and get the
buyer personas most likely to purchase it, ranked by fit.

Each persona includes:

- fit score (0–100) and household / budget profile
- the listing features that hook them, and what they want
- likely objections, with a suggested response
- marketing channels to reach them and tips for the showing
- a headline (and, with Claude, ad copy) aimed at that buyer

## How it works

`index.html` is a single self-contained page, published as a claude.ai Artifact.

- **With Claude** (when the viewer allows it): the listing is sent to Claude,
  which writes named personas, hooks and ad copy specific to the property.
- **Built-in matcher** (always available, no AI needed): 14 buyer archetypes
  scored against the property type, price position, condition, bedroom count
  and ticked features. Used for the example on first load and as a fallback.

Saved listings are kept in the viewer's own browser (localStorage). "Copy full
brief" copies everything as plain text for CRM notes or a marketing plan.

Ad copy is written to describe the property, not the buyer, to stay within
fair housing rules; personas are meant as an internal planning aid.
