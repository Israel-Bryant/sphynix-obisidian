---
type: source-of-truth
project: sphynix
status: active
canonical: true
tags:
  - ai
  - source-of-truth
---
# Fonte de Verdade

## AI Summary

Use esta nota para saber onde cada tipo de informacao deve ser buscada ou editada.

## Strategic Truth

Decisoes de produto e estrategia:

- [[05 - Decisao Estrategica do Flow]]
- [[07 - Rede Social e Marketplace]]
- [[12 - Decisoes Irrevogaveis]]

## Operating Truth

Estado e proxima prioridade:

- [[10 - Estado Atual]]
- [[11 - Proxima Acao]]
- [[06 - Lancamento BarberFlow - Fase 1]]

## Technical Truth

Codigo principal do site:

- repo: `https://github.com/Israel-Bryant/sphinyx-shop`
- branch: `main`

Codigo principal do app Flutter:

- repo: `https://github.com/Israel-Bryant/barberflow-sphynix`
- branch: `main`
- pipeline iOS: `codemagic.yaml`
- nota operacional iOS: [[08 - Publicacao iOS sem Mac]]

Arquivos importantes:

- `src/app/page.tsx`
- `src/app/flow/page.tsx`
- `src/app/flow/[slug]/page.tsx`
- `src/app/marketplace/page.tsx`
- `src/lib/flow-products.ts`
- `src/lib/store-links.ts`

## Product Content Truth

Conteudo do BarberFlow:

- editar em `src/lib/flow-products.ts`

Imagens do BarberFlow:

- `public/products/barberflow/`

## Handoff Truth

Quando for passar contexto para outra IA:

- [[04 - Handoff para Outro Codex]]
- [[99 - AI Context Pack]]
