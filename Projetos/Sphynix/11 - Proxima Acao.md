---
type: next-actions
project: sphynix
status: active
priority: highest
canonical: true
tags:
  - ai
  - proxima-acao
  - execucao
---
# Proxima Acao

## AI Summary

Se uma IA retomar o projeto agora, ela deve priorizar estas acoes nesta ordem.

## Ordered Actions

1. amanha de manha abrir [[20 - Log de Execucao Recente]] e retomar o bloqueio do App Store Connect pela ficha da versao
2. alinhar o projeto iOS do BarberFlow ao novo bundle id `com.sphynx.barberflowapp`
3. recriar o app iOS no Firebase e substituir o `GoogleService-Info.plist`
4. atualizar Codemagic/signing para o novo bundle id e gerar uma nova compilacao
5. preencher o novo app record da Apple e anexar a build sem assinaturas
6. decidir conscientemente a estrategia do premium no iPhone nesta primeira release
7. reunir screenshots reais do app
8. publicar o app nas lojas
9. preparar onboarding focado em barbeiros
10. iniciar aquisicao com foco em barbeiros

## Faixa Paralela do Flow

Quando a frente ativa for o produto `Flow`, a proxima execucao deve seguir assim:

1. revisar a superficie `Descobrir`
2. desenhar filtros e nichos com identidade visual propria, mas coesa
3. manter a linguagem de `fluidez social com consequencia operacional`
4. refinar perfil publico, colecoes e vitrine para ficarem mais autorais
5. manter Firebase web, onboarding, workspace e agenda estaveis enquanto a camada visual evolui

## If Working On Code

Prioridade de codigo:

1. manter estavel o app Flutter para release
2. so implementar billing iOS quando houver backend real para validacao da App Store
3. melhorar pagina do produto para conversao
4. manter `src/lib/flow-products.ts` como fonte central
5. no Flow, priorizar funcionalidade + interface antes de billing e copy

## If Working On Produto

Prioridade de produto:

1. lancamento controlado
2. validacao operacional
3. tracao inicial
4. so depois expansao

## Explicit Do Not Do Now

- nao abrir novas categorias agora
- nao criar varios apps separados
- nao reposicionar Flow fora da estrategia atual
- nao tratar o social como opcional
- nao prometer premium iOS nativo antes do backend existir

## Related Notes

- [[10 - Estado Atual]]
- [[12 - Decisoes Irrevogaveis]]
- [[06 - Lancamento BarberFlow - Fase 1]]
- [[99 - AI Context Pack]]
