---
name: product-ux
description: Use when designing or reviewing any product UI — onboarding, signup, forms, paywalls, pricing, checkout, dashboards, tables, admin panels, data views, landing pages — or when the concern is drop-off, low conversion, users abandoning a flow, a cluttered dashboard, a table that feels unusable, a landing page that loses visitors, or cleaning up AI/vibe-coded output that reads as generated. Also when adding gamification, streaks, badges, points, leaderboards, habit loops, or any retention mechanic meant to bring users back.
---

# Product UX

## Overview

Two failures kill products, and neither is visual. **Framing** decides whether the user acts — the same fields, the same price, the same button convert very differently depending on how they're presented. **Craft** decides whether they can work once they act — whether the data drives the interface, or the interface was drawn first and the data poured in after.

Fix the framing and the craft before touching the pixels. A prettier empty form is still an empty form.

Most of this work is undoing defaults. The gap between a vibe-coded app and a product people pay for is almost never the code — it's a dozen interface decisions AI gets wrong by default, and undoing them needs a checklist, not taste. And design for the user, not yourself: they aren't tourists exploring your interface, they bought it to get a job done and care only about the result. Guide them down the route far more than feels necessary.

**Subtract before you add.** Every element must earn its place by serving the user's task. What doesn't serve it isn't neutral — it's noise that buries what does, adds one more thing to decide, and dilutes the one action that matters. When in doubt, cut it. The test is *function*, not quantity: a tooltip, a default, or a loop that confirms an action all earn their place; a decorative chart, a second CTA competing with the first, filler copy, and a field you never read do not. Removing the useless is how you protect the useful — this is not license to strip what does a job.

## When to Use

- Conversion surfaces: signup, onboarding, forms with 3+ fields, paywalls, upgrade prompts, pricing, checkout, trials, landing/marketing pages.
- Working surfaces: dashboards, tables, data views, admin panels, activity logs.
- Cleaning up AI/vibe-coded output: a screen that reads as generated — repeated KPI cards, decorative color, overloaded cards, no empty/loading states.
- Symptoms: drop-off mid-flow, "maybe later" always wins, price feels expensive, dashboard feels cluttered, table is technically fine but nobody uses it, landing page loses visitors before signup.

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
| **Chunking** | Never ask them to hold more than three or four things. | Working memory tops out around three or four items, so a flat list of reasons to buy is half-forgotten by the bottom of the page. Group the reasons under named categories, and in pricing write "everything in Basic, plus:" instead of repeating the whole feature list in every tier — the user should read the difference, not hunt for it. |

## Part 2 — Craft (can they work?)

**Start from intent, not layout.** Before you think about cards, sidebars, or icons, ask the one question: what did the user arrive to *do*? Each page answers exactly one question. The clearest tell of a generated app is repetition — the same four KPI cards on the dashboard, the analytics page, and the billing page, because the tool has no memory of what it already built. Audit every page: name the one thing someone comes here for, and delete everything that isn't it. Functionality expands only when the user's intent expands (a second intent — browsing vs. searching — is what filters are for), never because you had space to fill.

**Convention is the frame; creativity goes inside it.** People arrive with a blueprint already in their head — logo top-left, navigation next to it, footer at the bottom — assembled from every other site they have ever used. When something isn't where the blueprint says it should be, most of them don't go looking; the screen reads as broken and they leave. Gaming Bible moved its mobile menu to the bottom corner, closer to the thumb and better UX on paper, and had to move it back because nobody could find it. So the macro structure and the landmarks stay where they're expected, and the originality lives *inside* that structure — a considered hover, a section that isn't the row everyone ships. This is the ceiling on Part 4's *get out of template territory*: the sweet spot designers call MAYA, most advanced yet acceptable — new enough that the visitor feels something, familiar enough that they still know where they are.

**The data drives the form.** Look at the data first, then choose the shape. A fixed set of values (department, status) is chips, not free text. Numbers are right-aligned so digits line up by place value. Long text truncates so other columns can breathe. Inactive rows are shaded down. Time-series data wants a timeline or a chart, not a timestamp column the user has to scan. Color comes from the data's meaning — red because the action is urgent, an avatar because the eye matches a face faster than it reads a name — never as decoration.

