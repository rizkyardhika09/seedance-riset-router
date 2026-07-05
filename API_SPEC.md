# API Specification (Draft)

## Base Path
`/v1`

## Endpoints

### POST /video/jobs
Create a new generation job.

Response:
- job_id
- status

### GET /video/jobs/{job_id}
Return current job state.

### GET /video/jobs/{job_id}/result
Return generated assets and metadata.

### POST /video/jobs/{job_id}/cancel
Cancel a running job.

### GET /health
Service health information.

## Canonical Response Fields
- job_id
- status
- progress
- provider
- model
- output
- error

Status: Draft
Validation: PoC Required