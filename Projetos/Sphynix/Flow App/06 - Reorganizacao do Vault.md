---
type: vault-organization
project: sphynix
status: proposed
canonical: true
updated: 2026-04-26
tags:
  - obsidian
  - organizacao
  - sphynix
---
# Reorganizacao do Vault

## Diagnostico

O vault esta util, mas ainda parece uma memoria linear.

Pontos bons:

- existe hub principal
- existe AI Memory
- existem notas canonicas
- ha um canvas visual inicial

Pontos fracos:

- Flow App nao tinha dashboard proprio
- estado atual estava atrasado em relacao ao codigo real
- repositorios e branchs estavam desatualizados
- roadmap, log e decisoes estavam misturados
- faltava um ritual claro de atualizacao

## Organizacao Recomendada

Sem mover arquivos antigos agora:

```text
Projetos/
  Sphynix/
    00 - Hub.md
    10 - Estado Atual.md
    11 - Proxima Acao.md
    12 - Decisoes Irrevogaveis.md
    13 - Fonte de Verdade.md
    AI Memory/
    Flow App/
      00 - Flow App Dashboard.md
      01 - Progress Map.md
      02 - Roadmap Longo Prazo.md
      03 - Log de Progresso.md
      04 - Ritual de Atualizacao.md
      05 - Decisao Monetizacao iOS.md
      06 - Reorganizacao do Vault.md
```

## Reorganizacao Futura

Quando houver tempo, migrar para:

```text
Projetos/Sphynix/
  00 - Hub.md
  Strategy/
  Product/
  Engineering/
  App Review/
  AI Memory/
  Archive/
```

## Minha Opiniao

Eu nao reorganizaria tudo agora.

Melhor caminho:

- criar camada nova e clara
- atualizar links canonicos
- usar por alguns dias
- so depois mover notas antigas para pastas definitivas

Isso evita quebrar links e deixa o vault melhorar por gravidade, nao por reforma pesada.
