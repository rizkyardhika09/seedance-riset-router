# Provider Registry

## Purpose
Central registry for all provider adapters supported by 9router.

## Provider Metadata
- id
- display_name
- version
- capabilities
- supported_models
- authentication_type
- health_status

## Registration Flow
1. Register adapter
2. Validate required interface
3. Advertise capabilities
4. Accept routing requests

## Routing Strategy
- Explicit provider selection
- Automatic capability matching (future)
- Health-aware routing (future)

Status: Draft
Validation: Lock after multiple provider implementations.