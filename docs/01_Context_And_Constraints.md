# Context and Constraints
HR inboxes have a predictable mix of requests.
1. How do I do X
2. Where is the form for Y
3. What is the policy for Z
4. I have a situation, what should I do

The risk profile is high because HR content is sensitive and often changes. The automation must prioritize correctness and source control over creativity.

Constraints used in this case study
1. The automation must rely only on approved knowledge sources
2. The automation must not use general HR knowledge
3. The automation must not invent policy, timelines, eligibility, or legal guidance
4. The automation must draft a reply body for every message
5. The automation must provide a no knowledge reply when content is missing or ambiguous
6. The automation must work from the newest message only unless older content changes meaning
7. The automation must produce output that is easy to review and send

Non goals
1. Autonomous decisions about employee actions
2. Automatic submission of HR forms
3. Automatic escalation to legal or leadership without explicit workflow rules
