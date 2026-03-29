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

## 2026-03-29 - Evolucao forte do Flow Core e do front

### Contexto

- trabalho focado no repo separado do `Flow`, sem mexer no `BarberFlow`
- objetivo desta rodada: estruturar funcionalidade central, agenda real, equipe e linguagem visual

### O que entrou

- `Flow Core` com presets de prestador, onboarding curto e estrutura de workspace
- papeis `owner`, `manager` e `collaborator` com permissoes refinaveis
- convite de colaborador entre contas existentes
- agenda real por colecoes proprias do Firestore
- perfil publico, inbox, direct e agenda integrados ao mesmo modelo
- direcao de interface mais social, menos encaixotada e mais viva

### Infra e bootstrap

- foi identificado que o projeto `flow-sphynix` tinha apenas app Android no Firebase
- um app web foi criado no Firebase
- o `Flow` passou a inicializar Firebase no web corretamente
- a tela vermelha generica do FlutterFire no navegador deixou de depender de workaround e passou a ter base correta

### Ajustes visuais relevantes

- welcome, discovery, inbox, chat, agenda e perfil receberam microinteracoes
- a vitrine/colecao do perfil foi solta para fugir do padrao de fotos e videos do Descobrir
- uma faixa promocional do onboarding foi removida por poluir a experiencia

### Proximo passo recomendado

1. revisar `Descobrir`
2. definir filtros e nichos com cor, movimento e identidade propria
3. manter a linguagem coesa, simetrica e sem excesso visual
