---
type: execution-log
project: sphynix
status: active
canonical: false
tags:
  - ai
  - log
  - execucao
  - apple
---
# Log de Execucao Recente

## 2026-03-26 - App Store Connect travado na submissao iOS

### Contexto

- build iOS gerada no Codemagic com sucesso
- compilacao `1.0.1 (8)` validada pela Apple
- bundle id confirmado: `com.sphynx.barberflow`
- assinaturas removidas da tentativa atual

### Problema observado

- a pagina da versao no App Store Connect nao deixa salvar nem seguir com consistencia
- o console do navegador mostrou erros internos da Apple e conflito de estado da versao

### Sinais tecnicos relevantes

- `409` em `iris/v1/appStoreVersions/...`
- `500` em endpoints ligados a review submission
- `No route found ... /version/inflight`
- `Mount element [object Object] not found`
- `An array is needed to render meta tags`

### Leitura operacional

- a build parece valida
- o problema mais provavel esta no registro da versao no App Store Connect, nao no binario
- ha forte indicio de estado quebrado da ficha atual da versao

### Proximo passo recomendado

1. retomar descansado
2. tentar criar uma nova versao limpa no App Store Connect
3. anexar a build valida sem assinaturas
4. se o conflito persistir, abrir chamado no suporte da Apple com o contexto acima

### Observacao importante

- premium nativo no iPhone continua bloqueado por design nesta fase
- nao reintroduzir assinaturas na submissao ate o fluxo da Apple ficar estabilizado
