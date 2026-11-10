# PRDs (documentos de requisitos de produto)

Aqui ficam os **PRDs** (*Product Requirements Documents*) do projeto. Um PRD define o que vai ser construído e por quê, do ponto de vista do usuário e do negócio: registra o problema, os objetivos, as métricas de sucesso, os cenários de uso e os limites do escopo antes do design técnico e da implementação.

---

## Ciclo de vida

O status de um PRD muda pelo fluxo de revisão do projeto.

| Status | Significado |
| :--- | :--- |
| `draft` | Requisitos de produto em redação, por um autor ou por um agente de IA. |
| `review` | Aberto para revisão de produto, design e engenharia. |
| `approved` | Escopo e métricas de sucesso aprovados; já pode dar origem a RFCs e Specs. |
| `delivered` | Todas as RFCs e Specs que saíram do PRD foram implementadas e entregues. |
| `archived` | PRD recusado, substituído ou mantido apenas como histórico. |

---

## Nome dos arquivos

O nome começa com um número sequencial de 4 dígitos, seguido do título em `kebab-case`:

```text
NNNN-titulo-da-iniciativa-de-produto.md
```

**Exemplos:**
- `0001-onboarding-self-service-com-sso.md`
- `0002-alertas-de-cobranca-por-uso.md`

---

## Como criar e atualizar um PRD

Use o `template.md` como base e o próximo ID livre. Defina o problema, as métricas de sucesso, os requisitos dentro do escopo e o que fica explicitamente de fora. Envie o PRD para revisão e atualize o status à medida que a validação do produto e a entrega avançam. Por enquanto esse fluxo é manual; a automação pode vir depois.

---

## Revisão e orientações para agentes de IA

1. **Revisão**:
   - Todo PRD novo passa por revisão.
   - Os itens de **Pontos em aberto** devem ser resolvidos durante a revisão.
2. **Geração de RFCs e Specs**:
   - Quando o PRD passar para `approved`, use a seção **Plano de adoção e documentos derivados** para criar as **RFCs** (`rfcs/`) e as **Specs** (`specs/`) correspondentes.
3. **Instruções para agentes de IA**:
   - Ao redigir ou revisar um PRD, ajude a deixar claros o problema do usuário, as metas mensuráveis em **Objetivos e métricas de sucesso**, os principais **Cenários de uso** e o que fica explicitamente em **Fora de escopo**.
   - Ao redigir uma RFC ou uma Spec a partir de um PRD `approved`, inclua-o em `related_prds` e respeite o escopo e os requisitos que ele define.
