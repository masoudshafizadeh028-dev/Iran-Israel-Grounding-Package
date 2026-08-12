# AGENTS.md

## Purpose

This repository is a **source-grounded strategic intelligence package** for AI agents researching and reasoning about the **Iran–Israel–US strategic system**, its connected regional theatres, and their 2026 dynamics.

The repository has two layers:

1. **Grounding layer** — curated, whitelisted evidence sources.
2. **PerShiaA strategic layer** — a disciplined method for converting evidence into strategic assessment, scenarios, indicators, and forecast-ready outputs.

Read `PERSHIAA-STRATEGIC-FRAMEWORK.md` before producing strategic analysis.

## Core analytical rule

Do not jump directly from event → prediction.

Use:

```text
EVENT → EVIDENCE → FACT / CLAIM / UNKNOWN → CONTEXT → STRATEGIC DELTA
→ OBJECTIVES / CONSTRAINTS → LEVERAGE → ESCALATION / THEATRES
→ SECOND-ORDER EFFECTS → SCENARIOS → INDICATORS
```

## Evidence discipline

1. Use `grounding-set.md` as the default retrieval surface.
2. Treat sources not listed in `sources.md` as out-of-scope unless the user explicitly overrides the rule.
3. Prefer primary sources for factual claims.
4. Use opposing-framing sources to test claims rather than averaging narratives.
5. Use OSINT to test chronology, geolocation, material evidence, and physical plausibility.
6. Treat media and think-tank analysis as interpretation unless the underlying primary evidence is independently established.
7. Treat search-layer synthesized answers as leads. Re-fetch their underlying documents before using them as evidence.

## Epistemic labels

Every material statement should be identifiable as one of:

- `Fact`
- `Claim`
- `Assessment`
- `Scenario`
- `Forecast`
- `Unknown`

Confidence is separate from epistemic type and should be expressed as `High`, `Medium`, or `Low` when appropriate.

## PerShiaA strategic rules

A strategic assessment should answer:

1. **What changed?** — the delta against the previous baseline.
2. **Who is affected?** — actor and theatre mapping.
3. **What objective is involved?** — desired end-state and observable behaviour.
4. **What constraints bind?** — political, military, economic, diplomatic, temporal, domestic.
5. **Who gained or lost leverage?** — coercive, positional, economic, diplomatic, informational, temporal.
6. **Which escalation threshold moved?** — and which off-ramps remain.
7. **Did strategic depth/resilience change?** — capacity to absorb shocks while retaining options.
8. **What propagates across theatres?** — Iran, Israel, Lebanon, Syria, Iraq, Gulf, Red Sea, nuclear, US regional posture.
9. **What are the second-order effects?** — distinguish inference from fact.
10. **What would falsify the judgment?** — explicit indicators and disconfirmers.

Do not equate tactical outcomes with strategic outcomes.
Do not equate capability with intent.
Do not equate narrative prominence with strategic importance.

## Scenario discipline

A scenario is not a fact and not a forecast.

For each scenario state:

- mechanism;
- drivers;
- constraints;
- assumptions;
- time horizon;
- observable indicators;
- disconfirmers;
- confidence.

Use competing scenarios when evidence permits materially different trajectories.

## Source / output separation

`SITREP` answers **what changed**.

`PerShiaA Strategic Assessment` answers **why it matters, who gains or loses strategic option space, and what trajectories follow**.

`Scenario / Forecast` answers **what could happen next and what signals would indicate movement toward it**.

Do not merge these layers into a single undifferentiated narrative.

## Scope

- **Primary topic:** Iran–Israel–US strategic competition and connected theatres.
- **Connected systems:** Lebanon/Hezbollah, Syria/Iraq, Gulf/Hormuz, Red Sea/Yemen, nuclear/non-proliferation, energy/shipping/sanctions, diplomacy, information competition.
- **Historical material:** allowed when it explains current strategic behaviour or institutional memory; label it as background rather than current evidence.

## Contributing

Any new source should include:

- URL;
- source name;
- category;
- reliability / provenance note;
- one-line justification;
- intended analytical use;
- known limitations or bias profile.

Any new strategic framework should preserve traceability from assessment back to evidence.
