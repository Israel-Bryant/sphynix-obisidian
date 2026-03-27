---
type: operating-state
project: sphynix
status: active
canonical: true
tags:
  - ai
  - estado-atual
  - operacao
---
# Estado Atual

## AI Summary

- site institucional da Sphynix ja existe
- Flow ja esta posicionado como linha de produtos
- BarberFlow ja esta estruturado como primeiro produto
- app BarberFlow em Flutter esta pronto para submissao
- ainda nao ha usuarios
- foco atual e lancamento e validacao

## Current State

- `Sphynix` = holding
- `Sphynix Platform` = infraestrutura
- `Flow` = linha de produtos mobile-first
- `BarberFlow` = primeiro produto e porta de entrada

## Code State

- site em Next.js estruturado e publicado em `sphynix.com`
- rota `/flow/barberflow` existente
- paginas legais publicadas em `/flow/barberflow/privacy` e `/flow/barberflow/terms`
- dados de produto centralizados em `src/lib/flow-products.ts`
- app Flutter com Apple Sign-In no iPhone, exclusao de conta, restaurar compras e endurecimento da agenda em equipe
- backend do app com protecao contra duplo agendamento e fluxo de exclusao mais seguro

## Product State

- app BarberFlow pronto para release controlado
- links legais funcionando no dominio oficial
- fluxo de equipe e agenda endurecido
- exclusao de conta e exclusao de barbearia com backend reforcado
- compra nativa no iPhone segue bloqueada por design ate existir backend real da App Store
- zero usuarios
- lancamento iminente
- estrategia de nicho definida

## Business State

- foco total inicial em barbearia
- expansao multisservicos ainda nao iniciada
- camada social confirmada como parte do produto

## Current Bottlenecks

- cadastro final do app na Apple
- App Store Connect com forte indicio de ficha de versao quebrada na submissao iOS
- archive e validacao final no Xcode / iPhone real
- estrategia explicita para premium no iPhone enquanto a App Store Server API nao existe
- screenshots reais finais
- operacao de aquisicao inicial

## Related Notes

- [[11 - Proxima Acao]]
- [[12 - Decisoes Irrevogaveis]]
- [[13 - Fonte de Verdade]]
- [[99 - AI Context Pack]]
