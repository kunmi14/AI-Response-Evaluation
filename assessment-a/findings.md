# Assessment A – Findings and Recommendations

## Scope

These findings summarise the confirmed learning points from the AI-generated test-case review. They are not claims about defects in a live application.

## Findings

### A-01 – Boundary values must be interpreted correctly

**Observation:** The quantity rules change at 129/130 and 204/205.

**Expected requirement:**
- 1–129: Standard checkout.
- 130–204: Manual confirmation.
- 205 and above: Quantity cannot be selected or submitted.

**Recommendation:** Include tests at the transition values 129, 130, 204, and 205. Verify the exact expected behaviour at each boundary.

### A-02 – Expected results must be grounded in requirements

**Observation:** During the assessment, the review process identified that a generated test case can use a relevant quantity but still have an incorrect expected result.

**Recommendation:** Validate each expected result against the source requirement before accepting an AI-generated test case.

### A-03 – Test steps and assertions need sufficient detail

**Observation:** A test case is difficult to execute or assess consistently if its steps or expected results are vague.

**Recommendation:** Specify the action, the relevant quantity, and the observable system response. For prohibited quantities, explicitly verify both selection and submission restrictions.

### A-04 – Distinguish duplicates from overlapping coverage

**Observation:** Two tests can cover the same general range without being exact duplicates. A boundary test and a normal-value test can provide different coverage.

**Recommendation:** Document the purpose of each test and retain it when it checks a distinct risk or behaviour.

## Overall recommendation

Use AI-generated test cases as drafts, not as automatically trusted test assets. A QA reviewer should verify requirement traceability, boundary values, expected results, steps, assertions, and coverage overlap before approving them.

## Evidence note

The retained record does not contain the complete original wording of all generated test cases. These findings therefore describe the confirmed review principles and scenario requirements, not reconstructed individual defects.
