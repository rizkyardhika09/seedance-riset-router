# 9router Framework Analysis

Status: Partially Verified
Date: 2026-07-01

## Verified Findings

### Architecture
- Registry is the single source of truth for providers.
- Provider definitions are colocated in `registry/{provider}.js`.
- Runtime builds four registries:
  - PROVIDERS
  - PROVIDER_MODELS
  - PROVIDER_MEDIA
  - PROVIDER_OAUTH

### Provider Design
Each provider defines metadata, transport, models, aliases, priority, and optional OAuth/media configuration.

### Media Adapter Pattern
Media adapters expose a consistent interface:
- buildUrl()
- buildHeaders()
- buildBody()
- normalize()

This normalizes provider-specific APIs into a unified internal format.

### Capability Registry
Provider media capabilities are registered independently from transport using fields such as:
- imageConfig
- videoConfig
- ttsConfig
- sttConfig
- embeddingConfig
- searchConfig

### Volcengine Ark
Verified:
- Volcengine Ark provider exists.
- Uses official Ark API key.
- Current observed endpoint targets coding chat completions, not Seedance video.
- No verified evidence yet that Seedance is implemented.

## Lessons for Seedance Router
- Use a registry-driven architecture.
- Separate provider metadata from execution logic.
- Normalize request/response through adapters.
- Model capabilities independently from transport.

## Pending Investigation
- Routing engine
- Retry logic
- Fallback strategy
- Provider selection algorithm
- Executor layer