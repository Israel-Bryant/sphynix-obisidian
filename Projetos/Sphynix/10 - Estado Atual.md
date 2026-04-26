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

- Sphynix ja tem site institucional e estrutura de produto definida
- Flow e o app unico de descoberta, reputacao, mapa e conversa para servicos locais
- BarberFlow continua como primeira categoria forte dentro do Flow
- Flow App em Flutter esta em fase de revisao de loja
- Apple App Review apontou risco Guideline 3.1.1 por cadastro profissional/negocio
- iOS foi ajustado para esconder criacao/ativacao de prestador enquanto nao houver decisao de IAP/modelo Apple-safe
- foco atual e App Review, build confiavel, Codemagic e validacao cliente
- Divine Chaos segue preservado como IP incubada em backlog

## Current State

- `Sphynix` = holding
- `Sphynix Platform` = infraestrutura
- `Flow` = linha de produtos mobile-first
- `BarberFlow` = primeiro produto e porta de entrada

## Code State

- site em Next.js estruturado e publicado em `sphynix.com`
- rotas `/flow/barberflow`, `/flow/barberflow/privacy` e `/flow/barberflow/terms` existem
- dados de produto web centralizados em `src/lib/flow-products.ts`
- app Flutter atual em `C:\Users\israe\OneDrive\Documents\Projetos\Flow`
- app Flutter ja recebeu Apple Sign-In, exclusao de conta, restaurar compras e endurecimento da agenda
- backend do app tem protecao contra duplo agendamento e fluxo de exclusao mais seguro
- repo Flutter usado para push: `https://github.com/Israel-Bryant/barberflow-sphynix`
- commit compliance iOS: `68bfe89 Prepare iOS review compliance build`
- branch compliance enviada: `ios-review-compliance-flow`
- Codemagic existe, mas ainda precisa ter repo/branch canonico confirmado para a proxima build
- Flow web/Firebase ja tem base de onboarding, workspace, equipe, convite, agenda real e perfil publico em evolucao

## Product State

- experiencia visual premium forte
- discovery, mapa, salvos e direct formam o nucleo cliente
- linguagem desejada do Flow: `fluidez social com consequencia operacional`
- perfil publico do prestador, inbox, chat, agenda e discovery ja receberam primeira rodada forte de microinteracoes
- fluxo de prestador no iOS esta temporariamente escondido
- modelo definitivo de monetizacao iOS ainda pendente
- zero usuarios reais
- lancamento ainda depende de App Review e build correta

## Business State

- foco total inicial em barbearia
- expansao multisservicos ainda nao iniciada
- camada social confirmada como parte do produto
- Divine Chaos e Divine Chaos Beasts nao sao prioridade operacional no momento

## Current Bottlenecks

- passar App Review sem ambiguidade de pagamento externo
- confirmar Codemagic/repo/branch da build correta
- evitar screenshots/metadados antigos com cadastro de negocio/trial
- decidir modelo prestador iOS
- consolidar copy, contraste e estados vazios
- reunir material comercial final depois da build aprovada
- iniciar operacao de aquisicao inicial sem abrir categorias cedo demais

## Related Notes

- [[11 - Proxima Acao]]
- [[Flow App/00 - Flow App Dashboard]]
- [[Flow App/01 - Progress Map]]
- [[12 - Decisoes Irrevogaveis]]
- [[13 - Fonte de Verdade]]
- [[15 - Cofre de Ideias e Backlog]]
- [[99 - AI Context Pack]]
