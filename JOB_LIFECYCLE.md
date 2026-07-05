# Job Lifecycle

## Canonical States

1. CREATED
2. QUEUED
3. RUNNING
4. COMPLETED
5. FAILED
6. CANCELLED

## Valid Transitions

CREATED -> QUEUED
QUEUED -> RUNNING
QUEUED -> CANCELLED
RUNNING -> COMPLETED
RUNNING -> FAILED
RUNNING -> CANCELLED

## Terminal States
- COMPLETED
- FAILED
- CANCELLED

## Required Metadata
- job_id
- created_at
- updated_at
- provider
- model
- progress
- status

Status: Draft
Validation: PoC required before locking.