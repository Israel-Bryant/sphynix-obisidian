---
type: handoff
project: sphynix-shop
status: reusable
tags:
  - codex
  - handoff
---
# Handoff para Outro Codex

## AI Quick Context

- `Sphynix` = holding
- `Sphynix Platform` = infraestrutura
- `Flow` = linha especifica de produtos
- `Flow` = mobile-first
- `BarberFlow` = primeiro produto real da linha

## Repos

- site: `https://github.com/Israel-Bryant/sphinyx-shop`
- app: `https://github.com/Israel-Bryant/barberflow-sphynix`
- vault: `https://github.com/Israel-Bryant/sphynix-obisidian`
- branch principal: `main`

## Tech Stack

- site: Next.js 16 + React 19 + TypeScript + Tailwind CSS 4
- app: Flutter + Firebase + Firebase Functions

## Important Routes

- `/`
- `/flow`
- `/flow/barberflow`
- `/flow/barberflow/privacy`
- `/flow/barberflow/terms`
- `/marketplace`
- `/launcher`

## Important Site Files

- `src/app/page.tsx`
- `src/app/flow/page.tsx`
- `src/app/flow/[slug]/page.tsx`
- `src/app/marketplace/page.tsx`
- `src/lib/flow-products.ts`
- `src/lib/store-links.ts`

## Important App Areas

- auth
- subscription / billing
- schedule / team mode
- functions backend

## What Is Already Done

- estrutura institucional da Sphynix como holding
- Flow posicionado como linha mobile-first
- pagina dinamica de produto em `/flow/[slug]`
- primeiro produto cadastrado: BarberFlow
- dados centralizados em `src/lib/flow-products.ts`
- paginas legais do BarberFlow publicadas no dominio oficial
- app Flutter endurecido para release
- Apple Sign-In implementado no iPhone
- exclusao de conta e exclusao de barbearia reforcadas
- agenda em equipe e criacao de agendamento endurecidas
- build iOS `1.0.1 (11)` validada pela Apple
- ficha antiga do App Store Connect foi descartada por corrupcao/`409`
- novo app record iOS criado com o bundle id `com.sphynx.barberflowapp`

## Current Objective

- fechar submissao nas lojas com seguranca
- cadastrar o app na Apple
- alinhar bundle id/Firebase/Codemagic ao novo app record iOS
- preparar screenshots reais finais
- manter a web institucional coerente com o app

## Content Source of Truth

- editar conteudo em `src/lib/flow-products.ts`
- colocar imagens em `public/products/barberflow/`

## Guardrails

- nao mudar o posicionamento institucional da marca
- manter Flow como linha separada dentro da Sphynix
- manter BarberFlow como produto da linha Flow
- revisar rotas e estrutura antes de editar
- nao assumir que premium nativo no iPhone esta pronto
- nao voltar a depurar a ficha antiga da Apple; seguir no app record novo

## Related Notes

- [[05 - Decisao Estrategica do Flow]]
- [[06 - Lancamento BarberFlow - Fase 1]]
- [[07 - Rede Social e Marketplace]]
- [[99 - AI Context Pack]]

## Prompt Pronto

```txt
Abra o projeto:
https://github.com/Israel-Bryant/sphinyx-shop

Branch:
main

Contexto do projeto:
- Sphynix = holding
- Sphynix Platform = infraestrutura
- Flow = linha especifica de produtos
- Flow = mobile-first
- BarberFlow = primeiro produto real da linha Flow

Stack:
- Next.js 16
- React 19
- TypeScript
- Tailwind CSS 4

Rotas importantes:
- /
- /flow
- /flow/barberflow
- /marketplace
- /launcher

Arquivos principais:
- src/app/page.tsx
- src/app/flow/page.tsx
- src/app/flow/[slug]/page.tsx
- src/app/marketplace/page.tsx
- src/lib/flow-products.ts
- src/lib/store-links.ts

O que ja esta feito:
- Estrutura institucional da Sphynix como holding
- Flow posicionado como linha de produtos mobile-first
- Pagina dinamica de produto em /flow/[slug]
- Primeiro produto cadastrado: BarberFlow
- Dados centralizados em src/lib/flow-products.ts
- Marketplace apontando para /flow/barberflow
- Homepage destacando BarberFlow como primeiro produto da linha

Objetivo agora:
- Continuar a pagina do BarberFlow
- Preparar a entrada de descricao real, beneficios, modulos e screenshots
- Manter src/lib/flow-products.ts como fonte central dos dados
- Preparar para receber links reais da App Store e Google Play depois

Onde o conteudo deve ser editado:
- src/lib/flow-products.ts

Onde as imagens reais devem entrar:
- public/products/barberflow/

Importante:
- Nao mudar o posicionamento institucional da marca
- Manter Flow como linha separada dentro da Sphynix
- Manter BarberFlow como produto da linha Flow
- Antes de editar, revisar as rotas e a estrutura atual para nao quebrar o que ja existe
```
