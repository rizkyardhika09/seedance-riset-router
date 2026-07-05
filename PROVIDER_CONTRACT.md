# Provider Contract

## Purpose
Define the minimum interface every provider adapter must implement.

## Required Operations
- authenticate()
- health_check()
- submit_job()
- get_job_status()
- get_result()
- cancel_job()

## Input Contract
- model
- prompt
- assets
- parameters

## Output Contract
- job_id
- status
- progress
- outputs
- error

## Requirements
- Map provider-specific states to canonical states.
- Normalize errors using ERROR_MODEL.md.
- Preserve provider metadata where possible.

Status: Draft
Validation: Lock after first provider implementation.