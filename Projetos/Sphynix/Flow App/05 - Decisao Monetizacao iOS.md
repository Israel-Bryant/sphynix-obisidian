---
type: decision-needed
project: flow-app
status: open
canonical: true
updated: 2026-04-26
tags:
  - flow
  - monetizacao
  - ios
  - app-review
---
# Decisao Monetizacao iOS

## Problema

A Apple apontou o cadastro de negocio/prestador como possivel acesso a mecanismo externo de compra ou assinatura usado no app.

Enquanto o modelo nao estiver claro, o iOS deve evitar:

- criar conta profissional
- prometer trial
- mencionar assinatura externa
- publicar vitrine profissional nova dentro do app
- desbloquear recurso digital pago sem IAP

## Opcoes

### Opcao A: iOS cliente-only

O iOS serve para clientes descobrirem, salvarem, abrirem mapa e conversarem.

Prestadores entram por web/admin.

Vantagem:

- mais simples para App Review
- evita IAP no curto prazo

Risco:

- prestador tem experiencia mais fragmentada

### Opcao B: iOS companion para prestador existente

Prestador ja cadastrado fora do iOS pode acessar perfil, mensagens e agenda.

Nao cria conta nova no app.

Vantagem:

- preserva uso profissional

Risco:

- precisa deixar isso muito claro para Apple

### Opcao C: IAP para prestador no iOS

Cadastro e recursos digitais de prestador passam pelo In-App Purchase.

Vantagem:

- permite fluxo completo no iOS

Risco:

- maior complexidade tecnica e margem da Apple

## Decisao Atual

Temporaria:

- esconder criacao/ativacao profissional no iOS
- manter app iOS focado em cliente/descoberta
- revisar depois que a primeira aprovacao passar

## Pendente

- escolher modelo definitivo antes de investir forte em prestador no iOS
