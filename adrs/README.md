# ADRs (registros de decisão de arquitetura)

Aqui ficam os **ADRs** (*Architecture Decision Records*) do projeto. Cada ADR registra uma decisão de arquitetura relevante: o contexto e o problema que levaram a ela, as opções avaliadas e as consequências da escolha.

---

## Ciclo de vida

O status de um ADR muda pelo fluxo de revisão do projeto.

| Status | Significado |
| :--- | :--- |
| `proposed` | Decisão em revisão. |
| `accepted` | Decisão aprovada e em vigor. Desenvolvedores e agentes de IA devem seguir as regras dela. |
| `deprecated` | A decisão não vale mais porque o sistema ou a funcionalidade a que se refere foi desativado. |
| `superseded` | A decisão foi substituída por um ADR mais novo (exige `--superseded-by ADR-NNNN`). |

---

## Nome dos arquivos

O nome começa com um número sequencial de 4 dígitos, seguido do título em `kebab-case`:

```text
NNNN-titulo-curto-da-decisao.md
```

**Exemplos:**
- `0001-adotar-a-arquitetura-de-documentacao-doc2gh.md`
- `0002-usar-postgresql-como-banco-principal.md`

---

## Como criar e atualizar um ADR

Use o `template.md` como base e o próximo ID livre. Explique a decisão, as alternativas
consideradas e as consequências. Envie o ADR para revisão e atualize o status quando a decisão
for fechada. Por enquanto esse fluxo é manual; a automação pode vir depois.

---

## Orientações para agentes de IA

1. **Instruções para agentes de IA**:
   - Antes de propor ou revisar mudanças de arquitetura, leia todos os ADRs com status `accepted`.
   - Ao gerar ou revisar código, faça cumprir todas as regras da seção **Verificação de conformidade (IA e revisão de código)**.
   - Nunca altere a decisão central de um ADR `accepted`. Para mudá-la, crie um novo ADR e marque o anterior como `superseded`.
