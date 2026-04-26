---
type: progress-log
project: flow-app
status: active
canonical: true
updated: 2026-04-26
tags:
  - flow
  - log
  - progresso
---
# Log de Progresso

## 2026-04-26

### App Review

- Apple retornou rejeicao por Guideline 3.1.1.
- Motivo interpretado: tela de cadastro de negocio com promessa de acesso/trial fora de IAP.
- Decisao temporaria: esconder criacao/ativacao de prestador no iOS.

### Codigo

- Criada politica central `FlowAppStorePolicy`.
- Cadastro provider bloqueado no iOS.
- Ativacao provider bloqueada no iOS para perfil ainda nao publicado.
- Role selection iOS passou a ser cliente-only.
- Ajustada copy sensivel removendo linguagem de assinatura/trial.
- Validacoes passaram: `flutter analyze` e `flutter test`.

### Git

- Commit local criado: `68bfe89 Prepare iOS review compliance build`.
- Branch enviada para GitHub: `ios-review-compliance-flow`.
- Ponto pendente: confirmar qual branch o Codemagic monitora.

### Obsidian

- Criada area `Flow App`.
- Criados dashboard, progress map, roadmap e ritual de atualizacao.

### QA Pre-Review

- Rodados tres agentes de QA: cliente final, barbeiro/prestador e copy PT-BR.
- Corrigidos riscos principais antes da build:
- crash de colecao vazia
- `Conta mestra` removida da entrada publica
- mapa completo passou a abrir perfil de estabelecimento
- agendamento visitante ganhou CTA `Entrar para agendar`
- workspace endurecido contra convite/permissao indevida
- perfil oculto agora sai de mapa/busca quando `publicProfileEnabled=false`
- copy de prototipo removida de perfil e pontos visiveis
- Commit enviado: `5efccbf Fix QA findings before review build`.

### Testes

- Adicionados testes de regressao para:
- colecao vazia sem studio primario
- perfil oculto fora do mapa
- convite aceito apenas pelo usuario alvo
- permissao de workspace bloqueando escalonamento
- CTA de autenticacao no agendamento para visitante
- `flutter analyze` passou.
- `flutter test` passou com 6 testes.
- Commit enviado: `60a92be Add regression tests for QA fixes`.

## Template de Atualizacao

### YYYY-MM-DD

#### Feito

- 

#### Decisoes

- 

#### Riscos

- 

#### Proxima Acao

- 
