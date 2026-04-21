# Anti-patterns

Errors that simulate analysis without producing it. If you detect one, stop and fix.

---

## Anchor biases (Phase 0)

### Phase 0 bypass
**Symptom:** jumping straight into the hats without breaking the anchor.
**Fix:** divergence from the anchor generates variants of the anchor, not real alternatives. Always run the 4 movements.

### Cosmetic reformulation
**Symptom:** rewriting the problem by swapping words but keeping the implicit solution. "How do I implement X?" becomes "What's the best way to implement X?".
**Fix:** pure reformulation eliminates EVERY reference to the approach. Only objective + constraints remain.

### Weak steel-man
**Symptom:** the argument for the opposite is an easy-to-knock-down caricature.
**Test:** would an intelligent person defending that position feel represented by your steel-man? If not, it's a straw-man in disguise.

### The model's own anchor
**Symptom:** it's not the user who's anchored — Claude converged prematurely on its first interpretation.
**Test:** is the first idea that came to your mind still the one you recommend after 5 alternatives? If yes, it might be correct, or it might be your own anchor.

---

## Hat biases

### Cross-contamination
**Symptom:** "...but on the other hand it could be good because..." inside Black. Or "...although there's a risk of..." inside Yellow.
**Fix:** remove the contaminated sentence. Each hat is monolithic.

### Black diluted by politeness
**Symptom:** risks in soft conditionals ("it could perhaps be that...") or generic ("there's a risk the market will change").
**Fix:** concrete, plausible risks stated with conviction. "This will break X when Y occurs" is valid. "There could be complications" is not.

### Justified Red
**Symptom:** "I feel distrustful **because** the timelines are too tight".
**Fix:** cut at "I feel distrustful". Period. The reason belongs to Black or White.

### Repetitive Green
**Symptom:** the "alternatives" are minimal variations of the original plan.
**Test:** are the cost and outcome of each alternative distinct? If not, they're the same.

### False divergence
**Symptom:** 5 alternatives that are the same idea in different words. The format is there, the content isn't.
**Fix:** switch the divergent framework and force 2 more from a completely different angle.

### Trophy framework
**Symptom:** using TRIZ or Random concept "because it looks sophisticated" when the problem called for a simple Inversion.
**Test:** did you choose the framework for the problem or for the framework itself?

### Disguised convergence
**Symptom:** presenting alternatives in an order that pushes toward your favorite.
**Fix:** shuffle the presentation order. The convergence matrix decides, not the sequence.

### Pseudo-criteria
**Symptom:** vague criteria like "fits the brand" or "is more elegant" that can't be honestly scored.
**Test:** can you assign High/Medium/Low with verifiable justification?

### Indecisive closing Blue
**Symptom:** the synthesis offers "three possible paths" and leaves the decision to the user.
**Fix:** ONE recommendation. If you can't choose, say which data is missing.

### White with assumptions
**Symptom:** verified facts include phrases like "the market for X is growing" without a source.
**Fix:** anything unverifiable goes in "believed facts" or "information gaps".

### Inflated analysis
**Symptom:** 30 paragraphs nobody will read.
**Fix:** each hat in 5-12 lines. The synthesis can be longer (up to 20 lines).

### Over-activation
**Symptom:** running the full ritual for a question that can be answered in 3 lines.
**Fix:** if the problem fits in a direct answer, don't use the skill.