**Compress the dense components first** — biggest visible change for the least work. AI is worst at repeated components: a card or row is where it dumps every button, chip, and timestamp at equal weight. Run a compression pass — collapse the button row into an overflow (⋯) menu, turn text chips into icons, mute the metadata, push the one number that matters to the edge. Same information, a third of the noise. And match the container to the content: four fields living in a mostly-empty slide-out want a centered modal instead. Reserve color for what carries meaning — status or a single action — not for every field at once.

**Progressive disclosure.** Hierarchy isn't only what's big; it's what's shown versus what's hidden. Rank each action on a spectrum of explicitness: a global button (always visible) → an icon in the row → an action revealed on hover → a swipe gesture. Put each action where its importance actually lands. A rarely-used Share goes in a popover, not permanently in the toolbar. Remove-user appears on hover with a tooltip. And onboarding is this same idea over time: one tooltip on the most important action, then the next — never a modal with six bullets that the user dismisses and instantly forgets. The trial's first minutes are when the user is least patient, so make the first step impossible to miss (the primary card sits higher, greener, says "start here"), show a progress bar toward the finish, and celebrate each completion — forced tutorials get clicked through without reading.

**The invisible UI is half the product.** What you can't see is as much of the interface as what you can: hover states, copy-on-hover chips, comment indicators, empty states, loading states, drawers, tooltips. Beginners ship only the visible layer, then wonder why a dense screen feels broken. Assume the user won't decode your icons and won't understand your ambiguous labels — tooltips are the single most common omission on amateur dashboards. New functionality usually doesn't need a new page; it needs a hidden layer thought through properly.

**Design for the ugly data, not the demo data.** The app looks great because you filled it with tidy examples — short names, round numbers — inside a bubble the user never shares. Stress it with real data: long strings, missing values, overflow, huge counts. Decide the rules now: truncate long text with an ellipsis, put icons on a solid shape so they survive any background, and build the empty, loading, and error states deliberately, because a new user hits those *first*.

**Perceived performance is a feature; speed is an aesthetic.** A blank wait reads as broken — a one-second delay measurably costs conversions — and the fix is usually showing something immediately, not faster code. A skeleton that mirrors the final layout reads as fast even though nothing loaded sooner; show a progress indicator for anything over ~1s, and something playful for genuinely long jobs. Users tolerate a two-second wait with evidence that something is happening; they don't tolerate two seconds of blank.

**Destructive actions: confirm, then complete.** Some actions should be hard to press. A silent delete leaves two wounds — no undo, and no proof it worked, so the user refreshes to check. For anything destructive, expensive, or final: state what will happen and that it can't be undone before, and for the truly serious require type-to-confirm (Supabase makes you type the database name — tedious by design, because it's the danger zone). After, show an explicit completion state plus a brief undo window. Unfinished actions nag (the Zeigarnik effect): a task that finished but showed nothing still bugs the user.

## Part 3 — Feel (do they come back?)

Delight is not decoration, but it only pays in two specific places. Everywhere else it's a distraction from Parts 1 and 2.

**Products built on repetition** (streaks, check-ins, journaling, habit logging): every completion needs emotional feedback, not a green checkmark. The user must *see* the thing they're building — momentum made visible is the product. A confirmation that merely confirms is a wasted moment.

**High-stakes domains** (fintech, crypto, health, insurance): polish is a trust signal, not a finish. A janky transition in a wallet reads as "unsafe with my money" — the user can't audit your security, so they judge it by the only proxy they have. Here, motion and craft in onboarding and security flows *are* the feature.

Scope: what the delight is *for* belongs here. How to build it — easing, shadows, typography, animation timing — is a visual-polish concern and lives in a polish skill, not this one.

### Retention mechanics: pick the engine

Points, badges, and leaderboards are both the most-added and the most-retired mechanics in product history — LinkedIn's Top Voice badges, Foursquare's mayorships, and Google News badges were all killed for rewarding presence over the behavior the product needed. They are the scoreboard of a game, not the game. Before adding any mechanic, choose the emotional engine the loop runs on:

