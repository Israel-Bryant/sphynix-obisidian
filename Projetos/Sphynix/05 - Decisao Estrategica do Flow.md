---
type: decision
project: flow
status: active
date: 2026-03-25
canonical: true
tags:
  - flow
  - barberflow
  - decisao-estrategica
---
# Decisao Estrategica do Flow

## AI Summary

- decisao ativa: lancar um unico app chamado `Flow`
- `BarberFlow` nao e descartado
- `BarberFlow` vira a categoria inicial e a porta de entrada
- estrategia: validar primeiro em barbearia, expandir depois

## Decision

Vamos lancar **um unico app** chamado **Flow**.

BarberFlow continua existindo como:

- porta de entrada
- categoria inicial mais forte
- fase nichada de validacao

## Why This Decision Exists

- um app so aumenta o efeito de rede
- reduz custo de manutencao
- evita fragmentacao por nicho
- acelera o lancamento porque BarberFlow ja esta pronto
- facilita abrir novas categorias depois da validacao

## Non-Negotiables

- nao criar varios apps separados por nicho nesta fase
- nao matar a marca BarberFlow no inicio
- nao expandir categorias antes de validar barbearia
- manter a camada social como parte do produto

## Current Strategy

1. lancar no nicho de barbearia
2. validar com usuarios reais
3. manter feed social desde o dia 1
4. expandir depois para multisservicos

## Rebranding Rule

- `BarberFlow` pode evoluir para `BarberFlow by Flow`
- a migracao deve ser suave
- usuarios iniciais nao devem perceber perda, apenas ganho

## Related Notes

- [[02 - Flow]]
- [[03 - BarberFlow]]
- [[06 - Lancamento BarberFlow - Fase 1]]
- [[07 - Rede Social e Marketplace]]
- [[99 - AI Context Pack]]
