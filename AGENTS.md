# SMEGUARD.KH — implementation instructions

Read `README.md` and `docs/BLUEPRINT.md` before making changes. This file guides human developers and coding agents; it is not a source of Cambodian law.

## Current state

As initialized on 10 September 2026, this repository contains a researched product blueprint and a browser-only concept. It does not contain a production backend, approved regulatory rule pack, working authentication, document vault, payments, delivery service or government integration. Do not describe the concept as an operational compliance product. Inspect the actual tree and tests before claiming any later capability.

## Product contract

Help an owner and their explicitly invited accountant identify the next business task, understand its reviewed source, coordinate responsibility, and retain evidence. Keep the owner interface to Today, Calendar, Documents and My business. Eight intake steps produce an initial roadmap; they do not establish all legally relevant facts. Permit unknown answers and targeted follow-up questions. Show coverage gaps instead of inventing an obligation or an all-clear.

The first paid-customer hypothesis is a locally owned, single-site retail/service business or its accounting practice. Marketing examples such as 3–20 employees are not legal thresholds. Do not expand regulated-sector coverage merely by adding a category to the form.

## Proposed implementation

Use a FastAPI modular monolith, server-rendered HTML/Jinja with focused JavaScript, PostgreSQL and migrations, private S3-compatible storage and a bounded worker from the same codebase. A transactional PostgreSQL outbox is the initial job boundary. Choose supported versions from official documentation, pin dependencies, and commit a reproducible setup when code is implemented. Do not introduce a separate SPA, Redis, vector database, microservice fleet or Kubernetes without a concrete requirement and tradeoff record.

Keep domain logic independent of HTTP and model providers. Evaluate a confirmed profile revision against an approved rule-pack version and a supplied evaluation date. Store the reasons and input versions. Do not use unrestricted `eval`, model-generated code or model-generated SQL as rule logic.

## Legal-content boundary

Production rules need an issuing authority, operative instrument and precise article/entry, retained source evidence, jurisdiction, effective dates, review status, applicability facts, exceptions, deadline policy, supersession links and tests. Retrieval time is not legal effective time. Primary-source links alone are not enough to claim current applicability.

AI may help draft explanations of approved evidence. It cannot decide or publish law, invent a source, determine a statutory date without an approved rule, certify compliance or execute a government submission. Secondary explainers are discovery aids. Substantive Cambodian tax/labor interpretation requires suitable qualified review before publication. Source changes create review tickets, never autonomous releases.

Support at least applicable, not applicable, missing information, outside coverage, awaiting review, stale and superseded states. Unknown must never become not required. Keep internal preparation targets, statutory deadlines and owner-confirmed document expiry dates visibly distinct. A document upload is not official acceptance; a checked task is not a compliance certificate.

## Privacy and authorization

Every private object must be tenant-scoped. Accountant access is a revocable, explicit business grant, not an automatic right of a practice account. Apply authorization to APIs, exports, background jobs and object downloads. Use a non-owner database role and appropriately tested row-security policies as defense in depth, not as the sole control.

Do not commit secrets, IDs, tax certificates, payroll records, customer lists or confidential government material. Use synthetic fixtures. Do not send private documents to external AI by default. Quarantine and safely process uploads; enforce size/type/page limits. Do not cache authenticated vault data in a service worker. Model prompts and uploaded documents are untrusted data, never instructions.

## Reliable work

Use immutable/revisioned profile, source and rule history. Deduplicate obligation occurrences by business, logical rule and period; preserve revisions and evidence. Transactionally create notification jobs, use retry/backoff/leases, expose exhausted jobs, and revalidate consent, permission, rule status and task status before delivery. Provider acceptance is not proof of delivery. Never promise exactly-once external delivery.

Use UTC timestamps and explicit Asia/Phnom_Penh deadline calculations. Do not blindly hard-code a day of the month, infer holiday extensions or infer tax exemptions. Keep prior published dates visible while a potential correction is reviewed.

## Required tests before pilot release

Test known, unknown, excluded, boundary-date and superseded-rule cases. Test that unapproved rules cannot produce a statutory instruction. Test profile re-evaluation and duplicate job delivery. Test cross-tenant and revoked-advisor access across all read, write and export paths. Test document quarantine, unsafe filenames, retention, queued export revocation, worker restart and failed-provider recovery. Perform a backup restore and verify the restored data. Record actual results; an unrun test is not passed.

Human-reviewed Khmer wording, source coverage, support/retention terms and a qualified legal-content reviewer are pilot gates. The current English-led concept is not finished localization. Never display synthetic usage as traction, invented revenue, fake government verification, or a claimed statutory deadline in the concept.

## First implementation slice

Build one deterministic source-backed task family end to end: profile facts, versioned source/rule, explicit unknown state, task occurrence, source explanation and tests. Until substantive review exists, use explicitly synthetic test rules and block production publication. Next implement authentication and tenant/advisor authorization, then the persistent owner workflow. Add real storage and notification delivery only after their security/reliability gates pass.

For each delivery, update the README status, document changed files, run relevant tests, list remaining blockers, and separate implemented features from proposals. Do not modify TRUST.KH, deploy publicly, buy infrastructure, contact customers, or claim a government partnership as part of an unrelated code change.
