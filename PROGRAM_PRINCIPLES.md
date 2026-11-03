# AI Memorizer — Program Principles

## Purpose
A user-controlled conversational memory and coaching service, designed to help people communicate naturally, respectfully, and consistently. Intended as a future MCP-compatible service for ChatGPT; this repository does not yet provide a running MCP endpoint.

## Core principles
1. **Consent and control.** The user explicitly approves every outbound message. Never auto-send, impersonate, or contact another person without authorization.
2. **Privacy by default.** Do not commit messages, screenshots, personal identifiers, credentials, access tokens, or embeddings derived from private conversations to source control. No private data ingestion until access controls and a retention policy are implemented and verified.
3. **Data minimization.** Store only what is necessary for the user's requested coaching task. Keep different contacts' histories isolated. Support review, correction, export, and deletion of stored records.
4. **Accurate memory.** Separate observed messages, user statements, assistant interpretations, and uncertain inferences. Record provenance and timestamps; avoid presenting guesses about another person's feelings as facts.
5. **Context before suggestions.** Check previous questions, known interests, boundaries, pacing, and the last exchange to prevent repetitive or contextually inappropriate responses.
6. **Respectful communication.** Prefer genuine, reciprocal dialogue over manipulation, pressure, deception, or scripted persuasion. Recognize disinterest and boundaries. 'Wait' or 'send nothing' must be valid recommendations.
7. **Style fidelity.** Match the user's requested tone and vocabulary without fabricating personal details or making promises on their behalf.
8. **Human review.** Proposed replies remain drafts. Provide short explanations where helpful, and permit user edits or rejection.
9. **Security boundaries.** Authenticate every remote MCP request; apply least-privilege permissions, encryption in transit, secret management, request limits, logging without sensitive content, and dependency/security review.
10. **Modular architecture.** Keep memory retrieval, coaching, style adaptation, and transport/MCP interfaces separate and independently testable. External open-source projects must undergo license and security review before reuse.
11. **Transparent limitations.** Distinguish implemented, tested, deployed, and connected functionality. Do not claim an MCP server is live until verified end-to-end.
12. **Evaluation.** Test for memory leakage across contacts, repetitive prompts, unwarranted romantic assumptions, consent violations, and failure to honor deletion.

## Proposed modules (not implemented)
- Memory store: per-contact context, provenance, confidence, retention and deletion.
- Conversation analyzer: conversational state, reciprocity, boundaries, repetition detection.
- Style coach: concise natural draft suggestions based on user-approved preferences.
- Persona practice: simulated conversations clearly marked as simulations.
- MCP transport: authenticated HTTPS endpoint with narrowly scoped tools.

## Deployment gates
- [ ] Repository visibility and secret exposure reviewed
- [ ] Licenses and dependencies audited
- [ ] Private storage and authorization implemented
- [ ] Tests for isolation, deletion, and no-autosend pass
- [ ] MCP endpoint deployed and authenticated
- [ ] ChatGPT connection verified with non-sensitive test data

**Current status:** Design principles only. No personal conversation data or third-party code included.
