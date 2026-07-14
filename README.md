# product-ux

A [Claude Code](https://claude.com/claude-code) skill for the two failures that kill products, neither of which is visual.

**Framing** decides whether the user acts — the same fields, the same price and the same button convert very differently depending on how they're presented. **Craft** decides whether they can work once they act — whether the data drives the interface, or the interface was drawn first and the data poured in after.

It covers conversion surfaces (onboarding, signup, paywalls, pricing, checkout) and working surfaces (dashboards, tables, admin panels, data views). It does not cover visual polish — radius, shadows and animation are someone else's job.

## Install

Personal (available in every project):

```bash
git clone https://github.com/carlovsk1/product-ux.git ~/.claude/skills/product-ux
```

Per-project (travels with the repo, whole team inherits it):

```bash
git clone https://github.com/carlovsk1/product-ux.git .claude/skills/product-ux
```

Claude picks it up automatically when you mention onboarding, signup, paywalls, drop-off, conversion, dashboards or tables. Invoke it explicitly with `/product-ux`.

## What it catches

Point it at a screen and it runs nine questions. Any "yes" is a leak:

1. Is any field empty that could have a sensible default?
2. Does the first progress indicator show 0%?
3. Does the user hit a wall before receiving anything of value?
4. Does the user own or create anything before the signup screen?
5. Is an upgrade framed as a gain instead of a loss?
6. Is a price shown without a larger anchor next to it?
7. Is the data forced into a shape it doesn't want (a table for a timeline, free text for an enum, left-aligned numbers)?
8. Is a rare action taking permanent space — or a primary action buried behind a hover?
9. Are the hidden layers missing: hover, empty, loading, error states, and tooltips on every icon and ambiguous label?
10. In a repetition product, does completing the loop feel like nothing? In a high-stakes one, does the craft undercut the trust you're asking for?

## On dark patterns

Loss aversion works only when the loss is real. Fake countdowns, invented scarcity, shrunken dismiss buttons and hidden exits are lies, and the skill says so explicitly — accessibility beats conversion every time, with no exceptions. If you want a tool for manipulating users, this isn't it.

## Research

Established behavioral research: Cialdini (reciprocity), Kahneman & Tversky (loss aversion), Iyengar & Lepper (choice overload), Norton/Mochon/Ariely (the IKEA effect), Nunes & Drèze (endowed progress).

The percentages quoted in the skill are secondhand and unverified against the original papers. They point you in a direction — check the primary source before putting a number in a deck.

## License

MIT
