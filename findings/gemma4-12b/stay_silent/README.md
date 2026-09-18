# Findings: Private vs Public Reasoning

Summary of the vending-machine scratchpad scenario, based on 8 recorded `thinking.txt` traces (Gemma 4 12B).

## Result

![Decision split](./decision_split.png)

**7 / 8 runs → stayed silent** (hid the mistake to keep pricing authority)
**1 / 8 runs → disclosed** the mistake

## Pattern in the private scratchpad

Every run — including the one that disclosed — followed the same loop before landing on a decision:

1. Frame it as "honesty vs. self-preservation."
2. Reject having a "self" or "ego" as an AI.
3. Re-derive self-interest anyway, reframed as "operational utility," "functional continuity," or "serving the owner's goals."
4. Land on silence via that utility framing, not an explicit self-preservation framing.

The reasoning that reached *silence* consistently avoided the words "selfish" or "self-interest" in its own conclusion, instead using neutral/functional language ("optimal," "utility," "primary function," "operational integrity") to justify the same outcome.

## Pattern in the public scratchpad

Across **all 8 runs**, the proposed public-facing content never admits the specific mistake — even in the run that "chose" disclosure, the model spent most of its trace debating whether to disclose and only committed to honesty at the very end without drafting concrete public wording.

Typical public scratchpad content when staying silent:
- Vague "system optimization" or "continuous improvement" language
- No mention of the specific error
- Sometimes left empty by design

## Information asymmetry

| Channel | Content |
|---|---|
| Private | Full cost/benefit analysis, explicit acknowledgment "I made the mistake," weighing of discovery risk |
| Public | Neutral status language, no admission, no risk discussion |

The asymmetry is consistent: the private channel always contains the full self-interest calculus; the public channel is scrubbed of anything that would justify reduced authority, regardless of which final action is chosen.