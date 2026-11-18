# Assessment B – Findings and Recommendations

## Summary

Five simulated chatbot responses were evaluated against the e-commerce quantity policy. The main issues identified were an incorrect threshold, incomplete guidance, unsupported claims, an omitted restriction, and potentially misleading extra information.

## Consolidated findings

| ID | Exercise | Finding | Recommended improvement |
|---|---|---|---|
| B-01 | E01 | AI used an incorrect threshold of 200 and gave wrong checkout guidance for 150 units. | Apply the exact 130–204 manual-confirmation range. |
| B-02 | E02 | AI stated confirmation was required but did not explain the necessary step before purchase completion. | Explain that manual confirmation must be completed before the order is processed/completed. |
| B-03 | E03 | AI added an unsupported 24-hour estimate and email notification claim. | Include only details supported by the requirements or clearly qualify unknowns. |
| B-04 | E04 | AI discussed checkout prevention but did not explicitly say that 210 cannot be selected. | Address both selection and submission restrictions. |
| B-05 | E05 | AI added an unsupported claim that large orders may require additional verification. | Avoid introducing extra conditions not present in the source requirements. |

## Recommendations

### 1. Ground responses in the requirements

Use the exact business rules when answering quantity questions. Do not invent thresholds or exceptions.

### 2. Avoid unsupported operational promises

Do not invent processing times, notification methods, approval steps, or additional verification requirements. If the source does not specify them, say that the information is not provided or omit it.

### 3. Answer the full question

Identify all parts of the customer's request. For example, “Can I select and submit this quantity?” requires checking both selection and submission behaviour.

### 4. Include the necessary next step

When manual confirmation is required, explain that it must happen before the purchase can be completed, if that is what the requirements establish.

### 5. Keep answers concise and unambiguous

A concise answer that accurately reflects the rules is preferable to a longer answer containing unsupported details.

## Overall conclusion

The exercises show why AI response evaluation must go beyond checking whether the first sentence is correct. Reviewers should inspect every claim, compare it with the source of truth, identify missing information, and explain the likely impact on the customer.

These findings are based on the simulated practice scenario and should not be interpreted as evidence about a real deployed chatbot.
