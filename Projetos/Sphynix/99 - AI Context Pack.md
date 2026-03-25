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

Flow = marketplace de servicos + rede social de trabalhos

BarberFlow = primeira implementacao valida e pronta para lancamento

## Launch Priority

- lancar BarberFlow imediatamente
- focar marketing em barbeiros
- medir tracao real
- expandir categorias apenas depois de sinais claros

## Metrics That Matter

- cadastros de prestadores
- agendamentos realizados
- posts no feed
- retencao diaria

## Code Context

- repo: `https://github.com/Israel-Bryant/sphinyx-shop`
- branch: `main`
- stack: Next.js 16 + React 19 + TypeScript + Tailwind CSS 4

## Important Routes

- `/`
- `/flow`
- `/flow/barberflow`
- `/marketplace`
- `/launcher`

## Source of Truth

- AI memory index: [[AI Memory/00 - AI Memory Hub]]
- repositorios: [[AI Memory/15 - Repositorios]]
- estado operacional: [[10 - Estado Atual]]
- proxima execucao: [[11 - Proxima Acao]]
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
