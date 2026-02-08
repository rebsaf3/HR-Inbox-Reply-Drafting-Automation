# Operations Runbook
This section describes how to operate the automation safely.

Daily checks
1. Review a sample of drafted replies
2. Confirm no knowledge replies are not spiking unexpectedly
3. Confirm content links resolve correctly
4. Review error logs for retrieval failures

Weekly checks
1. Review top categories by volume
2. Identify missing knowledge candidates
3. Run the test pack on the current prompt and routing map

Incident handling
1. If invented policy is detected, disable drafting or force no knowledge until fixed
2. Open a ticket with the full input and output
3. Identify whether the root cause was routing, retrieval, or prompt weakness
4. Patch, then rerun the test pack before re enabling

Change windows
Prefer scheduled changes with a known reviewer and a rollback plan.
