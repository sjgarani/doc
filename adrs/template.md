---
# ============================================================================
# Managed section — preserve the document metadata when updating this file
# ============================================================================
id: ADR-0000
type: adr
title: "Short and objective title of the architectural decision"
status: proposed
created_at: YYYY-MM-DD
updated_at: YYYY-MM-DD
superseded_by: ""
# ============================================================================
deciders:
  - "@owner"
supersedes: []
related_rfcs: []
related_specs: []
tags: []
---

# ADR-0000: Título curto e objetivo da decisão

## Contexto e problema

Descreva o contexto técnico e de negócio, o problema de arquitetura a resolver e as restrições ou forças envolvidas (latência, escalabilidade, segurança, facilidade de manutenção, prazos, conhecimento da equipe).

## Critérios de decisão

- Critério 1 (ex.: consistência de dados rigorosa)
- Critério 2 (ex.: pouca carga operacional para a equipe atual)
- Critério 3 (ex.: integração simples com os pipelines de CI/CD que já existem)

## Opções consideradas

1. **Opção 1**: nome da abordagem A
2. **Opção 2**: nome da abordagem B
3. **Opção 3**: deixar como está (não fazer nada)

## Prós e contras das opções

### Opção 1: nome da abordagem A

- **Prós**:
  - Principal vantagem 1
- **Contras**:
  - Limitação ou custo 1

### Opção 2: nome da abordagem B

- **Prós**:
  - Principal vantagem 1
- **Contras**:
  - Limitação ou custo 1

## Decisão

**Opção escolhida**: "[nome da opção]", porque [justificativa clara, apoiada nos critérios de decisão].

## Consequências

### Positivas
- Ganhos esperados em arquitetura, produtividade da equipe ou confiabilidade.

### Negativas e concessões
- Dívida técnica assumida, complexidade a mais ou esforço de migração.

## Verificação de conformidade (IA e revisão de código)

> Esta seção explica a assistentes de código com IA e a revisores humanos como verificar se o código do repositório respeita esta decisão.

- **Padrões obrigatórios**: [ex.: todo acesso ao banco de dados fica encapsulado em `src/repositories/`].
- **Padrões proibidos**: [ex.: entidades de domínio não chamam clientes HTTP externos diretamente].
- **Verificação automática**: [ex.: testes de arquitetura, regras de linter ou outras checagens automáticas].
