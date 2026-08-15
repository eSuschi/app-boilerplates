# Modular Systems – Architecture Notes

## Goals
- Clear module boundaries
- Unidirectional dependencies
- Easy testing and replacement of individual modules
- Long-term maintainability over short-term speed

## Recommended high-level structure

```
src/
  core/           # domain logic, pure business rules
  modules/        # feature modules (each self-contained)
  infrastructure/ # external services, persistence, APIs
  app/            # composition root / wiring
```

## Principles
1. Core never depends on infrastructure.
2. Modules communicate through well-defined interfaces.
3. Side effects are pushed to the edges.
4. Prefer explicit composition over hidden magic.

This document will evolve with concrete boilerplates.
