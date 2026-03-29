# Flow

## Definicao

**Flow** e uma linha de produtos da Sphynix.

Nao e:

- a holding inteira
- o marketplace inteiro
- um dominio separado obrigatoriamente

E:

- uma frente propria
- mobile-first
- focada em automacao de servicos
- um unico app multisservicos
- uma base para marketplace + rede social

## Decisao Estrategica Atual

Flow sera **um unico app**, nao varios apps separados por nicho.

Leitura atual:

- **BarberFlow** nao morre
- BarberFlow vira a categoria de entrada mais forte
- o lancamento comeca nichado em barbearia
- a expansao vem depois da validacao

Veja tambem:

- [[05 - Decisao Estrategica do Flow]]
- [[06 - Lancamento BarberFlow - Fase 1]]
- [[07 - Rede Social e Marketplace]]

## Posicionamento

Flow existe dentro do ecossistema principal da Sphynix.

Estrutura recomendada:

- `sphynix.com/flow`
- produtos da linha em rotas dedicadas

## Foco Inicial

- iOS
- Android
- operacoes de servico
- agenda
- relacionamento com clientes
- recorrencia
- feed social com descoberta
- agendamento dentro do conteudo

## Estado de Produto Mais Recente

- existe um repositorio proprio do `Flow`, separado do `BarberFlow`
- o `Flow` esta sendo desenhado como `core + presets`, sem mexer no BarberFlow
- o onboarding do prestador agora e um wizard curto com preset, modo operacional e disponibilidade inicial
- o modelo de time foi desenhado como `workspace` com `owner`, `manager` e `collaborator`
- convite de colaborador parte de uma conta existente no Flow
- o core ja contempla agenda por horario, fila, aprovacao manual e modelo hibrido
- a agenda real do Flow ja foi ligada em colecoes proprias do Firestore
- o perfil publico do prestador ja conversa com direct, agenda e presenca publica dentro do app
- a direcao de interface esta caminhando para `fluidez social com consequencia operacional`

## Regras Atuais do Flow

- cliente entra dentro do ecossistema do Flow
- o principal caminho de descoberta e perfil publico, busca, feed e deep link
- chat considerado agora e `cliente ↔ prestador/time`
- billing e copy nao sao foco desta fase
- a prioridade atual e funcionalidade, interface e atratividade do produto

## Produtos da Linha

- [[03 - BarberFlow]]

## Ideias de Evolucao

- dashboard web complementar
- marketplace de profissionais
- camada de descoberta tipo rede social
- integracao com pagamentos
- liberacao progressiva de novas categorias
