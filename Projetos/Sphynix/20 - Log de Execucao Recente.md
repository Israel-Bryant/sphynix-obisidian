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

## 2026-04-01 - Reset da frente Apple e novo app record

### Contexto

- a build `1.0.1 (11)` foi gerada no Codemagic e validada com sucesso
- o binario novo confirmou `Criptografia nao isenta: Nao`
- mesmo com build nova, screenshots preenchidas e compilacao anexada, o App Store Connect seguia retornando `PATCH ... appStoreVersions ... 409 (Conflict)`
- a ficha antiga foi finalmente removida para parar de desperdiçar tempo operacional

### O que ficou provado

- o problema nao estava no binario do app
- o problema nao estava nas capturas de tela
- o problema nao estava na chave de criptografia do `Info.plist`
- o problema estava no registro/ficha de submissao da Apple

### O que foi feito

- `ITSAppUsesNonExemptEncryption = false` foi adicionado no projeto iOS
- o CI do Codemagic foi ajustado para ignorar o subprojeto `public_booking_web` na analise da raiz
- a build `1.0.1 (11)` foi aceita pela Apple
- um novo App ID / app record iOS foi criado com o bundle id `com.sphynx.barberflowapp`

### Proxima sequencia correta

1. atualizar o projeto Flutter/iOS para `com.sphynx.barberflowapp`
2. recriar o app iOS no Firebase
3. trocar o `GoogleService-Info.plist`
4. atualizar o `codemagic.yaml` e o signing
5. gerar nova build e anexar no novo app record

### Observacao importante

- o bloqueio da Apple deixou de ser interpretado como erro do app
- a frente iOS agora depende de alinhamento de identificadores, nao de mais debugging do binario

## 2026-04-03 - Causa real encontrada no workflow do Codemagic

### Contexto

- mesmo com app record novo, bundle id novo, Firebase iOS novo e build valida, o App Store Connect seguia retornando `PATCH ... appStoreVersions ... 409 (Conflict)` sempre que a compilacao era anexada
- a build aparecia normalmente no TestFlight e no app novo, o que confundia o diagnostico

### Causa raiz

- o workflow iOS no `Codemagic` estava exportando a build com:
  - `testFlightInternalTestingOnly: true`
- isso fazia a compilacao nascer como voltada apenas para teste interno do TestFlight
- por isso ela podia ser validada e testada internamente, mas nao funcionava corretamente como build de submissao da App Store

### Correcao aplicada

- o flag `testFlightInternalTestingOnly` foi removido do `codemagic.yaml`
- uma nova build foi gerada depois dessa mudanca
- a nova compilacao finalmente permitiu salvar a versao normalmente no App Store Connect

### Aprendizado operacional

- quando a build aparece so como apta para teste interno e gera `409` ao anexar na versao da loja, revisar imediatamente o export do Codemagic
- nao assumir que `build validada` significa `build elegivel para submissao`
- `internal-only` pode mascarar o problema por varios dias porque a Apple aceita o binario, mas rejeita a relacao com a versao da loja

### Estado depois da correcao

- frente iOS voltou a andar
- app novo na Apple aceitou a compilacao correta
- pipeline Apple/Codemagic/Firebase/bundle id ficou coerente novamente

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
