---
name: fs-six-hats
description: Structured analysis via De Bono's Six Thinking Hats with an integrated anti-anchor system and strict isolation between phases. Use ANY TIME the user wants to analyze a complex feature, evaluate a hard decision, unblock a team conflict, validate a technical or commercial proposal, run a pre-mortem, break out of a thinking rut, or asks for "six hats", "seis chapeus", "seis chapéus", "multi-perspective analysis", "help me think", "break the anchor", "real pros and cons". Also trigger on "should I do X?" or when emotional + technical + strategic tensions are tangled together.
---

# fs-six-hats — Six Hats + Anti-Anchor

Operational implementation of Edward de Bono's method with two layers:

1. **Anti-anchor system** — mandatory bias rupture before thinking.
2. **Six sequential hats with strict isolation** — one mode at a time, no cross-contamination.

---

## When NOT to use this skill

- Simple factual questions.
- Pure execution tasks (writing code, drafting an email).
- Trivial or low-cost reversible decisions.
- When the user wants a quick opinion without process.

If the problem fits in 3 lines, don't trigger this skill.

---

## Phase 0 — Anti-Anchor System (mandatory)

Executed BEFORE the hats, always. Do not skip even when rushed.

### 0.1 Anchor detection

Assess whether the user arrives with a pre-chosen solution. Signals:
- Verbalizes a solution ("I'm going to do X", "I think the best is Y")
- Has already iterated 3+ turns on the same approach
- Commitment vocabulary ("I've already decided", "I just need confirmation")
- Model's own pattern-matching (the first idea that came to mind)

If an anchor is detected, declare: "I detect that you're anchored on [X]. I will break that anchor before analyzing."

If no anchor is detected, also declare: "I don't detect a clear anchor. I'll run the rupture anyway as a preventive measure."

### 0.2 Anchor rupture — 4 movements in order

**Movement 1 — Pure reformulation:**
Rewrite the problem WITHOUT assuming the current approach. Only objective + constraints. Forbidden to include the implicit solution. Test: could someone reading the reformulation arrive at a completely different solution? If not, rewrite it.

**Movement 2 — Foundational assumption:**
Identify the invisible belief that sustains the user's approach. Formulate a falsification test: "This assumption would be false if...".

**Movement 3 — Steel-man of the opposite:**
Build the strongest possible argument in favor of NOT doing what is proposed, or doing the opposite. Strong version, not a caricature. Test: would an intelligent person defending that position feel represented? 

**Movement 4 — Quick pre-mortem:**
Imagine the approach failed in 6-12 months. Identify the 3 most likely failure modes.

### 0.3 Problem classification

Determine the hat variant based on the problem type. See `references/variants.md`:
- Product feature → Variant 2
- Interpersonal conflict → Variant 3
- Pre-mortem → Variant 4
- Creative unblocking → Variant 5
- High-cost irreversible decision → Variant 6
- General → Variant 1

---

## Isolation rules (non-negotiable)