| Engine | How it works | Use when |
|---|---|---|
| **Completion drive** | An open loop demands closure — a 90%-filled ring, 2 of 3 questions answered. The pull is toward finishing, and it resets fresh each day. | Default. The daily unit has a natural "done" state. Apple's rings drove measured real-world behavior change with no points at all. |
| **Anticipation** | A reward is coming and its size is unknown. Reveal one item at a time — each reveal is its own event. | There's something to reveal: an insight, a weekly reading, a variable payoff. Recharges instead of burning out. |
| **Fear of loss** (streaks) | The user protects what they built. It works — then shifts from "I want to" toward "I can't miss a day" the longer it runs, and it is the design regulators now target. | Only with the escape hatch built in: the user chooses the goal level, can pause or repair, and a miss forgives by design. A streak the user can't pause, influence, or escape is the flagged pattern. |

Whichever engine you pick:

- **One engine, not a stack.** Mechanic richness follows an S-curve — past the peak, each added mechanic *reverses* engagement. The fully-gamified case study (quests, HP, and stats bolted onto daily tasks) produced counterproductive effects in 100% of studied users: they managed the game instead of doing the work. One engine, plus at most one competence or social layer.
- **Signal competence, not presence.** Gamification reliably makes users feel recognized and connected, and does almost nothing for competence — the need most tied to long-term intrinsic motivation. Include one mechanic that proves the user got better at the real thing: a rating that moves, a personal record auto-flagged, a count that stands for real completed work (a 100-ride badge that means 100 actual rides). A mechanic that only proves they opened the app is theater.
- **If competition, make it winnable.** One global leaderboard is a podium for three users and a demotivator for everyone else. Many hyper-local competitions — this hill, this cohort, this week — are winnable, and winnability, not the leaderboard, is what predicts competitive motivation.
- **Measure the behavior, not the app time.** The mechanic exists to drive the real-world behavior: runs logged, nights journaled, lessons finished. Engagement rising while the behavior doesn't is the definition of engagement theater.

**Show the value back — the scoreboard, not the tool.** The most underused retention surface in B2B is a summary of what the user actually achieved: "this month: 30 hours saved, 26 leads found, $18K attributed," tied to their own work, not app-usage stats. Buyers must justify the subscription to a boss or to themselves; if you don't show the value, they assume it's low — they never guess high. This is the honest half of "signal competence": prove the product did the job.

**Motion earns its place or it goes.** The test is whether it tells the user something. Completion confetti and a skeleton fade inform; scrolljacking, parallax, and elements flying in from the edge don't — they read as amateur. Prefer a "load more" button to infinite scroll: it gives the user control and lets them reach the footer.

Caution: delight cannot rescue a badly framed flow. A charming mascot on a form that asks before it gives is still a form that asks before it gives. And beware the famous case studies — the products credited to "delight" also shipped new features, curriculum and marketing in the same window. Correlation gets sold as causation in this space constantly.

## Part 4 — Landing pages (do they buy?)

The landing page is where a vibe-coded product loses most of its visitors, and the fixes are presentation, not complexity. A visitor should get, without effort, a clear reason to be here, a clear reason to buy, and a clear sense of what's being sold.

**Get out of template territory.** The alternating text-left / image-right rows repeating down the page are the signature of generated slop — stack the hero and let it breathe instead. Replace stock photos with a real screenshot of the product. Make every call-to-action say the *exact* same thing: mixing "Get started", "Try a demo", and "Start free trial" breaks the mental model that same label = same destination.

**Copy shifts from what it does to how it helps.** "Collect and analyze your data" is descriptive and fine; "Turn your data into decisions" promises the outcome — the same feature, and the single biggest jump on the page.

**Curate the visual, then add depth.** Don't dump the whole dashboard — crop the screenshot to the one part that proves the section's point, so the reader doesn't hunt for what to notice. Swap a row of four identical cards for a bento grid, so different content gets different room. Interactivity is the clearest signal a person designed this. Small trust touches carry weight: a badge, a row of customer logos, a mega menu that quietly says the product has depth worth exploring. None of it needs custom illustration, 3D, or a freelancer — it's the components you already built.

