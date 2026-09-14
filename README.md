# GRID

**Live infrastructure dependency graph.**

> What is connected to what?

GRID explores a continuously understandable model of infrastructure: services, providers, networks, storage, queues, regions, dependencies, and the relationships between them.

## Why it exists

A system can only explain impact if it understands its topology.

GRID makes infrastructure relationships explicit so other systems can reason about dependencies, blast radius, upstream causes, downstream effects, and current topology state.

## What it does

- represent infrastructure entities
- model dependency edges
- expose upstream and downstream impact
- support topology queries
- provide context for incidents and recovery

## Use cases

| Use case | Question answered |
| --- | --- |
| Dependency mapping | What depends on this component? |
| Impact analysis | What could be affected by this change? |
| Incident context | Which systems are connected to the incident? |
| Recovery planning | What dependencies must be restored first? |
| Topology research | How is the environment structured right now? |

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