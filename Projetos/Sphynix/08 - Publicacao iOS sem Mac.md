---
type: ios-release-playbook
project: sphynix
status: active
canonical: false
tags:
  - ios
  - app-store
  - codemagic
  - release
---
# Publicacao iOS sem Mac

## Purpose

Registrar o caminho pratico para subir o BarberFlow na Apple sem possuir um Mac fisico.

## Reality Check

- sem `macOS` + `Xcode`, nao da para gerar archive iOS localmente
- o caminho mais direto para este caso e usar CI/CD com maquina Mac
- a opcao recomendada para o BarberFlow e `Codemagic`

## Tomorrow Morning Reminder

Ao abrir o trabalho amanha de manha:

1. entrar em `codemagic.io`
2. conectar o GitHub
3. selecionar o repositorio `barberflow-sphynix`
4. configurar build iOS
5. conectar Apple Developer / App Store Connect
6. gerar a primeira build `.ipa`
7. enviar a build para o App Store Connect

## Recommended Path

### 1. Criar ou acessar conta no Codemagic

- entrar em `https://codemagic.io/`
- autenticar com GitHub
- autorizar acesso ao repositorio `barberflow-sphynix`

### 2. Criar workflow iOS para Flutter

- selecionar o repositorio do app
- escolher workflow Flutter
- habilitar plataforma `iOS`

### 3. Conectar Apple Developer

Ter em maos:

- conta Apple Developer ativa
- app criado no App Store Connect
- bundle id `com.sphynx.barberflow`

Preferencia:

- conectar a conta Apple no proprio Codemagic
- ou usar chave da App Store Connect se o fluxo pedir

### 4. Configurar signing

Conferir:

- bundle id igual a `com.sphynx.barberflow`
- capability de `Sign in with Apple`
- certificados e provisioning resolvidos pelo Codemagic ou pela conta Apple conectada

### 5. Rodar build iOS

Objetivo:

- gerar um `.ipa`
- se possivel, mandar direto para o App Store Connect

### 6. Voltar para o App Store Connect

Depois do build:

- esperar a compilacao processar
- selecionar a build na secao `Compilacao`
- revisar metadados finais
- enviar para revisao

## Expected Risks

- signing Apple mal configurado
- bundle id divergente
- capability faltando
- build number repetido
- conta Apple sem permissao suficiente

## Success Criteria

- build iOS gerada em CI
- build aparecendo no App Store Connect
- app pronto para enviar para revisao

## Related Notes

- [[11 - Proxima Acao]]
- [[06 - Lancamento BarberFlow - Fase 1]]
- [[04 - Handoff para Outro Codex]]
- [[99 - AI Context Pack]]