**Steal deliberately.** Keep a folder of screenshots from apps and sites you admire (Dribbble, Mobbin). Feed them to the AI as the target — "match this" — instead of accepting its defaults.

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
12. Is the retention loop running on fear of loss without an escape hatch — no user-chosen goal, no pause, no repair? Or is more than one engine stacked?
13. Do all the mechanics prove presence (opens, streaks) while none proves competence — that the user got better at the real thing?
14. Does more than one page answer the same question — the same KPI cards repeated across pages (the AI-repetition tell)? Does any page carry what its one intent doesn't need?
15. Is a dense card or row un-compressed — every button, chip, and timestamp at equal weight instead of collapsed into a menu and quieted?
16. Was the screen only ever tested with tidy demo data, never with real, long, missing, or overflowing values?
17. Does a wait show blank instead of a skeleton or a progress indicator?
18. Does a destructive, expensive, or final action fire silently — no confirmation before, no explicit completion state or undo after?
19. Is the same action named differently across screens (delete / remove / trash)?
20. Landing page: alternating text/image rows, stock photos, inconsistent CTA labels, descriptive instead of outcome copy, or a full-dashboard screenshot where a crop would do?
21. In B2B, is there no scoreboard showing the value the product actually delivered?
22. Does any motion fail to inform — decoration, scrolljacking, or infinite scroll with no way to reach the footer?
23. Does a structural landmark (logo, nav, footer, mobile menu) sit off the pattern people expect — moved for originality, or for a UX win that only holds on paper?
24. Is a set of reasons to buy, or a pricing tier, dumped flat and un-grouped — every tier repeating the whole feature list instead of "everything in Basic, plus:"?

## Never Trade Accessibility for Conversion

Loss aversion makes the exit *heavier*, never *harder to reach*. Shrinking a hit area, hiding the dismiss, or dropping its contrast is a dark pattern, not a principle. The weight belongs in the label ("I'll risk it"), never in the tap target — an accessible 44pt dismiss with honest copy beats a 28pt one every time. Hover-only actions need a keyboard and touch path too. If a polish or a11y rule says "enlarge this target", it wins. No exceptions.

## Common Mistakes

- **Blurring the result behind a paywall.** Kills reciprocity. Show the partial result; charge for depth.
- **Confusing dark patterns with these principles.** Fake countdowns and invented scarcity are lies. Loss aversion works only when the loss is *real*.
- **Being creative with the frame instead of inside it.** A layout that moves the landmarks reads as broken, not original — and the visitors it loses leave without telling you why.
- **Decorative color on a dashboard.** On a landing page you can get away with it. On a data view, color that doesn't encode meaning is noise.
- **Fixing the pixels instead of the framing.** Radius and shadows don't fix a screen that asks before it gives.
- **Designing against demo data.** Tidy examples hide the truncation, empty, and overflow problems every real user hits first.
- **The silent destructive action.** No confirm, no completion state, no undo — the user can't tell it worked and can't take it back.
- **The template landing page.** Alternating text/image rows and stock photos tell a visitor the product was vibe-coded before they read a word.
- **Porting Part 1's loss aversion into the retention loop.** Loss framing converts a *decision*; as a daily engine it curdles into obligation and a fear ping at 11pm. Retention runs on closure or anticipation first — fear only with the escape hatch built in.

## Research

Choice overload (Iyengar & Lepper), endowed progress (Nunes & Drèze), reciprocity (Cialdini), the IKEA effect (Norton, Mochon & Ariely), loss aversion (Kahneman & Tversky), the contrast effect, the Zeigarnik effect (unfinished tasks stay salient), and the Doherty threshold / perceived-performance work behind skeleton screens. On retention mechanics: the S-curve of gamification richness (Frontiers in Psychology, 2025), streak obligation (The Decision Lab; Snapchat adolescent study, 2023), the competence gap (Springer Nature meta-analysis, 2024), winnability in competition (ScienceDirect, 2022), and the Gestalt principle of closure. On layout convention and chunking: Jakob's Law, MAYA (Raymond Loewy), and the working-memory limit (Miller, 1956, revised toward roughly four items by Cowan, 2001).

The percentages here are secondhand and unverified against the original papers. Use them to pick a direction, never to justify a decision in writing — check the primary source first.
