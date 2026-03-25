---
type: ai-tooling
project: sphynix
status: active
canonical: true
tags:
  - ai
  - plugins
  - obsidian
---
# Plugin Notes for AI

## Installed Plugins Relevant to AI

- `dataview`
- `omnisearch`
- `obsidian-local-rest-api`
- `smart-connections`

## Recommended Use

### Dataview

Use para:

- notas canonicas
- consultas por `type`
- consultas por `status`
- leitura estruturada

### Omnisearch

Use para:

- busca textual rapida
- localizar termos exatos
- recuperar notas por palavra-chave

### Local REST API

Use para:

- integracao externa com agentes
- leitura e escrita automatizada no vault

## Security Rule

- nunca expor ou versionar tokens, chaves ou configuracoes sensiveis do plugin
- dados locais de plugins devem ficar fora do Git quando possivel

### Smart Connections

Use para:

- descoberta semantica
- notas relacionadas
- navegacao por similaridade

## AI Preference Order

1. ler notas canonicas
2. usar Dataview para consultas estruturadas
3. usar Omnisearch para busca textual
4. usar Smart Connections para contexto por similaridade
5. usar Local REST API para automacao externa

## Related Notes

- [[00 - AI Memory Hub]]
- [[16 - AI Search Dashboard]]
- [[99 - AI Context Pack]]
