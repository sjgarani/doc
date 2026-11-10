# RFCs (pedidos de comentários)

Aqui ficam as **RFCs** (*Requests for Comments*) do projeto. Uma RFC é uma proposta aberta à discussão. Ela serve para mudanças grandes de arquitetura, funcionalidades novas e complexas, alterações em APIs ou contratos públicos e iniciativas técnicas que atravessam várias partes do sistema: tudo o que ganha com uma revisão em conjunto antes de ser implementado.

---

## Ciclo de vida

O status de uma RFC muda pelo fluxo de revisão do projeto.

| Status | Significado |
| :--- | :--- |
| `draft` | Proposta em redação, por um autor ou por um agente de IA. |
| `review` | Aberta para discussão e comentários. |
| `approved` | Proposta aprovada; já pode dar origem a ADRs e Specs. |
| `rejected` | Proposta recusada. Continua no repositório como registro histórico. |
| `implemented` | Todas as Specs e tarefas que saíram da proposta foram concluídas. |

---

## Nome dos arquivos

O nome começa com um número sequencial de 4 dígitos, seguido do título em `kebab-case`:

```text
NNNN-titulo-da-proposta.md
```

**Exemplos:**
- `0001-fluxo-de-autenticacao-oauth2.md`
- `0002-pipeline-assincrono-de-eventos.md`

---

## Como criar e atualizar uma RFC

Use o `template.md` como base e o próximo ID livre. Explique a proposta, as alternativas e o que
ainda está em aberto. Envie a RFC para revisão para abrir a discussão e atualize o status quando
o grupo chegar a uma decisão. Por enquanto esse fluxo é manual; a automação pode vir depois.

---

## Revisão e orientações para agentes de IA

1. **Revisão**:
   - Toda RFC nova passa por revisão.
   - Os itens de **Pontos em aberto** devem ser resolvidos durante a revisão.
2. **Geração de ADRs, Specs e Runbooks**:
   - Quando a RFC passar para `approved`, registre em **ADRs** (`adrs/`) as decisões de arquitetura que ela estabelece, divida a implementação em **Specs** (`specs/`) e descreva os procedimentos operacionais em **Runbooks** (`runbooks/`).
3. **Instruções para agentes de IA**:
   - Ao redigir uma RFC, analise o código existente, os ADRs `accepted` e os PRDs relacionados (`related_prds`) para levantar os componentes afetados, os riscos de compatibilidade e as alternativas possíveis.
   - Quando uma RFC estiver `approved`, use a checklist de **Plano de adoção e documentos derivados** para criar os ADRs, as Specs e os Runbooks correspondentes.
