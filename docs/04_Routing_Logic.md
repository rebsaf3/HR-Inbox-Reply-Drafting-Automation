# Routing Logic
Routing is the most common failure point, so it must be constrained and observable.

Routing steps
1. Extract newest email body
2. Normalize the text for matching
3. Query routing entries using strong keys first
4. If no strong match, use weaker matches
5. Return a small candidate set, maximum three
6. Choose the best candidate using explicit rules
7. If no candidate meets threshold, route to no knowledge

Normalization guidance
1. Trim whitespace
2. Lowercase
3. Remove signatures when possible
4. Ignore long quoted threads when the newest message is clear

Choice rules example
1. If exactly one strong match exists, select it
2. If multiple strong matches exist, select the one with the most specific key
3. If only weak matches exist, select none unless confidence is high
4. If a selected route has no usable resource, fall back to no knowledge

Observability
Store the selected category and the resource used in logs so reviewers can audit behavior.
