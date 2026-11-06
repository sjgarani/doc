# Framework de documentação

Um framework de documentação feito para ser reaproveitado em projetos de software. Ele dá
uma forma padronizada de planejar, registrar e acompanhar o desenvolvimento.

A ideia é incluir este repositório em outros projetos com `git subtree`: a estrutura e as
práticas de documentação ficam num só lugar e são sincronizadas em cada projeto que as usa.

## Objetivos

- Dar à documentação técnica uma estrutura padronizada.
- Registrar as decisões de arquitetura e as consequências de cada uma.
- Discutir as mudanças propostas antes de implementá-las.
- Transformar requisitos e decisões em especificações prontas para execução.
- Documentar procedimentos operacionais que pessoas e agentes de IA consigam executar com segurança.
- Manter a ligação entre os documentos e o trabalho de implementação.
- Apoiar o planejamento, o acompanhamento e a revisão do trabalho.

## Estrutura

- [`adrs/`](adrs/): ADRs, os registros das decisões de arquitetura importantes e dos motivos de cada uma.
- [`rfcs/`](rfcs/): RFCs, as propostas maiores que precisam de discussão.
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

1. Quando uma mudança precisar de discussão ampla, comece por uma RFC.
2. Com a proposta aprovada, registre em ADRs as decisões de arquitetura que vão perdurar.
3. Divida o trabalho em Specs, com critérios de aceitação claros e verificáveis.
4. Se uma Spec cria ou altera um procedimento operacional, escreva ou atualize o Runbook
   correspondente e ligue um documento ao outro.
5. Ligue cada documento aos itens de trabalho e às revisões relacionadas.
6. Atualize os status à medida que o trabalho avança.

Os status, as regras de nome e os campos de rastreabilidade de cada tipo estão no README e no
template do diretório correspondente. Enquanto não houver ferramentas de apoio, siga os templates
dentro do fluxo de revisão do projeto.

## Situação do projeto

Este repositório contém o framework de documentação. Ferramentas para criar, validar e
sincronizar documentos podem surgir com o tempo, mas nenhuma é necessária para começar a usar.
