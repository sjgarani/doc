# Specs (especificações técnicas e funcionais)

Aqui ficam as **Specs** do projeto. Uma Spec é o roteiro que desenvolvedores e **agentes de IA** seguem para implementar uma funcionalidade, um módulo ou uma refatoração, e fica ligada ao trabalho de implementação e às revisões correspondentes.

---

## Ciclo de vida

O status de uma Spec muda pelo fluxo de revisão do projeto.

| Status | Significado |
| :--- | :--- |
| `draft` | Em redação; os requisitos ou o design ainda estão incompletos. |
| `ready` | Revisada e pronta para ser implementada por um desenvolvedor ou agente de IA. |
| `in-progress` | Implementação em andamento. |
| `done` | Todos os critérios de aceitação e tarefas foram implementados, testados e integrados. |
| `archived` | Mantida só como histórico, ou substituída por uma Spec mais nova. |

---

## Nome dos arquivos

O nome começa com um número sequencial de 4 dígitos, seguido do título em `kebab-case`:

```text
NNNN-nome-da-funcionalidade-ou-modulo.md
```

**Exemplos:**
- `0001-endpoint-de-cadastro-de-usuario.md`
- `0002-worker-de-reenvio-de-webhooks.md`

---

## Como criar e atualizar uma Spec

Use o `template.md` como base e o próximo ID livre. Preencha a especificação, ligue-a aos itens
de trabalho e às revisões relacionadas e mantenha o status em dia durante toda a implementação.
Por enquanto esse fluxo é manual; a automação pode vir depois.

---

## Rastreabilidade e orientações para agentes de IA

1. **Fonte de verdade para agentes de IA**:
   - A seção **Contexto para agentes de IA** indica os diretórios e arquivos afetados, os ADRs que precisam ser respeitados e os comandos de teste e verificação.
   - A **Divisão de tarefas** é uma checklist (`- [ ]`), para que desenvolvedores e agentes de IA acompanhem a implementação passo a passo.
2. **Rastreabilidade**:
   - Toda Spec `ready` ou `in-progress` deve estar ligada aos documentos de que deriva (`related_prds`, `related_rfcs`, `related_adrs`) e às revisões relacionadas.
