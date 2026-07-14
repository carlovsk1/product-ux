---
name: ux-psychology
description: Use when designing or reviewing user-facing flows where the user must decide, commit, or pay — onboarding, signup, empty forms, paywalls, upgrade prompts, pricing pages, checkout — or when the concern is drop-off, low conversion, abandoned onboarding, or "users don't finish this".
---

# UX Psychology

## Overview

Users don't decide logically. Six behavioral principles predict whether a flow converts. Apply them to the screen's *framing*, not its visuals — the same fields, the same price, the same button can convert 2x more depending on how they're presented.

## When to Use

- Building or reviewing: signup, onboarding, forms with 3+ fields, paywalls, upgrade/premium prompts, pricing, checkout, trials.
- Symptoms: high drop-off mid-flow, users bounce at the signup wall, "maybe later" always wins, price feels expensive.

Do NOT use for: internal tools, admin dashboards, or flows where the user is already committed and speed matters more than persuasion.

## The Six Principles

| Principle | Rule | Fix |
|---|---|---|
| **Smart defaults** | Never ship an empty form. | Pre-fill every field with the most common choice. 70–90% never change defaults; a default reads as a recommendation. Button shows the outcome ("Search 12 results"), not the action. |
| **Goal gradient** | Never start a user at 0%. | Count something they already did (created the account) as step 1. Show 20%, not 0%. Progress creates momentum even when the progress is granted, not earned. |
| **Reciprocity** | Give value before asking for anything. | Deliver a real, partial result *before* the signup wall — score, top issues, preview. Then ask to save it. Never blur results behind "create an account to continue". |
| **IKEA / endowment effect** | Let them build before they commit. | Move customization (name, colors, goal, first item) *before* signup. The final button says "Continue", not "Sign up" — leaving now means abandoning something they made. |
| **Loss aversion** | Sell the loss, not the gain. | Losing hurts ~2x more than gaining pleases. Show what they lose by not acting (named files, expiring data, a countdown), not what they'd gain. The dismiss option carries weight ("I'll risk it"), not "Maybe later". |
| **Contrast effect** | Never show a price in isolation. | Anchor it against a bigger number already on screen. $50 next to a $1,900 cart, labeled "just 2.6%", feels free. $50 on its own page becomes $600/year. |

## Review Checklist

Run against any flow screen:

1. Is any field empty that could have a sensible default?
2. Does the first progress indicator show 0%?
3. Does the user hit a wall before receiving anything of value?
4. Does the user own/create anything before the signup screen?
5. Is an upgrade framed as a gain instead of a loss?
6. Is a price shown without a larger anchor next to it?

Any "yes" is a conversion leak. Fix the framing before touching the visuals.

## Never Trade Accessibility for Conversion

Loss aversion makes the exit *heavier*, never *harder to reach*. Shrinking a hit area, hiding the dismiss button, or lowering its contrast is a dark pattern, not a principle. The weight goes in the label ("I'll risk it"), never in the tap target — an accessible 44pt dismiss with honest copy beats a 28pt one every time. If a polish skill says "enlarge this hit area", it wins. No exceptions.

## Common Mistakes

- **Blurring the result behind a paywall.** Kills reciprocity. Show the partial result; charge for depth.
- **Confusing dark patterns with these principles.** Fake countdowns and invented scarcity are lies. Loss aversion only works honestly: show a loss that is *actually* real.
- **Applying to internal tooling.** Persuasion on a screen the user is forced to use is just noise.
- **Fixing the UI instead of the framing.** A prettier empty form is still an empty form.

## Research

Choice overload (Iyengar & Lepper), endowed progress (Nunes & Drèze), reciprocity (Cialdini), the IKEA effect (Norton, Mochon & Ariely), loss aversion (Kahneman & Tversky), the contrast effect.

The percentages in this file are secondhand and unverified against the original papers. Use them to pick a direction, never to justify a decision in writing — check the primary source first.
