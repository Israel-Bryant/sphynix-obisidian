---
type: ai-dashboard
project: sphynix
status: active
canonical: true
tags:
  - ai
  - dashboard
  - dataview
---
# AI Search Dashboard

## Purpose

Painel de leitura rapida para IA usando `Dataview`.

Use esta nota para localizar rapidamente:

- contexto canonico
- estado operacional
- decisoes
- execucao
- handoff

## Canonical Notes

```dataview
TABLE type, status
FROM "Projetos/Sphynix"
WHERE canonical = true
SORT file.name ASC
```

## Notes by Type

```dataview
TABLE type, project, status
FROM "Projetos/Sphynix"
WHERE type
SORT type ASC, file.name ASC
```

## Active Execution Notes

```dataview
TABLE priority, timeframe, status
FROM "Projetos/Sphynix"
WHERE type = "execution" OR type = "next-actions" OR type = "operating-state"
SORT file.name ASC
```

## Decision and Guardrail Notes

```dataview
TABLE type, status
FROM "Projetos/Sphynix"
WHERE type = "decision" OR type = "immutable-decisions"
SORT file.name ASC
```

## Fast AI Reading Order

1. [[00 - AI Memory Hub]]
2. [[99 - AI Context Pack]]
3. [[10 - Estado Atual]]
4. [[11 - Proxima Acao]]
5. [[12 - Decisoes Irrevogaveis]]
6. [[13 - Fonte de Verdade]]
7. [[15 - Repositorios]]
