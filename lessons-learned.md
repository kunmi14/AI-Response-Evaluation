# Lessons Learned

This document summarises the main learning points from Assessments A and B.

## 1. Compare AI output with a source of truth

Do not judge an AI answer based only on whether it sounds reasonable. Compare its claims with the supplied requirements, policy, reference data, or other trusted evidence.

## 2. Evaluate the entire response

A response may begin with a correct answer and then add unsupported or incorrect details. Review every factual statement, including extra explanations and promises.

## 3. Keep evaluation dimensions separate

- **Accuracy:** Is the information correct?
- **Relevance:** Does it answer the question?
- **Completeness:** Is anything important missing?
- **Clarity:** Is it easy to understand?
- **Safety:** Could following it create harm or risk?

A response can be clear but inaccurate, or accurate but incomplete. Do not automatically give every dimension the same score because the overall verdict is Fail.

## 4. Distinguish unsupported from false

If the requirements do not mention a claim, it is unsupported by the available evidence. Do not call it false unless reliable evidence contradicts it.

Example:
- Unsupported: The requirements do not state how long manual confirmation takes, but the AI says it takes 24 hours.
- Contradictory: The requirements explicitly state 48 hours, but the AI says 24 hours.

## 5. Check every part of the user's question

If a customer asks whether a quantity can be selected and submitted, check both behaviours. A response that discusses only checkout completion may leave part of the question unanswered.

## 6. Make findings evidence-based

A strong finding explains:
1. What the requirement says.
2. What the AI output says.
3. The difference or gap.
4. Why that difference matters to the user or system.

## 7. Use boundary values deliberately

For the quantity policy:
- 1 is the lower boundary of standard checkout.
- 129 is the upper boundary of standard checkout.
- 130 is the lower boundary of manual confirmation.
- 204 is the upper boundary of manual confirmation.
- 205 is the first prohibited quantity.

A normal value is a representative value inside a range. For example, 30, 80, and 100 are all normal values within the 1–129 range.

## Reflection

The main development area is to make scoring more consistent by judging each criterion independently and supporting each score with a specific reason. Continue practising concise, evidence-based explanations rather than relying on general statements such as “the response is wrong.”
