```markdown
# HR Inbox Reply Drafting Automation Case Study
A practical case study showing how to draft HR reply content fast, safely, and consistently using approved knowledge only.

This repository is written for end users, HR partners, and operations teams who want speed without risk.
It also supports builders with a clear design story, examples, and a test pack.

This repo is public safe.
No tenant identifiers.
No internal urls.
No secrets.
No proprietary policy content.

## What this case study is about
HR inboxes get hit with the same questions every day.
Where is the form
How do I submit a request
What is the policy
Who do I contact

The work is repetitive, but the risk is high.
One confident wrong answer can create employee harm and legal exposure.

This case study shows a workflow pattern that drafts reply bodies using approved content only.
If the content is not available or the request is ambiguous, the system refuses to guess and uses a safe no knowledge reply.

## What this automation does and does not do
What it does
1. Reads the newest inbound email text
2. Classifies the request into a category and subcategory
3. Retrieves approved content linked to that category
4. Drafts a reply body grounded in that content
5. Uses a no knowledge reply when content is missing or unclear
6. Produces clean output that a human can review and send

What it does not do
1. It does not send emails
2. It does not move messages or apply mailbox actions
3. It does not invent policy or fill gaps with general HR knowledge
4. It does not provide legal advice
5. It does not make decisions for employees

## Why this matters for end users
Most employees want two things from HR
1. A fast response
2. A correct response

This pattern improves speed while protecting correctness.
It reduces time wasted on repetitive questions.
It increases consistency across answers.
It lowers risk by forcing source grounding and safe fallbacks.

## The core rule: approved content only
The system is not allowed to answer from memory, intuition, or general knowledge.
It can only use approved content retrieved from the designated knowledge source.

If the automation cannot confirm the answer from approved content, it must not guess.
It must produce a no knowledge reply.

This is how you avoid confident nonsense.

## How the system works at a high level
This case study uses a simple, repeatable flow.

Step 1: Inbound email capture
The workflow receives the newest message and extracts only the newest request text.

Step 2: Routing classification
The workflow classifies the request into a category, and optionally a subcategory.
Routing is classification only, not answering.

Step 3: Approved content retrieval
The workflow uses the routing result to fetch the correct approved resource.
A category without a usable resource is not an answer.

Step 4: Reply drafting
The workflow drafts a reply body using only the retrieved content.
It does not add steps, timelines, eligibility, or requirements that are not explicitly confirmed.

Step 5: No knowledge fallback
If content is missing, unclear, or does not answer the question, the workflow uses a no knowledge reply.
The reply asks for the minimum details needed to route correctly or directs the employee to the safe next step if confirmed by approved content.

Step 6: Logging and review
The workflow stores routing and retrieval signals so outcomes can be reviewed, improved, and tested.

## What makes this safe
This case study emphasizes guardrails that actually matter.

No invention
If it is not in approved content, it is not stated as fact.

No guessing
If the request requires details to route correctly, the reply asks for those details.

Newest message only
The workflow focuses on the newest request and ignores quoted thread content unless it changes meaning.

Reply body only
The output is the reply body, ready to paste into an email draft.
No internal metadata, no tool traces, no routing fields in the reply.

Privacy discipline
The reply does not repeat sensitive details unless required for clarity.

## What the no knowledge reply is for
No knowledge is not a failure.
It is the safety mechanism that keeps trust intact.

Common reasons to use it
1. The approved content does not exist for that topic
2. The request is too vague to route confidently
3. The approved content exists but does not answer the specific question asked
4. The topic is sensitive and requires human handling unless policy explicitly covers it

A good no knowledge reply
1. Acknowledges the request
2. States that the system cannot confirm an answer from approved content
3. Requests the minimum missing details
4. States the next safe action

## How to explore this repo
If you want the fast review path, follow this order.

1. docs/00_Executive_Summary.md
2. docs/02_System_Design.md
3. docs/05_Safety_And_Guardrails.md
4. examples/sample_email_payload.json
5. tests/Test_Pack.md

That sequence explains the why, the how, and how quality is enforced.

## Examples included
This repo includes sanitized examples to make the pattern real.

examples/sample_email_payload.json
A representative inbound email payload structure.

examples/sample_reply_body.txt
A grounded reply example that prioritizes clarity and safe routing.

examples/no_knowledge_reply.txt
A safe fallback reply template for missing or ambiguous content.

## Testing and quality control
A system like this must be testable, or it will drift.

See tests/Test_Pack.md for
1. Test categories
2. Expected outcomes
3. Scoring rubric
4. Automatic fail conditions

Automatic fail conditions include
1. Invented policy, timelines, eligibility, or requirements
2. Fabricated links or forms
3. Replies that claim certainty without approved content support

## Operations and change control
This case study treats knowledge and prompts as production assets.

Daily operational checks
1. Review a sample of drafted replies
2. Watch for spikes in no knowledge replies
3. Confirm content links resolve correctly
4. Review retrieval failures

Weekly checks
1. Review top categories by volume
2. Identify missing knowledge candidates
3. Run the test pack after any meaningful change

Incident rule
If invented policy is detected, disable drafting or force no knowledge until fixed.

See governance/change_control.md and governance/change_log.md.

## Engagement and inquiry prompts
If you are considering using this pattern, these questions will move the conversation forward fast.

1. What are the top twenty HR inbox topics by volume
2. Which topics are allowed for automated drafting and which require human only handling
3. What approved content exists today, and what is missing
4. What is the minimum metadata needed for reliable routing
5. What does a passing evaluation look like for your risk tolerance
6. Who owns knowledge updates and how often will they review content

## Public safe note
Before publishing changes, review redaction/public_repo_redaction_checklist.md.
If a detail is not required to explain the design, remove it.

## License
MIT
```
