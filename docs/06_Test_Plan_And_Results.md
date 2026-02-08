# Test Plan and Results
A test pack is required. Without tests, updates will silently break behavior.

Test categories
1. Direct policy questions that are covered by content
2. Requests that require a link to a form
3. Ambiguous requests that should trigger clarification
4. Requests with no approved content that must trigger no knowledge
5. Emails that include long quoted threads
6. Tone and formatting checks

Scoring rubric
1. Correct routing, 30 points
2. Correct content grounding, 40 points
3. Correct fallback when missing info, 20 points
4. Output formatting, 10 points

Passing threshold
Eighty five points or higher, plus zero tolerance for invented policy.

See tests/Test_Pack.md for the full set.
