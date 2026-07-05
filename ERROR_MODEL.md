# Error Model

## Purpose
Normalize provider-specific errors into a common format.

## Canonical Error Codes
- INVALID_REQUEST
- AUTHENTICATION_FAILED
- AUTHORIZATION_FAILED
- RATE_LIMITED
- PROVIDER_UNAVAILABLE
- JOB_NOT_FOUND
- JOB_FAILED
- TIMEOUT
- INTERNAL_ERROR
- UNKNOWN_ERROR

## Standard Error Response
- code
- message
- provider
- provider_code
- retryable
- timestamp

## Retry Policy
Retry only when `retryable=true`.

Status: Draft
Validation: Update after first provider integration.