---
# ============================================================================
# Managed section — preserve the document metadata when updating this file
# ============================================================================
id: RUNBOOK-0000
type: runbook
title: "Action-oriented title of the operational procedure"
status: draft
created_at: YYYY-MM-DD
updated_at: YYYY-MM-DD
last_verified_at: ""
# ============================================================================
owners:
  - "@owner"
related_specs: []
related_adrs: []
tags: []
---

# RUNBOOK-0000: Título do procedimento, começando pela ação

## Objetivo e quando usar

- **Objetivo**: Diga que resultado este procedimento entrega.
- **Quando usar**: Liste o que leva a executá-lo, como nomes de alertas, sintomas observados, manutenções programadas ou solicitações.

## Pré-requisitos

- **Acessos e permissões**: Sistemas, perfis ou ambientes de que o operador precisa.
- **Ferramentas**: CLIs, scripts ou consoles necessários, com a versão mínima quando ela fizer diferença.
- **Aprovações**: Solicitações de mudança ou aprovações que precisam sair antes de começar.
- **Credenciais**: Onde obtê-las, como o caminho no cofre de segredos ou o responsável pela credencial. Nunca escreva segredos neste documento.

## Riscos e impacto

- **Impacto no serviço**: Indisponibilidade prevista, queda de desempenho ou efeitos que os usuários vão perceber.
- **Risco para os dados**: Que dados podem ser alterados, apagados ou expostos.
- **Passos irreversíveis**: Os passos que não têm volta, por exemplo o passo N.
- **Janela de manutenção**: Quando o procedimento pode e quando não pode ser executado.

## Procedimento

Execute os passos na ordem. Se o resultado de um passo não for o **Resultado esperado**, pare e siga **Se falhar**. Em ações manuais, deixe de fora o **Comando**.

### Passo 1: Descrição curta da ação

- **Comando**:
  ```bash
  comando --com-argumentos
  ```
- **Resultado esperado**: O que o operador deve ver quando o passo dá certo.
- **Se falhar**: Vá para [Rollback](#rollback) ou [Escalonamento](#escalonamento).

### Passo 2: Descrição curta da ação

- **Comando**:
  ```bash
  comando --com-argumentos
  ```
- **Resultado esperado**: O que o operador deve ver quando o passo dá certo.
- **Se falhar**: Vá para [Rollback](#rollback) ou [Escalonamento](#escalonamento).

## Verificação

- Liste as checagens que confirmam que o procedimento deu certo (comandos, dashboards ou endpoints de saúde) e o resultado esperado de cada uma.

## Rollback

Desfaça, na ordem inversa, cada passo que alterou o estado do sistema:

1. Desfazer o passo 2: comando ou ação.
2. Desfazer o passo 1: comando ou ação.

## Escalonamento

- **Contatos**: A equipe, o plantão ou o responsável a acionar.
- **Quando escalonar**: As situações em que é preciso parar e escalonar, como um rollback que falhou ou um impacto maior do que o previsto em **Riscos e impacto**.

## Regras de execução para agentes de IA

> Esta seção diz aos agentes de IA quais passos eles podem executar sozinhos e quando devem parar.

- **Executar sem confirmação**: [ex.: passo 1, uma consulta de status que só faz leitura].
- **Exige confirmação humana**: [ex.: passo 2, que reinicia o serviço]. Todo passo que altera estado, não tem volta ou produz efeito fora do sistema entra aqui.
- **Quando parar**: [ex.: qualquer resultado inesperado, um pré-requisito faltando ou um impacto maior do que o previsto em **Riscos e impacto**].
