---
type: product-dashboard
project: flow-app
status: active
canonical: true
updated: 2026-04-26
tags:
  - flow
  - produto
  - progresso
  - app-review
---
# Flow App Dashboard

## Leitura Rapida

O Flow App esta em fase de revisao de loja e consolidacao de produto.

Estado de agora:

- app Flutter existe e compila
- experiencia visual premium esta forte
- Apple App Review apontou risco em cadastro de prestador/negocio
- iOS foi ajustado para esconder criacao/ativacao profissional
- commit de compliance inicial: `68bfe89 Prepare iOS review compliance build`
- commit de QA pre-review: `5efccbf Fix QA findings before review build`
- commit de testes de regressao: `60a92be Add regression tests for QA fixes`
- branch enviada ao GitHub: `ios-review-compliance-flow`
- Codemagic ainda depende de alinhar a branch monitorada

## Mapa Visual

Abrir no Obsidian:

- [[01 - Progress Map]]
- [[02 - Roadmap Longo Prazo]]
- [[03 - Log de Progresso]]
- [[04 - Ritual de Atualizacao]]

## Grafico de Progresso

```mermaid
flowchart LR
  A[App Review iOS] --> B[Compliance 3.1.1]
  B --> C[Build Codemagic]
  C --> D[TestFlight / App Store]
  D --> E[Lancamento controlado]
  E --> F[Validacao com usuarios]
  F --> G[Monetizacao clara]

  B --> B1[Cadastro prestador escondido no iOS]
  B --> B2[Texto de trial/assinatura removido]
  B --> B3[QA bugs corrigidos + testes de regressao]
  C --> C1[Branch/remote precisam ficar canonicos]
  F --> F1[Discovery, mapa, salvos, direct]
```

## Score Atual

| Area | Status | Progresso | Proxima acao |
|---|---|---:|---|
| App Review iOS | Em revisao | 78% | Confirmar build correta no Codemagic |
| Compliance Apple | Em andamento | 85% | Revisar screenshots/metadados antes de reenviar |
| UX premium | Forte | 84% | Revisao visual em device real |
| Discovery social | Em construcao | 65% | Quebrar componentes e validar sinais reais |
| Codemagic/Git | Parcial | 55% | Definir branch monitorada no Codemagic |
| Monetizacao | Indefinida | 25% | Escolher: iOS cliente-only, web provider, ou IAP |
| Obsidian/Memory | Reorganizando | 55% | Manter este dashboard atualizado a cada sessao |

## Prioridade Agora

1. Garantir que o Codemagic gere uma build a partir de `ios-review-compliance-flow`.
2. Atualizar screenshots/metadados para nao mostrar tela antiga de barbearia/trial.
3. Reenviar build iOS sem cadastro profissional e sem linguagem de trial externo.
4. Criar decisao formal sobre prestador no iOS: esconder, companion, ou IAP.
5. Rodar revisao visual em device real/iPad antes do envio final.

## Links Canonicos

- [[../00 - Hub]]
- [[../10 - Estado Atual]]
- [[../11 - Proxima Acao]]
- [[../13 - Fonte de Verdade]]
- [[../AI Memory/00 - AI Memory Hub]]
