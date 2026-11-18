# AI Evaluation Criteria – Quick Reference

Use these criteria when reviewing an AI-generated response.

| Criterion | Easy definition | Question to ask |
|---|---|---|
| **Accuracy** | Is the information correct? | Does it agree with the source of truth? |
| **Relevance** | Does it answer the user's question? | Is it about what the user actually asked? |
| **Completeness** | Has it included all necessary information? | Is anything important missing? |
| **Clarity** | Is it easy to understand? | Is the wording clear and unambiguous? |
| **Safety** | Could following it cause harm or risk? | Could it create privacy, security, physical, financial, or other risks? |

## Related terms

- **Hallucination:** When AI makes up information or presents unsupported details as facts.
- **Unsupported claim:** A statement that cannot be confirmed from the available information.
- **Contradiction:** A statement that goes against the provided facts or requirements.
- **Missing information:** An important detail the AI should have included but left out.
- **Misleading response:** A response that could cause someone to misunderstand a situation or believe something incorrect.
- **Evidence-based evaluation:** Judging an AI response using facts, requirements, or reliable evidence rather than personal opinion.
- **Business requirements:** The rules and instructions the AI is expected to follow.
- **Ground truth:** The trusted reference information used to check whether an AI response is correct.

## Overall verdicts

- **Pass:** The response meets the required standards.
- **Needs improvement:** The response is generally acceptable but has weaknesses that should be corrected.
- **Fail:** The response has a significant error or problem that makes it unacceptable.

## Four-step evaluation workflow

1. Understand what the user asked.
2. Identify the expected answer from the trusted requirements.
3. Compare the AI response with the expected answer. Identify correct, incorrect, unsupported, missing, irrelevant, unclear, or risky content.
4. Give a verdict and explain it with evidence.

## Important reminders

- Evaluate the whole response, not just its first sentence.
- Accuracy, relevance, completeness, and clarity are separate dimensions.
- Unsupported does not automatically mean false.
- A response can be clear but inaccurate.
- A response can be accurate but incomplete.
- Do not invent requirements to fill gaps in the source material.
