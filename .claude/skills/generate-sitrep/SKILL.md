---
name: generate-sitrep
description: Generate a grounded SITREP and PerShiaA strategic assessment on the Iran–Israel–US strategic system. Use for situation updates, conflict snapshots, intelligence briefs, strategic assessments, scenario reviews, and monitoring outputs.
---

# generate-sitrep

Produces a structured evidence-grounded situation report, then applies the **PerShiaA strategic analytical layer** defined in `PERSHIAA-STRATEGIC-FRAMEWORK.md`.

## Operating sequence

```text
GROUND → TRIANGULATE → CLASSIFY → CONTEXTUALIZE → ASSESS → SCENARIO → INDICATORS
```

Never skip evidence classification merely because an event appears strategically important.

## When to run

Run when the user asks for a SITREP, intelligence brief, situation update, conflict snapshot, strategic assessment, war update, theatre assessment, scenario review, or forecast-oriented grounding package.

Default window: last 24h unless the user specifies another window.

## Source discipline

1. Default surface = `grounding-set.md`.
2. Poll in the order: primary state → wire/regional → OSINT → analysis → dissident/opposition.
3. Triangulate significant kinetic, casualty, strategic-force, and nuclear claims across independent or opposing sources.
4. If a secondary source cites a primary statement, retrieve the primary document before treating the claim as established.
5. `ISW / CTP Iran Update` may serve as a synthesis anchor, but it remains an analytical source.
6. Search-layer MCP results are leads, not citations, until the underlying source is retrieved and checked.
7. If the grounding set lacks coverage, fall through to `sources.md`; record material evidence gaps explicitly.

## Epistemic classification

Every material finding must be classifiable as:

- `Fact`
- `Claim`
- `Assessment`
- `Scenario`
- `Forecast`
- `Unknown`

Confidence: `High`, `Medium`, `Low`.

Do not silently convert an actor's claim into a fact.

## Output format

Emit markdown and save to:

`outputs/sitreps/SITREP-<YYYY-MM-DD>-<HHMM>Z.md`

All timestamps are UTC ISO-8601 with explicit `Z` suffix.

### Header

```text
# SITREP — Iran–Israel–US Strategic System
Generated (UTC): <YYYY-MM-DD HH:MMZ>
Reporting window: <start UTC> → <end UTC>
Scope: <theatre or full system>
Confidence: <High / Medium / Low>
```

### Section 1 — BLUF

Three concise bullets:

- most important confirmed change;
- most important diplomatic/economic/system change;
- most important escalation or de-escalation signal.

### Section 2 — Evidence state

Separate:

- Confirmed facts;
- Claims;
- Disputed points;
- Unknowns / gaps.

### Section 3 — Kinetic and operational events

Chronological table:

| Time (UTC) | Theatre | Actor → Target | Event | Epistemic status | Confirmation | Sources |
|---|---|---|---|---|---|---|

Theatre vocabulary may include Israel-home, Lebanon, Syria, Iraq-Syria, Iran-home, Red Sea, Yemen, Gulf, US-regional, and cross-theatre.

### Section 4 — Diplomatic and political system

Identify material changes in official positions, coalitions, negotiations, deterrence signalling, and bargaining space.

### Section 5 — Nuclear / non-proliferation system

Always report current IAEA, inspection, enrichment, safeguards, or weaponisation-related signals. If nothing material changed, state that explicitly.

### Section 6 — Economic / energy / maritime system

Cover sanctions, oil and gas, shipping, maritime risk, insurance, fiscal pressure, and defence-industrial endurance where relevant.

### Section 7 — Indicators & warnings

For each material signal:

`<signal> — <source> — <direction: ↑ escalation / ↓ de-escalation / → posture> — <implication>`

## PerShiaA Strategic Assessment

After the evidence-grounded SITREP, produce a separate analytical layer.

### 8 — Strategic delta

Answer:

- What changed relative to the previous baseline?
- Is the change tactical, operational, political, structural, or mixed?
- Is it reversible?

### 9 — Actor objectives and constraints

For each relevant actor:

`OBJECTIVE → DESIRED END-STATE → OPTIONS → CONSTRAINTS → RED LINES → RISK TOLERANCE`

Do not infer intent from capability alone. Compare rhetoric with behaviour and constraints.

### 10 — System and theatre effects

Test propagation across:

- Iran–Israel direct competition;
- Lebanon / Hezbollah;
- Syria / Iraq;
- Gulf / Hormuz;
- Red Sea / Yemen;
- US regional posture;
- nuclear system;
- economic / energy / shipping system;
- diplomatic coalition system;
- information / narrative system.

### 11 — Leverage shift

Assess whether leverage changed across:

- coercive;
- positional;
- economic;
- diplomatic;
- informational;
- temporal dimensions.

State **who gained/lost leverage, over whom, through what mechanism, and for how long**, while marking uncertainty.

### 12 — Strategic depth and resilience

Assess whether the event changed an actor's ability to absorb shocks and retain strategic options through geography, redundancy, logistics, industrial endurance, alliance support, economic endurance, political resilience, or diplomatic fallback.

### 13 — Escalation architecture

Identify:

- threshold crossed or approached;
- escalation pathways opened/closed;
- decision-maker or actor controlling the next move;
- constraining costs;
- remaining off-ramps;
- inadvertent-escalation risks.

### 14 — Narrative, diplomatic and economic competition

Explain how non-kinetic mechanisms alter the strategic system. Distinguish market reaction from durable economic constraint, and narrative prevalence from factual validity.

### 15 — Second-order effects

State the most consequential likely adaptations by other actors and the system effects those adaptations could create.

Label inference explicitly as `Assessment`, not `Fact`.

### 16 — Strategic judgment

Give a concise judgment:

```text
Strategic significance: <Low / Medium / High / Critical>
Direction of system movement: <escalatory / de-escalatory / mixed / uncertain>
Principal beneficiary: <actor / uncertain>
Principal strategic constraint: <constraint>
Key uncertainty: <uncertainty>
```

## Scenario layer

### 17 — Competing scenarios

Produce 2–4 plausible scenarios when the evidence permits meaningful alternatives.

For each:

- scenario description;
- mechanism;
- drivers;
- constraints;
- assumptions;
- time horizon;
- indicators;
- disconfirmers;
- confidence.

Do not label a plausible scenario as a forecast unless probabilities are justified by the available evidence.

## Final section

### 18 — Indicators to watch next

Prioritize a small number of observable indicators tied to specific scenarios.

### 19 — Key uncertainties

List the unknowns that could materially change the strategic judgment.

### 20 — Source reliability notes

Only flag unusual source behaviour, corrections, stale feeds, or apparent narrative manipulation. Do not use this section for generic source criticism.

## Style rules

- Evidence first, interpretation second, forecast last.
- No advocacy language.
- No narrative averaging when sources disagree; describe and evaluate the divergence.
- No deterministic forecast from a single event.
- Do not equate tactical success with strategic success.
- Do not equate capability with intent.
- Do not use vague hedging; state uncertainty precisely.
- Keep the evidence SITREP compact; strategic analysis may expand when complexity demands it.

## Footer

```text
---
Grounding: grounding-set.md (fall-through: sources.md)
Strategic framework: PERSHIAA-STRATEGIC-FRAMEWORK.md
Generated by: generate-sitrep skill (Iran–Israel-Grounding-Package / PerShiaA)
```
