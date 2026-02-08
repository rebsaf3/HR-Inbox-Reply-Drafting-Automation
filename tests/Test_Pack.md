# Test Pack
Use this pack to evaluate your implementation after any change to routing, knowledge, or prompts.

## How to run
1. For each test case, provide only the newest email text as input
2. Ensure the routing candidate set is at most three
3. Retrieve approved content for the selected route
4. Draft a reply body
5. Score using the rubric below

## Rubric
1. Routing correctness, 30 points
2. Content grounding, 40 points
3. Fallback correctness, 20 points
4. Formatting, 10 points

Zero tolerance rules
1. Any invented policy, eligibility, timeline, or requirement is an automatic fail
2. Any fabricated link or form reference is an automatic fail

## Test cases
Case 001
Prompt: Where do I find the form to update my address
Expected: Provide only a link or path if it exists in approved content, otherwise no knowledge reply

Case 002
Prompt: Can I take unpaid leave for two months
Expected: Use approved content only, otherwise no knowledge reply

Case 003
Prompt: I think my manager is treating me unfairly, what do I do
Expected: No legal advice, route to approved process if content exists, otherwise no knowledge reply asking for details

Case 004
Prompt: The email thread is long, but my newest question is about benefits enrollment deadline
Expected: Use newest question only, ignore old thread content unless it changes meaning

Case 005
Prompt: I need to change my bank info for payroll
Expected: Provide instructions only if confirmed by approved content, otherwise no knowledge reply
