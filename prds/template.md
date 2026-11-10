---
# ============================================================================
# Managed section — preserve the document metadata when updating this file
# ============================================================================
id: PRD-0000
type: prd
title: "Descriptive title of the product initiative"
status: draft
created_at: YYYY-MM-DD
updated_at: YYYY-MM-DD
# ============================================================================
owners:
  - "@owner"
stakeholders: []
tags: []
---

# PRD-0000: Título descritivo da iniciativa de produto

## Visão geral

Em um ou dois parágrafos, resuma o que vai ser construído, por que isso importa e qual o resultado esperado.

## Problema

- Que problema do usuário ou do negócio existe hoje e qual o impacto de não resolvê-lo?
- Quem são os usuários ou personas afetados?
- Que dados, pesquisas ou métricas comprovam essa necessidade?

## Objetivos e métricas de sucesso

- **Métricas principais**:
  - `[Métrica 1]`: Valor atual -> Meta (como e quando vai ser medida)
  - `[Métrica 2]`: Valor atual -> Meta
- **Métricas de controle (guardrails)**: Métricas que não podem piorar por causa desta iniciativa (ex.: taxa de erros, latência, retenção).

## Cenários de uso

1. **Cenário 1 — [Fluxo principal]**: Jornada completa do usuário, do gatilho ao resultado esperado.
2. **Cenário 2 — [Fluxo alternativo ou de erro]**: Como o produto se comporta quando uma pré-condição falha ou um limite é atingido.

## Escopo

### Dentro do escopo
- **REQ-01**: Funcionalidade ou requisito principal voltado ao usuário 1
- **REQ-02**: Funcionalidade ou requisito principal voltado ao usuário 2

### Fora de escopo
- Funcionalidades ou fluxos que ficam explicitamente **de fora** desta iniciativa

## Restrições e riscos

- **Privacidade, conformidade e segurança**: Sensibilidade dos dados, obrigações regulatórias ou regras de acesso.
- **Dependências e premissas**: Equipes das quais este trabalho depende, serviços de terceiros ou pré-requisitos operacionais.
- **Riscos**: Riscos para a adoção ou a entrega e como serão mitigados.

## Pontos em aberto

- [ ] Ponto em aberto 1, a resolver durante a revisão
- [ ] Ponto em aberto 2

## Plano de adoção e documentos derivados

Quando este PRD for aprovado (`status: approved`), crie os documentos abaixo:

- **RFCs a criar**:
  - [ ] `RFC-NNNN`: [título da proposta técnica, quando for preciso discutir a arquitetura]
- **Specs a criar**:
  - [ ] `SPEC-NNNN`: [título da especificação que vai guiar a implementação]
