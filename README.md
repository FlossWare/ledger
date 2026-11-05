# FlossWare Ledger

Ledger is a language-neutral, storage-independent, append-only data ledger for portable records, deterministic replay, validation, versioning, and import/export.

It allows independent projects to preserve canonical history and reconstruct their own persistent state without coupling themselves to Ledger's physical storage or to another project's database schema.

## Project status

**Specification first. No implementation is defined or required yet.**

The authoritative contract is [Ledger v1 Specification](specification/v1.md). The [Architecture Overview](docs/architecture.md) explains the boundaries and design constraints behind that contract.

## Core principles

- The specification is authoritative; implementations conform to it.
- The canonical history is append-only and immutable.
- Reads, replay, validation, and interchange operate on portable records.
- Indexes, caches, materialized views, and projections are derived and rebuildable.
- Consumers own their domain models and reconstructed persistent state.
- Storage engines are implementation details behind a storage adapter.
- API paths use `/api/v1/`; representation media types are independently versioned.
- v1 is one cohesive specification. A breaking contract change requires v2.
- Implementations may be written in different languages. Python is the initial implementation target; Java is a planned implementation target.
- No Kafka dependency, broker requirement, or distributed-infrastructure prerequisite.

## Documentation

- [Ledger v1 Specification](specification/v1.md)
- [Architecture Overview](docs/architecture.md)

## Non-goals

Ledger is not a message broker, workflow engine, distributed log platform, ORM, domain database, or replacement for a consuming project's application model. It does not require consumers to adopt its internal storage schema.

## Implementations

No implementation is part of the initial specification baseline. Implementations will be developed only after the v1 contract has been reviewed and stabilized.
