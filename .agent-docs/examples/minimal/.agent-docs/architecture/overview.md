# Architecture Overview (Example)

## L0 System Overview
- Purpose: Example service for demonstration.
- Primary users: Internal developers.

## L1 Component Map
- api/: HTTP handlers and routing.
- core/: domain logic and services.
- storage/: persistence adapters.

## L2 Critical Flows
- Create item: api -> core -> storage.
