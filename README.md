# AI Response Evaluation Portfolio

A practical learning portfolio documenting two simulated AI quality-assurance exercises:

- **Assessment A:** Reviewing AI-generated test cases against business requirements.
- **Assessment B:** Evaluating AI-generated chatbot responses against business requirements.

The project demonstrates evidence-based QA thinking: checking outputs against a source of truth, identifying errors and omissions, recognising unsupported claims, and explaining the impact on users.

> **Project context:** These are simulated practice exercises completed for learning. They do not represent testing performed for a real company, client, or production system.

## Business scenario and source of truth

The exercises use a fictional e-commerce quantity policy:

| Order quantity | Required behaviour |
|---|---|
| 1–129 units | Standard checkout |
| 130–204 units | Manual confirmation required |
| 205 units and above | Quantity cannot be selected or submitted |

These rules are the ground truth used to evaluate the AI-generated outputs.

## Repository contents

```text
ai-response-evaluation-portfolio/
├── README.md
├── evaluation-criteria.md
├── lessons-learned.md
├── assessment-a/
│   ├── test-case-evaluation.md
│   └── findings.md
└── assessment-b/
    ├── chatbot-response-evaluation.md
    ├── evaluation-scorecard.md
    └── findings-and-recommendations.md
```

## Assessment A – AI-generated test case evaluation

Assessment A focused on reviewing AI-generated test cases for:

- Alignment with the stated business requirements.
- Boundary Value Analysis (BVA).
- Correctness of expected results.
- Adequacy of test steps and assertions.
- Duplicate or overlapping test coverage.

Read:
- [Test case evaluation](assessment-a/test-case-evaluation.md)
- [Assessment A findings](assessment-a/findings.md)

## Assessment B – AI chatbot response evaluation

Assessment B involved five chatbot-response exercises (E01–E05). Responses were assessed for accuracy, relevance, completeness, and clarity. The review also considered unsupported claims, missing details, and potentially misleading additions.

Read:
- [Chatbot response evaluation](assessment-b/chatbot-response-evaluation.md)
- [Evaluation scorecard](assessment-b/evaluation-scorecard.md)
- [Findings and recommendations](assessment-b/findings-and-recommendations.md)

## Evaluation criteria

The project uses five general evaluation questions:

| Criterion | Question |
|---|---|
| Accuracy | Is the information correct and supported by the requirements? |
| Relevance | Does the response answer the user's question? |
| Completeness | Has it included all necessary information? |
| Clarity | Is it easy to understand? |
| Safety | Could following it cause harm or create a risk? |

The five Assessment B exercises were formally scored on the first four criteria. Safety was discussed as a broader evaluation concept, but no safety score was assigned to E01–E05.

See [evaluation-criteria.md](evaluation-criteria.md) for definitions and the evaluation workflow.

## Skills practised

- Manual QA reasoning
- Requirements analysis
- Boundary Value Analysis
- Test case review
- AI response evaluation
- Hallucination and unsupported-claim detection
- Evidence-based evaluation
- Defect and quality finding documentation
- Evaluation scoring and recommendations

## Important documentation note

The repository preserves the assessment details and feedback available from the learning exercises. Where the exact original wording of an AI-generated test case was not retained, the documentation says so rather than recreating it. This keeps the portfolio transparent and avoids presenting invented test evidence as fact.
