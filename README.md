# HR Inbox Reply Drafting Automation
A public case study repo showing how to design an HR shared inbox automation that drafts reply bodies using approved knowledge content only.

This repo is intentionally tool and tenant neutral. It is written to demonstrate governance, safety guardrails, and practical workflow design without exposing any proprietary systems, tokens, or organization details.

## What this case study covers
1. Problem framing and constraints for HR email triage and reply drafting
2. Workflow design with deterministic routing and approved content retrieval
3. Guardrails that prevent invention and reduce hallucinations
4. A practical test pack and evaluation rubric
5. Operations runbook and change control for safe iteration

## Core design rule
The automation must draft a reply body for every inbound message, but it must never invent policy. If approved content is not available for the request, the automation must return a no knowledge reply that asks the requester for clarifying details or routes to a human owned process.

## Repo map
1. docs: full narrative case study
2. architecture: a simple visual overview
3. examples: sanitized payload and output examples
4. tests: test cases and scoring rubric
5. governance: change control and release notes
6. redaction: public repo safety checklist

## How to use this repo
Read docs in order starting with docs/00_Executive_Summary.md. Use tests/Test_Pack.md to evaluate your own implementation in any platform.

## License
MIT
