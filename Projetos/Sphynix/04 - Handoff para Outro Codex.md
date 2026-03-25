# Handoff para Outro Codex

## Repo

- `https://github.com/Israel-Bryant/sphinyx-shop`
- branch: `main`

## Contexto

- Sphynix = holding
- Sphynix Platform = infraestrutura
- Flow = linha especifica de produtos
- Flow = mobile-first
- BarberFlow = primeiro produto real da linha

## Stack

- Next.js 16
- React 19
- TypeScript
- Tailwind CSS 4

## Rotas Importantes

- `/`
- `/flow`
- `/flow/barberflow`
- `/marketplace`
- `/launcher`

## Arquivos Principais

- `src/app/page.tsx`
- `src/app/flow/page.tsx`
- `src/app/flow/[slug]/page.tsx`
- `src/app/marketplace/page.tsx`
- `src/lib/flow-products.ts`
- `src/lib/store-links.ts`

## O Que Ja Esta Feito

- estrutura institucional da Sphynix como holding
- Flow posicionado como linha mobile-first
- pagina dinamica de produto em `/flow/[slug]`
- primeiro produto cadastrado: BarberFlow
- dados centralizados em `src/lib/flow-products.ts`

## Objetivo Agora

- continuar a pagina do BarberFlow
- preparar entrada de descricao real
- preparar screenshots reais
- preparar links reais da App Store e Google Play

## Onde Editar Conteudo

- `src/lib/flow-products.ts`

## Onde Colocar Imagens

- `public/products/barberflow/`

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
