---
type: roadmap
project: flow-app
status: active
canonical: true
updated: 2026-04-26
tags:
  - flow
  - roadmap
  - longo-prazo
---
# Roadmap Longo Prazo

## Norte do Produto

Flow deve virar um app de descoberta, reputacao e conversa para servicos locais.

O visual premium e uma vantagem, mas o produto ganha valor quando:

- o cliente encontra um profissional bom rapido
- o profissional publicado recebe atencao e conversa real
- o mapa, feed, perfil e direct parecem uma unica experiencia
- a loja entende o modelo de negocio sem ambiguidade

## Fase 1: App Review e Build Confiavel

Objetivo: passar pela revisao e parar de depender de sorte operacional.

- alinhar repo e branch canonicos para Codemagic
- garantir versionamento automatico
- esconder criacao provider no iOS enquanto nao houver IAP
- revisar screenshots e metadados
- criar checklist pre-review
- testar rotas iOS sensiveis

## Fase 2: Consistencia de Produto

Objetivo: transformar a experiencia premium em sistema.

- padronizar copy: cliente, perfil, mapa, salvos, direct
- corrigir contraste de textos em fundos claros/escuros
- criar estados vazios bonitos e uteis
- deixar botoes e CTAs previsiveis
- revisar iPad, iPhone pequeno e desktop
- criar guia interno de linguagem visual

## Fase 3: Base Tecnica

Objetivo: reduzir risco para continuar evoluindo rapido.

- quebrar `discovery_hub_page.dart` em modulos menores
- criar testes de navegacao e feature flags por plataforma
- criar camada de analytics/eventos
- limpar dados mockados versus dados reais
- revisar Firebase rules e modelos de colecao
- documentar fluxo de deploy

## Fase 4: Discovery Inteligente

Objetivo: fazer o app parecer vivo e pessoal.

- melhorar ranking por busca, filtro, salvos e abertura de perfil
- persistir sinais de gosto com privacidade
- conectar feed, mapa e perfil com a mesma logica
- criar recomendacoes explicaveis sem parecer texto tecnico
- medir conversao: busca -> perfil -> direct -> retorno

## Fase 5: Monetizacao Apple-Safe

Objetivo: escolher um modelo que nao brigue com a App Store.

Opcoes:

- iOS cliente-only e prestador via web/admin
- iOS como companion para prestador ja cadastrado
- IAP para recursos digitais de prestador dentro do iOS
- anuncios/destaques com regras transparentes

Decisao pendente:

- [[05 - Decisao Monetizacao iOS]]

## Fase 6: Crescimento

Objetivo: validar com gente real.

- definir cidade/nicho inicial
- criar painel de prestadores publicados
- preparar abordagem comercial
- criar funil de onboarding fora do app se necessario
- medir retencao de cliente
- medir conversas iniciadas por prestador

## Backlog Vivo

| Item | Prioridade | Estado |
|---|---|---|
| Codemagic branch canonica | Alta | Pendente |
| Review-safe screenshots | Alta | Pendente |
| Testes rota provider iOS | Alta | Pendente |
| Copy e contraste global | Alta | Em andamento |
| Quebra do discovery hub | Media | Pendente |
| Analytics de discovery | Media | Pendente |
| Dashboard admin prestador | Media | Pendente |
| Monetizacao definitiva | Alta | Pendente |
