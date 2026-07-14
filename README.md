# ux-psychology

A [Claude Code](https://claude.com/claude-code) skill for the flows where users decide, commit, or pay — onboarding, signup, forms, paywalls, pricing, checkout.

It reviews the **framing** of a screen, not its visuals. The same fields, the same price, and the same button convert very differently depending on how they're presented. Six behavioral principles, one review checklist, and a hard line against dark patterns.

## Install

Personal (available in every project):

```bash
git clone https://github.com/carlovsk1/ux-psychology.git ~/.claude/skills/ux-psychology
```

Per-project (travels with the repo, whole team inherits it):

```bash
git clone https://github.com/carlovsk1/ux-psychology.git .claude/skills/ux-psychology
```

Claude picks it up automatically when you mention onboarding, signup, paywalls, drop-off, or conversion. Invoke it explicitly with `/ux-psychology`.

## What it catches

Point it at a flow and it runs six questions. Any "yes" is a conversion leak:

1. Is any field empty that could have a sensible default?
2. Does the first progress indicator show 0%?
3. Does the user hit a wall before receiving anything of value?
4. Does the user own or create anything before the signup screen?
5. Is an upgrade framed as a gain instead of a loss?
6. Is a price shown without a larger anchor next to it?

## On dark patterns

Loss aversion works only when the loss is real. Fake countdowns, invented scarcity, shrunken dismiss buttons, and hidden exits are lies, and the skill says so explicitly — accessibility beats conversion every time, with no exceptions. If you want a tool for manipulating users, this isn't it.

## Research

The principles come from established behavioral research: Cialdini (reciprocity), Kahneman & Tversky (loss aversion), Iyengar & Lepper (choice overload), Norton/Mochon/Ariely (the IKEA effect), Nunes & Drèze (endowed progress).

The percentages quoted in the skill are secondhand and unverified against the original papers. They're there to point you in a direction — check the primary source before putting a number in a deck.

## License

MIT
