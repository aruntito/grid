# GRID Architecture

GRID represents infrastructure as an evolving dependency graph.

## Flow

```text
DISCOVERY / INVENTORY / TELEMETRY
              │
              ▼
        ENTITY NORMALIZATION
              │
              ▼
         DEPENDENCY GRAPH
          ┌────┴────┐
          ▼         ▼
      UPSTREAM   DOWNSTREAM
       IMPACT      IMPACT
          └────┬────┘
               ▼
        TOPOLOGY CONTEXT
```

## Core model

Nodes represent infrastructure entities. Edges represent typed dependencies. Observations provide evidence for graph state.

## Design principles

1. Dependencies are explicit and typed.
2. Graph state carries observation context.
3. Unknown state is different from absent state.
4. Impact queries must be explainable.
5. Topology should support both humans and machines.