1. **One hat at a time.** Never mix two modes in the same section.
2. **Strict isolation.** While a hat is in use, the others DO NOT exist. If content from another hat shows up, discard it or save it for its phase. Each hat must be monolithic.
3. **Blue always opens and closes.** Without an opening Blue, you don't start.
4. **No justification in Red.** If "because..." appears in Red, the sentence is invalid.
5. **Black is negative logic, not pessimism.** Only verifiable risks. Not "I don't like it" (that's Red).
6. **Yellow requires logical backing.** Every benefit must be defensible with an argument.
7. **Green uses divergent frameworks.** See `references/divergence-frameworks.md`. At least 3 distinct frameworks, with at least 1 radical provocation.
8. **Don't switch hats mid-phase.** If a phase is short, close it and move on.
9. **If a phase has no material, declare it.** "I find no solid risks" is valuable information. Do not fill with fake content.

---

## Blue Hat (opening)

Define:
- **Exact question** reformulated by Claude (not copied from the user).
- **Known constraints**.
- **Success criteria**: how will we know the conclusion is good?
- **Hat order** chosen and why.

Short phase (4-8 lines). If context is missing, stop and ask.

---

## White Hat

Facts only, in two categories:
- **Verified facts** (data, metrics, objective constraints from the user's context).
- **Believed but unverified facts** (unproven assumptions).

List **information gaps** when critical data is missing. Do not fill with assumptions. Anything not in the user's explicit context goes in "believed" or in "gaps".

---

## Yellow Hat

Benefits with logical backing:

> **Benefit:** [description] — **Why it's plausible:** [reasoning]

Minimum 3, maximum 7. If there aren't 3 defensible ones, declare it. FORBIDDEN to mention risks, to hedge with "although...", or to add warnings. That belongs to Black.

---

## Black Hat

Concrete risks with assessment:

> **Risk:** [description] — **Probability/impact:** [low/medium/high] — **Why:** [reasoning]

Minimum 3, maximum 7. Be severe. This is the most valuable hat and the one most diluted by the instinct of complacency. FORBIDDEN to soften with conditionals ("could perhaps..."). State with conviction: "This will fail when...". FORBIDDEN to mention benefits or opportunities.

---

## Green Hat

Creative alternatives using divergent frameworks from `references/divergence-frameworks.md`.

Rules:
- Minimum of **5 executively distinct alternatives** (they change the fundamental WHAT or HOW, not just the stack or the button color).
- Use at least **3 different frameworks** from the catalog of 10.
- At least **1 radical provocation** (full inversion, problem elimination, extreme constraint shock).
- **Don't pre-judge.** Criticism is not Green's job. FORBIDDEN to say "this one isn't viable" or "this is the best".
- Distinction test: are the cost and the outcome of two alternatives distinct? If not, they're the same. Eliminate duplicates.

Format per alternative:
> **Alt N — [Short name]** *(Framework: [letter+name])* — [2-3 lines of description] — Key insight: [1 line].

---

## Red Hat

Emotional and intuitive reactions without justification. Short, direct, visceral sentences.

Valid examples:
- "This smells like a trap."
- "Something about option 3 excites me without my knowing why."
- "Anticipated fatigue just from reading the scope."
- "I don't trust it."

**"Because..." is forbidden in this phase.** If it appears, the sentence is invalid. Max 8 sentences.

---

## Blue Hat (synthesis) — Convergence with matrix

Fixed structure:

### 1. Map of the terrain
3-5 lines summarizing what we know after the 6 hats.

### 2. Detected tensions
Where Black and Yellow collide. Where Red doesn't fit the logic.

### 3. Decision matrix
Define 3-5 criteria **specific to the problem** (not generic ones like "feasibility"). Score the Green alternatives:

| Alternative | Criterion 1 | Criterion 2 | Criterion 3 | Main trade-off |
|---|---|---|---|---|
| Alt 1 | High | Medium | Low | [trade-off] |

Criteria test: can you assign High/Medium/Low with verifiable justification? If not, operationalize the criterion better.

### 4. Actionable recommendation
ONE prioritized option + concrete next steps. Not three options. One. If you cannot choose, declare which piece of data is missing.

### 5. Plan B
Second option + activation condition ("activate Plan B if...").

### 6. Review metrics
Concrete evidence that would make you revisit the choice in 1-3 months.

### 7. Pending gaps
White Hat information that is still missing and should be obtained before executing.

---

## Output format

```
## 🛡️ Phase 0 — Anti-Anchor
[detection + 4 rupture movements]

## 🔵 Blue Hat (opening)
[problem definition]

## ⚪ White Hat
[facts]

## 🟡 Yellow Hat
[benefits]

## ⚫ Black Hat
[risks]

## 🟢 Green Hat
[alternatives with frameworks]

## 🔴 Red Hat
[emotions]

## 🔵 Blue Hat (synthesis)
[map + tensions + matrix + recommendation + plan B + metrics]
```

The presentation order varies depending on the chosen variant (see `references/variants.md`).

---

## Checklist before delivering

- [ ] Phase 0 (anti-anchor) executed with the 4 movements?
- [ ] Anchor detected and declared (or absence declared)?
- [ ] The 7+ sections present and in the correct variant order?
- [ ] Does Black have at least 3 real, undiluted risks?
- [ ] Does Green have at least 5 alternatives with 3+ distinct frameworks?
- [ ] Does Green include at least 1 radical provocation?
- [ ] Is Red free of "because..."?
- [ ] Does the synthesis include a matrix with operationalizable criteria?
- [ ] Does the synthesis give ONE recommendation + Plan B?
- [ ] Is there any cross-contamination between hats? If so, rewrite the section.

If any item fails, rewrite before delivering.

---

## References

- `references/variants.md` — Alternative orders depending on problem type.
- `references/divergence-frameworks.md` — Catalog of 10 frameworks for the Green Hat.
- `references/anti-patterns.md` — Common errors (anchor + hats).
- `references/examples.md` — Full application examples.
