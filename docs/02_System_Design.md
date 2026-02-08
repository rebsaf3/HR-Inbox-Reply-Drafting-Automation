# System Design
High level components
1. Inbound email capture
2. Routing classifier
3. Approved content retrieval
4. Reply drafting
5. Output normalization
6. Logging and quality signals
7. Human review and send step, optional

Deterministic routing
Routing is classification, not answering. The classifier returns a small set of likely categories. The workflow then retrieves approved content linked to the chosen category. If no usable content exists, the workflow uses the no knowledge reply.

Approved content retrieval
Approved content is stored as curated pages or documents. Each routing category maps to one or more resources. Only retrieved content can be used to draft the reply.

Reply drafting
The draft is constrained.
1. Answer only what is supported by retrieved content
2. Use direct quotes only when necessary and short
3. Provide a link or reference to the approved resource when available
4. If content does not answer the question, do not guess

Output
The output is a reply body only, ready to paste into an email client. It should not include internal routing metadata.
