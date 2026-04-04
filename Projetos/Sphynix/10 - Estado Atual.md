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
- Divine Chaos esta preservado como IP incubada em backlog

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
- repo Flutter `barberflow-sphynix` com pipeline inicial de `Codemagic` configurado
- assinatura iOS ja estruturada no Codemagic
- build iOS gerada com sucesso e aparecendo no App Store Connect
- pipeline iOS no Codemagic estabilizado o suficiente para gerar novas compilacoes validas
- repo proprio do `Flow` em Flutter em evolucao paralela ao BarberFlow
- Flow com `Flow Core` em construcao: presets, onboarding de prestador, workspace/time, convite de colaborador, permissao refinavel e agenda real por colecoes proprias no Firestore
- Flow web agora com Firebase configurado de verdade, inclusive app web cadastrado no projeto `flow-sphynix`

## Product State

- app BarberFlow pronto para release controlado
- links legais funcionando no dominio oficial
- fluxo de equipe e agenda endurecido
- exclusao de conta e exclusao de barbearia com backend reforcado
- compra nativa no iPhone segue bloqueada por design ate existir backend real da App Store
- build iOS `1.0.1 (11)` validada pela Apple, com `Criptografia nao isenta: Nao`
- ficha antiga do App Store Connect foi removida depois de varios conflitos `409`
- um novo app record/App ID iOS foi recriado para destravar a submissao
- causa raiz do bloqueio iOS foi identificada no workflow do Codemagic: a build estava sendo exportada como `internal testing only`
- depois da remocao desse flag, a nova compilacao passou a salvar corretamente na versao da App Store
- zero usuarios
- lancamento iminente
- estrategia de nicho definida
- `Divine Chaos` e `Divine Chaos Beasts` nao sao prioridade operacional no momento
- Flow segue em fase de construcao de produto, sem depender de alteracoes no BarberFlow
- direcao visual do Flow migrando para uma linguagem mais social, viva e menos encaixotada
- perfil publico do prestador, inbox, chat, agenda e discovery ja receberam uma primeira rodada forte de microinteracoes

## Business State

- foco total inicial em barbearia
- expansao multisservicos ainda nao iniciada
- camada social confirmada como parte do produto

## Current Bottlenecks

- cadastro final do app na Apple
- acompanhar a review da Apple no app record novo
- estrategia explicita para premium no iPhone enquanto a App Store Server API nao existe
- screenshots reais finais
- publicacao nas lojas
- material comercial final
- links reais App Store / Google Play
- operacao de aquisicao inicial
- consolidar a experiencia do Flow sem perder simplicidade
- revisar `Descobrir`, filtros e nichos com identidade propria, sem virar carnaval visual

## Related Notes

- [[11 - Proxima Acao]]
- [[12 - Decisoes Irrevogaveis]]
- [[13 - Fonte de Verdade]]
- [[15 - Cofre de Ideias e Backlog]]
- [[99 - AI Context Pack]]
