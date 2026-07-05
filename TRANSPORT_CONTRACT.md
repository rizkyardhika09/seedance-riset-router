# Universal Transport Contract (Draft)

## Purpose
Define a provider-agnostic contract between clients, 9router, and AI providers.

## Lifecycle
1. Submit Job
2. Queue
3. Running
4. Completed | Failed | Cancelled

## Required Operations
- Submit Job
- Get Job Status
- Get Result
- Cancel Job
- Health Check

## Canonical Job States
- QUEUED
- RUNNING
- COMPLETED
- FAILED
- CANCELLED

## Required Job Metadata
- job_id
- provider
- model
- created_at
- updated_at
- status
- progress

## Open Questions
- Retry contract
- Asset upload contract
- Callback/Webhook contract
- Authentication abstraction
- Error normalization

Status: Draft
Validation: Proof of Concept required before locking.