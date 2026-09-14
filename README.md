# GRID

**Live infrastructure dependency graph.**

> What is connected to what?

GRID explores a continuously understandable model of infrastructure: services, providers, networks, storage, queues, regions, dependencies, and the relationships between them.

## What it does

- represent infrastructure entities
- model dependency edges
- expose upstream and downstream impact
- support topology queries
- provide context for incidents and recovery

## Architecture

```text
DISCOVERY / INVENTORY / TELEMETRY
              │
              ▼
        ENTITY NORMALIZATION
              │
              ▼
       DEPENDENCY GRAPH
              │
       ┌──────┴──────┐
       ▼             ▼
   IMPACT PATHS   TOPOLOGY STATE
       │             │
       └──────┬──────┘
              ▼
       OPERATIONAL CONTEXT
```

## Ecosystem

GRID supplies topology context to `PULSE`, `TRACE`, `BLACKBOX`, `RECOVER`, and `FIRSTLIGHT`. `GHOST` extends discovery into unknown infrastructure.

## Status

Early research and architecture.

- [Architecture](docs/architecture.md)
- [Roadmap](docs/roadmap.md)

## License

MIT.