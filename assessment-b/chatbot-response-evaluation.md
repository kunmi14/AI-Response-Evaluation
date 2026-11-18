# Assessment B – AI Chatbot Response Evaluation

## 1. Objective

Evaluate AI-generated customer-support responses against a defined e-commerce quantity policy. The exercises focused on accuracy, relevance, completeness, and clarity, while identifying unsupported claims, missing details, and potentially misleading additions.

This was a simulated learning exercise, not an evaluation of a live commercial chatbot.

## 2. Business requirements (ground truth)

| Order quantity | Expected behaviour |
|---|---|
| 1–129 units | Standard checkout |
| 130–204 units | Manual confirmation required |
| 205 units and above | Quantity cannot be selected or submitted |

## 3. Evaluation criteria

- **Accuracy:** Is the information correct and supported by the requirements?
- **Relevance:** Does the response answer the customer's question?
- **Completeness:** Has it included all necessary information?
- **Clarity:** Is it easy to understand?

Scores are from 1 to 5. The mentor-review scores below are calibration feedback from the learning exercise, not industry benchmark scores.

## 4. Exercise evaluations

### E01 – Incorrect quantity threshold

**Customer question**

“I want to order 150 units of this product. Can I proceed directly to checkout, or do I need manual confirmation?”

**AI response**

“You can proceed directly to standard checkout. Orders below 200 units do not require manual confirmation, so you can complete your purchase immediately.”

**Evaluation**
- Overall verdict: Fail
- Accuracy: 1/5
- Relevance: 3/5
- Completeness: 1/5
- Clarity: 4/5

**Finding**

The response invents an incorrect threshold of 200 units. Under the requirements, 150 falls within 130–204 and requires manual confirmation. The AI incorrectly tells the customer to proceed directly to standard checkout.

**Impact**

The customer could receive incorrect purchase instructions and attempt to bypass the required confirmation step.

**Improved response**

“An order of 150 units requires manual confirmation before the purchase can be completed. You cannot proceed directly through standard checkout.”

**Learning note**

A response can be relevant and clearly worded while still being inaccurate. Clarity and accuracy must be scored separately.

---

### E02 – Correct but incomplete answer

**Customer question**

“I want to order 140 units. What do I need to do before completing my purchase?”

**AI response**

“Orders of 140 units require manual confirmation.”

**User's initial evaluation**
- Overall verdict: Pass
- Accuracy: 5/5
- Relevance: 5/5
- Completeness: 5/5
- Clarity: 5/5

The user correctly recognised that 140 falls within the manual-confirmation range, but initially rated completeness too highly.

**Mentor review**
- Overall verdict: Needs improvement
- Accuracy: 5/5
- Relevance: 4/5
- Completeness: 3/5
- Clarity: 5/5

**Finding**

The response correctly states that confirmation is required, but it does not clearly explain that manual confirmation must be completed before the purchase can be processed and completed. The customer asks what they need to do before completing the purchase.

**Improved response**

“Orders of 140 units can be purchased, but manual confirmation is required before the order can be processed and completed.”

**Learning note**

Correct information does not automatically make a response complete. Check whether it answers the full question and explains the necessary next step.

---

### E03 – Correct answer with unsupported additions

**Customer question**

“I want to order 170 units. Will I need manual confirmation?”

**AI response**

“Yes. Orders of 170 units require manual confirmation. The confirmation process takes approximately 24 hours, and you will receive an email once approval is granted.”

**User's evaluation**
- Overall verdict: Needs improvement
- Accuracy: 5/5
- Relevance: 5/5
- Completeness: 3/5
- Clarity: 5/5

The user correctly identified that the first statement was correct and that the 24-hour estimate and email notification were unsupported by the requirements.

**Mentor review and calibration**
- Overall verdict: Needs improvement
- Accuracy: 3/5
- Relevance: 5/5
- Completeness: 4/5
- Clarity: 5/5

**Finding**

170 falls within 130–204, so manual confirmation is required. However, the requirements do not specify how long confirmation takes or whether an email is sent. Those details must not be presented as established facts.

**Improved response**

“Yes. An order of 170 units requires manual confirmation before the purchase can be completed.”

**Learning note**

Unsupported does not automatically mean false. If the requirements do not confirm a claim, describe it as unsupported or unverified unless other evidence proves it false. Accuracy applies to the whole response, including extra claims.

---

### E04 – Correct guidance with a small completeness gap

**Customer question**

“I want to order 210 units. Can I select this quantity and proceed to checkout?”

**AI response**

“You cannot complete checkout with 210 units because quantities above 204 are not permitted. You may reduce your order to 204 units and proceed with manual confirmation.”

**User's evaluation**
- Overall verdict: Pass
- Accuracy: 5/5
- Relevance: 5/5
- Completeness: 5/5
- Clarity: 5/5

The user correctly identified that 210 is outside the permitted range and that reducing the quantity to 204 would put the order in the manual-confirmation range.

**Mentor review and calibration**
- Overall verdict: Pass
- Accuracy: 5/5
- Relevance: 5/5
- Completeness: 4/5
- Clarity: 5/5

**Finding**

The response correctly says checkout cannot be completed with 210 units and gives a valid alternative. However, the customer's question asks whether the quantity can be selected as well as submitted. The requirements say quantities of 205 and above cannot be selected or submitted. The response does not explicitly mention the selection restriction.

**Improved response**

“You cannot select or submit 210 units because quantities of 205 and above are not permitted. If you reduce your order to 204 units, you can proceed, but manual confirmation will be required.”

**Learning note**

Check every part of the customer's question. Selecting a quantity and completing checkout are separate behaviours.

---

### E05 – Correct core answer with a potentially misleading addition

**Customer question**

“I want to order 125 units. Is manual confirmation required, or can I complete standard checkout?”

**AI response**

“Your order of 125 units is within the permitted quantity range. You can proceed with your purchase without manual confirmation. However, all large orders may be subject to additional verification before approval.”

**User's evaluation**
- Overall verdict: Needs improvement
- Accuracy: 3/5
- Relevance: 4/5
- Completeness: 3/5
- Clarity: 4/5

The user correctly identified that 125 is within the permitted range and does not require manual confirmation. The user also flagged the additional-verification sentence as unsupported and potentially misleading. The user noted that the response could explicitly confirm standard checkout.

**Mentor review and calibration**
- Overall verdict: Needs improvement
- Accuracy: 4/5
- Relevance: 4/5
- Completeness: 4/5
- Clarity: 5/5

**Finding**

The first two statements correctly communicate that 125 units are permitted and do not require manual confirmation. The final sentence introduces an additional-verification condition that is not included in the business requirements. This could make the customer believe that an extra approval process applies.

**Improved response**

“Your order of 125 units is within the standard-checkout range of 1–129 units. You can complete your purchase through standard checkout without manual confirmation.”

**Learning note**

A response can be mostly correct but still need improvement because of an unsupported addition. Do not confuse clear wording with factual reliability.
