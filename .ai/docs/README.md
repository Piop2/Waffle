# Docs

## Structure

- `architecture/` — system structure and design overview
- `decisions/` — technical decision records (ADR)
- `guides/standards/` — conventions and code style
- `guides/features/` — feature-level development guides

## Conventions

- Documents are written in Korean except README
- ADR status must be one of: `proposed` / `accepted` / `deprecated`
- ADR files must follow the format defined in `decisions/_template.md`
- Each document should have a single responsibility — split if it covers multiple topics

## File Naming

- lowercase kebab-case (`payment-flow.md`)
- ADR files prefixed with zero-padded number (`001-use-postgresql.md`)
