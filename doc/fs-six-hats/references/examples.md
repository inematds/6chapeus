# Application examples

## Example 1 — Product feature (with anti-anchor + parallel agents)

**User input:** "I'm deciding whether to add threaded comments to my SaaS for nutritionists. My users are asking for it, I think it's the best move."

### 🛡️ Phase 0 — Anti-Anchor

**Detection:** the user says "I think it's the best". Arrives anchored on "yes, must ship". Clear signal.

**Pure reformulation:** "I have a management SaaS for nutritionists with 23 active users. 4 asked for a collaborative feature. I need to decide how (or whether) to improve communication inside the platform."

**Foundational assumption:** "Users who request features are representative of the total base." Falsification test: it would be false if the 4 are power users and the remaining 19 don't even use half of the current features.

**Steel-man of the opposite:** "Don't add anything and dedicate those 6 weeks to acquiring 20 more users. With 23 users, any new feature is premature optimization. The real problem isn't retention, it's acquisition."

---

### Hats (executed in parallel, each without seeing the others)

### ⚪ White
**Verified:** 4 requests out of 23 active users (17%), no competitor offers that function, team of 1 dev.
**Unverified:** "it would increase retention" (no data), "everybody wants it" (only 4 of 23).
**Gaps:** actual development time, willingness to pay more, current churn.

### 🟡 Yellow
1. Retention through social engagement — plausible: collaborative features increase daily usage in B2B SaaS.
2. Competitive differentiation — plausible: no one in the niche has it.
3. Organic data — plausible: threads generate content usable for recommendations.

### ⚫ Black
1. Legal moderation — High/High — health data is a special category under data protection law; moderation of content is mandatory.
2. Scope creep — High/High — comments drag in notifications, mentions, editing, deletion, reporting: 6-8 weeks minimum.
3. Weak signal — Medium/Medium — 4/23 is 17%, sample too small to decide.
4. Opportunity cost — High/High — 6 weeks with no new user acquisition while you only have 23 active.

### 🟢 Green
**Alt 1 — External channel** *(Framework: J-Elimination)* — Slack/Discord managed by you, zero cost, 1 hour. Insight: eliminates the technical problem entirely.
**Alt 2 — 1:1 messaging between nutritionist and patient** *(Framework: E-SCAMPER/Eliminate)* — No public thread, no legal moderation, 1 week. Insight: covers the real need without the regulatory risk.
**Alt 3 — Research first** *(Framework: D-First principles)* — Before building, validate with the 23 whether they'd pay more. Insight: the irreducible truth is you don't know if this generates revenue.
**Alt 4 — Provocation: the SaaS without a screen** *(Framework: G-Random concept: "telephone")* — What if communication were voice/audio integrated instead of text? Insight: nutritionists prefer to talk, not type.
**Alt 5 — Double down on acquisition** *(Framework: A-Inversion)* — What would guarantee failure? Continuing to add features for 23 users. Insight: invest the 6 weeks in marketing/sales.

### 🔴 Red
- This smells like pleasing the loudest ones.
- Enthusiasm for Alt 2 (1:1 messaging).
- "Everyone's asking" sounds like an excuse to avoid the uncomfortable thing: selling.
- Anticipated fatigue at reading "legal moderation".

### 🔵 Blue (synthesis)

**Map:** 4 of 23 users ask for a complex feature, no retention data, high legal risk, large scope for a solo dev, critical opportunity cost.

**Tensions:** Yellow sells differentiation, but Black dismantles it with real cost. Red confirms enthusiasm for the smaller alternative.

**Matrix:**

| Alternative | Dev time | Legal risk | Revenue potential | Trade-off |
|---|---|---|---|---|
| Alt 1 (Slack) | Low | Low | Low | No control, fragments the experience |
| Alt 2 (1:1) | Medium | Medium | Medium | Covers the need without risk, but doesn't differentiate |
| Alt 3 (Research) | Very low | None | High | Delays the decision, but grounds it in data |
| Alt 5 (Acquisition) | N/A | None | High | Ignores current user requests |

**Recommendation:** Alt 3 (research) this week + Alt 2 (1:1 messaging) if the research confirms demand. Total cost: 1 week.
**Plan B:** if the research shows <30% interest, pivot to Alt 5 (pure acquisition).
**Review metric:** in 3 months, if the base exceeds 100 users and >30% request group discussion, reconsider threads.

---

## Example 2 — Team conflict (summary)

**Input:** "My collaborator missed the deadline and is blaming me in front of the client."
**Variant:** 3 (conflict → Red first)

Phase 0 detects an anchor on "I want to end the relationship". Reformulates as: "I need to decide how to handle a collaborator's breach that was escalated publicly."

The 6 agents operate in parallel. Red (presented first but executed in parallel) captures anger, betrayal, and shame without justifications. White gathers dates and messages. Green generates options from a private conversation to a clean exit with the client intact.

Synthesis: private conversation within 24h with 3 points prepared in writing. If there's no acknowledgment, orderly exit within 48h.
