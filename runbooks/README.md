# Runbooks

Aqui ficam os **Runbooks** do projeto. Um Runbook é um procedimento operacional, passo a passo, que pode ser executado por um desenvolvedor, por um operador ou por um **agente de IA**. Os Runbooks cobrem operações recorrentes, manutenção de rotina e resposta a incidentes, como trocar credenciais, restaurar um backup ou pôr de pé um serviço que caiu.

---

## Ciclo de vida

O status de um Runbook muda pelo fluxo de revisão do projeto.

| Status | Significado |
| :--- | :--- |
| `draft` | Procedimento em redação, ou que nunca foi executado do início ao fim. |
| `active` | Procedimento verificado (`last_verified_at` preenchido) e liberado para execução. |
| `deprecated` | O procedimento não se aplica mais, porque o sistema ou a operação foi desativado ou substituído. O arquivo continua no repositório como histórico. |

---

## Nome dos arquivos

O nome começa com um número sequencial de 4 dígitos, seguido do título em `kebab-case`:

```text
NNNN-acao-ou-cenario.md
```

**Exemplos:**
- `0001-trocar-credenciais-do-banco-de-dados.md`
- `0002-restaurar-servico-a-partir-do-backup.md`

---

## Como criar e atualizar um Runbook

Use o `template.md` como base e o próximo ID livre. Diga quando o procedimento deve ser
executado, o que ele exige e quais são os riscos. Depois escreva cada passo com o comando, o
resultado esperado e o que fazer se ele falhar. Nunca coloque segredos em um Runbook: indique
onde obtê-los, seja o cofre de segredos ou o responsável pela credencial.

Ligue o Runbook às Specs e aos ADRs de que ele deriva (`related_specs`, `related_adrs`) e
inclua-o em `related_runbooks` nessas Specs. Envie o Runbook para revisão e só passe para
`active` depois de uma execução completa bem-sucedida, registrada em `last_verified_at`.

Quando o sistema mudar, atualize os passos e o `updated_at`. O `last_verified_at` só muda depois
da próxima execução bem-sucedida. Por enquanto esse fluxo é manual; a automação pode vir depois.

---

## Orientações para agentes de IA

1. **Instruções para agentes de IA**:
   - Execute apenas Runbooks `active`. Runbooks `draft` ainda não foram verificados, e os `deprecated` nunca devem ser executados.
   - Siga a seção **Regras de execução para agentes de IA**: execute direto os passos listados em **Executar sem confirmação**, peça confirmação humana antes de qualquer passo listado em **Exige confirmação humana** e pare assim que ocorrer qualquer situação de **Quando parar**.
   - Se o resultado de um passo não for o **Resultado esperado**, siga o que diz **Se falhar** em vez de continuar.
   - Ao redigir um Runbook, consulte as Specs, os ADRs e o código relacionados para levantar os comandos, os riscos e os passos de rollback.
