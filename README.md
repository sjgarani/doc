# Framework de documentação

Um framework de documentação feito para ser reaproveitado em projetos de software. Ele dá
uma forma padronizada de planejar, registrar e acompanhar o desenvolvimento.

A ideia é incluir este repositório em outros projetos com `git subtree`: a estrutura e as
práticas de documentação ficam num só lugar e são sincronizadas em cada projeto que as usa.

## Objetivos

- Dar à documentação técnica uma estrutura padronizada.
- Registrar os requisitos de produto, os problemas dos usuários e as métricas de sucesso antes do design técnico.
- Registrar as decisões de arquitetura e as consequências de cada uma.
- Discutir as mudanças propostas antes de implementá-las.
- Transformar requisitos e decisões em especificações prontas para execução.
- Documentar procedimentos operacionais que pessoas e agentes de IA consigam executar com segurança.
- Manter a ligação entre os documentos e o trabalho de implementação.
- Apoiar o planejamento, o acompanhamento e a revisão do trabalho.

## Estrutura

- [`prds/`](prds/): PRDs, os documentos de requisitos de produto que definem problemas dos usuários, objetivos, métricas de sucesso e escopo.
- [`rfcs/`](rfcs/): RFCs, as propostas maiores que precisam de discussão.
- [`adrs/`](adrs/): ADRs, os registros das decisões de arquitetura importantes e dos motivos de cada uma.
- [`specs/`](specs/): Specs, as especificações técnicas e funcionais que guiam a implementação.
- [`runbooks/`](runbooks/): Runbooks, os procedimentos passo a passo para operações recorrentes, manutenção e resposta a incidentes.

Cada diretório tem um `README.md` e um template para começar. Mantenha sempre em dia o ID, o
status e os links de cada documento para o trabalho relacionado.

## Como usar como subtree

No projeto que vai usar o framework, adicione este repositório como subtree em um diretório
próprio:

```bash
git remote add doc2gh <REPOSITORY_URL>
git fetch doc2gh
git subtree add --prefix=docs/doc2gh doc2gh main --squash
```

Para receber as atualizações depois:

```bash
git fetch doc2gh
git subtree pull --prefix=docs/doc2gh doc2gh main --squash
```

Troque o diretório e o branch conforme o projeto.

## Fluxo recomendado

1. Quando for definir uma funcionalidade do produto, o problema do usuário e as métricas de sucesso, comece por um PRD.
2. Quando uma mudança técnica precisar de discussão ampla, escreva uma RFC.
3. Com a proposta aprovada, registre em ADRs as decisões de arquitetura que vão perdurar.
4. Divida o trabalho em Specs, com critérios de aceitação claros e verificáveis.
5. Se uma Spec cria ou altera um procedimento operacional, escreva ou atualize o Runbook
   correspondente e ligue um documento ao outro.
6. Ligue cada documento aos documentos de que ele deriva, aos itens de trabalho e às revisões relacionadas.
7. Atualize os status à medida que o trabalho avança.

Os status, as regras de nome e os campos de rastreabilidade de cada tipo estão no README e no
template do diretório correspondente. Enquanto não houver ferramentas de apoio, siga os templates
dentro do fluxo de revisão do projeto.

## Situação do projeto

Este repositório contém o framework de documentação. Ferramentas para criar, validar e
sincronizar documentos podem surgir com o tempo, mas nenhuma é necessária para começar a usar.

## Licença

Distribuído sob a [MIT License](LICENSE).
