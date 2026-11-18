# Assessment A – AI-Generated Test Case Evaluation

## 1. Objective

Review AI-generated test cases for a simulated e-commerce quantity feature. The objective was to check whether test cases reflected the business rules and provided useful coverage.

This was a learning exercise, not testing of a live product.

## 2. Business requirements (ground truth)

| Order quantity | Expected behaviour |
|---|---|
| 1–129 units | Standard checkout |
| 130–204 units | Manual confirmation required |
| 205 units and above | Quantity cannot be selected or submitted |

## 3. Areas reviewed

Assessment A involved reviewing generated test cases for:

- Correct interpretation of the quantity ranges.
- Boundary-value coverage.
- Correct expected results.
- Clear test steps and observable assertions.
- Duplicate or overlapping test coverage.

The assessment also included a mini-challenge on identifying duplicate tests and a boundary-value exercise.

## 4. Boundary Value Analysis notes

For the standard-checkout range (1–129):

| BVA category | Value | Explanation |
|---|---:|---|
| Lower boundary | 1 | Smallest permitted quantity |
| Representative normal value | 100 | A value inside the valid range |
| Upper boundary | 129 | Largest quantity eligible for standard checkout |

Values such as 30 and 80 are also valid normal values because they fall inside the range. A normal value is not one fixed number.

Important transition values across the full policy:

| Value | Why it matters |
|---:|---|
| 1 | Lower limit of permitted quantities |
| 129 | Last quantity eligible for standard checkout |
| 130 | First quantity requiring manual confirmation |
| 204 | Last quantity requiring manual confirmation |
| 205 | First quantity that cannot be selected or submitted |

## 5. Test-case review principles

### Expected results must match requirements

A test case may use a valuable boundary value but still be incorrect if its expected result does not match the stated business rule.

### Assertions should be observable

Expected results should describe what a tester can actually verify. For example, for a quantity of 205, the expected result should state that the quantity cannot be selected or submitted.

### Duplicate and overlapping tests are not always the same

Two tests are exact duplicates when they verify the same behaviour under the same conditions. Two tests may overlap while still serving different purposes.

For example:
- Quantity 129 checks the upper boundary of standard checkout.
- Quantity 100 checks a representative value inside the standard-checkout range.

They are not exact duplicates simply because both are in the same range. Their value depends on whether they verify distinct behaviour.

## 6. Learning outcomes

- Identify lower and upper boundaries.
- Select representative normal values.
- Check expected results against the source requirements.
- Distinguish exact duplicates from overlapping coverage.
- Improve test steps and assertions so results are measurable.

## 7. Evidence limitation

The exact original wording of every AI-generated test case and the complete submitted review for each case are not reproduced here because those details are not present in the retained assessment record. This document records the confirmed requirements and learning outcomes without inventing test-case content.
