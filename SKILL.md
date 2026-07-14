---
name: product-ux
description: Use when designing or reviewing any product UI — onboarding, signup, forms, paywalls, pricing, checkout, dashboards, tables, admin panels, data views — or when the concern is drop-off, low conversion, users abandoning a flow, a cluttered dashboard, a table that feels unusable, or "it looks fine but nobody uses it".
---

# Product UX

## Overview

Two failures kill products, and neither is visual. **Framing** decides whether the user acts — the same fields, the same price, the same button convert very differently depending on how they're presented. **Craft** decides whether they can work once they act — whether the data drives the interface, or the interface was drawn first and the data poured in after.

Fix the framing and the craft before touching the pixels. A prettier empty form is still an empty form.

**Subtract before you add.** Every element must earn its place by serving the user's task. What doesn't serve it isn't neutral — it's noise that buries what does, adds one more thing to decide, and dilutes the one action that matters. When in doubt, cut it. The test is *function*, not quantity: a tooltip, a default, or a loop that confirms an action all earn their place; a decorative chart, a second CTA competing with the first, filler copy, and a field you never read do not. Removing the useless is how you protect the useful — this is not license to strip what does a job.

## When to Use

- Conversion surfaces: signup, onboarding, forms with 3+ fields, paywalls, upgrade prompts, pricing, checkout, trials.
- Working surfaces: dashboards, tables, data views, admin panels, activity logs.
- Symptoms: drop-off mid-flow, "maybe later" always wins, price feels expensive, dashboard feels cluttered, table is technically fine but nobody uses it.

Not for: internal throwaway tools, or flows where the user is already committed and raw speed beats everything.

## Part 1 — Framing (does the user act?)

| Principle | Rule | Fix |
|---|---|---|
| **Smart defaults** | Never ship an empty form. | Pre-fill every field with the most common choice — a default reads as a recommendation, and most users never change it. The button states the outcome ("Search 12 results"), not the action. |
| **Goal gradient** | Never start a user at 0%. | Count something they already did (created the account) as step 1. Show 20%, not 0%. Progress creates momentum even when it's granted rather than earned. |
| **Reciprocity** | Give value before asking for anything. | Deliver a real, partial result *before* the signup wall — a score, the top issues, a preview. Then ask to save it. Never blur the result behind "create an account to continue". |
| **IKEA / endowment effect** | Let them build before they commit. | Move customization (name, colors, goal, first item) *before* signup. The final button says "Continue", not "Sign up" — leaving now means abandoning something they made. |
| **Loss aversion** | Sell the loss, not the gain. | Losing hurts roughly twice as much as gaining pleases. Show what they lose by not acting (named files, expiring data), not what they'd gain. The dismiss carries weight ("I'll risk it"), never "Maybe later". |
| **Contrast effect** | Never show a price in isolation. | Anchor it against a bigger number already on screen. $50 beside a $1,900 cart, labeled "just 2.6%", feels free. $50 alone on a page becomes $600/year. |

## Part 2 — Craft (can they work?)

**The data drives the form.** Look at the data first, then choose the shape. A fixed set of values (department, status) is chips, not free text. Numbers are right-aligned so digits line up by place value. Long text truncates so other columns can breathe. Inactive rows are shaded down. Time-series data wants a timeline or a chart, not a timestamp column the user has to scan. Color comes from the data's meaning — red because the action is urgent, an avatar because the eye matches a face faster than it reads a name — never as decoration.

**Progressive disclosure.** Hierarchy isn't only what's big; it's what's shown versus what's hidden. Rank each action on a spectrum of explicitness: a global button (always visible) → an icon in the row → an action revealed on hover → a swipe gesture. Put each action where its importance actually lands. A rarely-used Share goes in a popover, not permanently in the toolbar. Remove-user appears on hover with a tooltip. And onboarding is this same idea over time: one tooltip on the most important action, then the next — never a modal with six bullets that the user dismisses and instantly forgets.

**The invisible UI is half the product.** What you can't see is as much of the interface as what you can: hover states, copy-on-hover chips, comment indicators, empty states, loading states, drawers, tooltips. Beginners ship only the visible layer, then wonder why a dense screen feels broken. Assume the user won't decode your icons and won't understand your ambiguous labels — tooltips are the single most common omission on amateur dashboards. New functionality usually doesn't need a new page; it needs a hidden layer thought through properly.

## Part 3 — Feel (do they come back?)

Delight is not decoration, but it only pays in two specific places. Everywhere else it's a distraction from Parts 1 and 2.

**Products built on repetition** (streaks, check-ins, journaling, habit logging): every completion needs emotional feedback, not a green checkmark. The user must *see* the thing they're building — momentum made visible is the product. A confirmation that merely confirms is a wasted moment.

**High-stakes domains** (fintech, crypto, health, insurance): polish is a trust signal, not a finish. A janky transition in a wallet reads as "unsafe with my money" — the user can't audit your security, so they judge it by the only proxy they have. Here, motion and craft in onboarding and security flows *are* the feature.

Scope: what the delight is *for* belongs here. How to build it — easing, shadows, typography, animation timing — is a visual-polish concern and lives in a polish skill, not this one.

Caution: delight cannot rescue a badly framed flow. A charming mascot on a form that asks before it gives is still a form that asks before it gives. And beware the famous case studies — the products credited to "delight" also shipped new features, curriculum and marketing in the same window. Correlation gets sold as causation in this space constantly.

## Review Checklist

Any "yes" is a leak:

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
11. Is anything on the screen there without a job — a decorative element, a competing CTA, filler copy, a field nobody reads? Cut it.

## Never Trade Accessibility for Conversion

Loss aversion makes the exit *heavier*, never *harder to reach*. Shrinking a hit area, hiding the dismiss, or dropping its contrast is a dark pattern, not a principle. The weight belongs in the label ("I'll risk it"), never in the tap target — an accessible 44pt dismiss with honest copy beats a 28pt one every time. Hover-only actions need a keyboard and touch path too. If a polish or a11y rule says "enlarge this target", it wins. No exceptions.

## Common Mistakes

- **Blurring the result behind a paywall.** Kills reciprocity. Show the partial result; charge for depth.
- **Confusing dark patterns with these principles.** Fake countdowns and invented scarcity are lies. Loss aversion works only when the loss is *real*.
- **Decorative color on a dashboard.** On a landing page you can get away with it. On a data view, color that doesn't encode meaning is noise.
- **Fixing the pixels instead of the framing.** Radius and shadows don't fix a screen that asks before it gives.

## Research

Choice overload (Iyengar & Lepper), endowed progress (Nunes & Drèze), reciprocity (Cialdini), the IKEA effect (Norton, Mochon & Ariely), loss aversion (Kahneman & Tversky), the contrast effect.

The percentages here are secondhand and unverified against the original papers. Use them to pick a direction, never to justify a decision in writing — check the primary source first.
