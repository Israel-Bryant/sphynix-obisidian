---
type: ai-context
project: sphynix
status: active
canonical: true
tags:
  - ai
  - context
  - handoff
---
# AI Context Pack

## Purpose

Esta nota existe para leitura rapida por IA.

Use esta nota quando for necessario:

- entender o projeto rapidamente
- retomar trabalho em outro computador
- passar contexto para outro agente

## Canonical Identity

- empresa: `Sphynix`
- papel da empresa: holding
- plataforma: `Sphynix Platform`
- linha de produto ativa: `Flow`
- produto inicial prioritario: `BarberFlow`

## Core Decisions

- Flow sera um unico app
- BarberFlow continua vivo como entrada e categoria forte
- o lancamento inicial fica nichado em barbearia
- a expansao para multisservicos vem depois da validacao
- a camada social faz parte do produto desde o dia 1

## Current Product Model

Flow = app de descoberta, reputacao, mapa e conversa para servicos locais

BarberFlow = primeira categoria forte dentro do Flow, nao app separado

Flow repo paralelo = construcao do core multisservicos com onboarding, workspace, agenda e discovery proprios

## Launch Priority

- passar App Review iOS
- garantir build confiavel no Codemagic
- manter iOS sem criacao de prestador enquanto o modelo Apple-safe nao estiver decidido
- validar experiencia cliente primeiro
- lancar de forma controlada com foco em barbeiros
- medir tracao real
- expandir categorias apenas depois de sinais claros

## Metrics That Matter

- cadastros de prestadores
- agendamentos realizados
- posts no feed
- retencao diaria

## Code Context

- site repo: `https://github.com/Israel-Bryant/sphinyx-shop`
- app repo: `https://github.com/Israel-Bryant/barberflow-sphynix`
- vault repo: `https://github.com/Israel-Bryant/sphynix-obisidian`
- app Flutter local: `C:\Users\israe\OneDrive\Documents\Projetos\Flow`
- branch compliance iOS: `ios-review-compliance-flow`
- commit compliance iOS: `68bfe89 Prepare iOS review compliance build`
- site stack: Next.js 16 + React 19 + TypeScript + Tailwind CSS 4
- app stack: Flutter + Firebase Functions

## App Context

- build iOS atual: via `Codemagic`
- signing Apple: ja configurado em nivel operacional
- App Store Review apontou Guideline 3.1.1 por cadastro profissional/negocio
- iOS foi ajustado para esconder criacao/ativacao de prestador temporariamente
- foco tecnico imediato: confirmar branch/repo do Codemagic e gerar build correta

## Important Routes

- `/`
- `/flow`
- `/flow/barberflow`
- `/flow/barberflow/privacy`
- `/flow/barberflow/terms`
- `/marketplace`
- `/launcher`

## Operational Reality

- `sphynix.com` esta no ar e servindo a experiencia web do BarberFlow
- as paginas legais do BarberFlow ja existem no dominio oficial
- o app Flutter ja recebeu Apple Sign-In, exclusao de conta e endurecimento de agenda
- a compra nativa no iPhone segue bloqueada por design ate existir backend/modelo real de validacao
- a ficha antiga do App Store Connect foi descartada e o iOS segue em app record novo
- o foco operacional atual e lancar sem regressao, nao abrir nova frente de produto
- em paralelo, o `Flow` esta sendo estruturado como produto social + operacional
- o `Flow` ja tem base de onboarding de prestador, workspace/time, convite, agenda real e perfil publico
- a linguagem desejada do `Flow` e `fluidez social com consequencia operacional`

## Source of Truth

- Flow App dashboard: [[Flow App/00 - Flow App Dashboard]]
- progress map: [[Flow App/01 - Progress Map]]
- roadmap: [[Flow App/02 - Roadmap Longo Prazo]]
- AI memory index: [[AI Memory/00 - AI Memory Hub]]
- repositorios: [[AI Memory/15 - Repositorios]]
- estado operacional: [[10 - Estado Atual]]
- proxima execucao: [[11 - Proxima Acao]]
- publicacao iOS: [[08 - Publicacao iOS sem Mac]]
- decisoes fixas: [[12 - Decisoes Irrevogaveis]]
- fontes oficiais: [[13 - Fonte de Verdade]]
- glossario: [[14 - Glossario]]
- estrategia: [[05 - Decisao Estrategica do Flow]]
- lancamento: [[06 - Lancamento BarberFlow - Fase 1]]
- visao de produto: [[07 - Rede Social e Marketplace]]
- handoff tecnico: [[04 - Handoff para Outro Codex]]

## AI Rules

- nao propor varios apps separados por nicho nesta fase
- nao tratar BarberFlow como produto descartado
- nao remover a camada social do conceito do produto
- nao expandir cedo demais sem validacao do nicho
- nao assumir que premium iOS nativo ja esta pronto
- nao reabrir cadastro profissional no iOS sem resolver IAP/modelo Apple-safe
