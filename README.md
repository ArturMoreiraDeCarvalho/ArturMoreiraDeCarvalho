# Artur Moreira de Carvalho

Desenvolvedor de Software Júnior · Backend PHP/Laravel, SQL/Oracle e Python · Sistemas financeiros e contábeis multi-tenant · IA aplicada

Belo Horizonte, MG · [Portfólio](https://arturmoreiradecarvalho.github.io/artur-portfolio/) · [LinkedIn](https://www.linkedin.com/in/artur-moreira-de-carvalho3336/) · [English summary](#in-english)

## Quem sou

Sou desenvolvedor de software júnior na PZM Enterprise (Grupo PZM). Trabalho no backend de uma plataforma SaaS multi-tenant de conciliação contábil, com PHP 8/Laravel, PHP legado e Oracle SQL. Comecei como estagiário em 2024 e hoje entrego funcionalidades e correções em conciliação, cronograma de fechamento, tributos e obrigações e lançamentos manuais.

Uso Python para automatizar validação e curadoria de dados e para criar ferramentas de desenvolvimento. No dia a dia, trabalho com agentes de código e escrevo as regras e o contexto que eles usam.

## O que faço

- **Backend:** regras de negócio contábeis, isolamento por cliente (tenant), autorização no servidor, reautenticação para ações críticas e consultas SQL em Oracle (views, sequences, scripts de migração).
- **Dados financeiros e contábeis:** importação de balancetes com verificação de duplicidade, validação de entrada, relatórios e exportação para Excel, indicadores de conciliação.
- **Qualidade:** testes automatizados com PHPUnit/Pest, Cypress e pytest. Introduzi o Cypress no projeto (configuração, comandos e testes E2E de login e aprovação).
- **IA aplicada:** projetei e desenvolvo o PERKUS, um assistente de conciliação contábil com núcleo determinístico e um modelo de IA externo usado com limites claros (detalhes abaixo).
- **Desenvolvimento assistido por IA:** regras e contexto para agentes de código, um servidor MCP local com ferramentas somente leitura e um grafo de conhecimento do código em SQLite. São ferramentas internas e não estão publicadas.

## Stack

| Onde | Tecnologias |
| --- | --- |
| Trabalho | PHP 8, Laravel, PHP legado, Oracle SQL, JavaScript, PHPUnit/Pest, Cypress, Docker (ambiente local), Git |
| Projetos públicos | Python 3.11+, pytest, ruff, pydantic, typer, Node.js, OpenAPI, Docker, GitHub Actions |

## Case principal: PERKUS

Assistente de conciliação contábil dentro da plataforma do Grupo PZM. Código proprietário: aqui descrevo só o problema, a arquitetura e as decisões.

- **Problema:** quem trabalha com conciliação, fechamento e apuração precisa de orientação e de consultas operacionais na própria tela (prazos, pendências, aprovações, saldos), sem quebrar permissões nem o isolamento entre clientes.
- **Arquitetura:** pipeline determinístico em PHP 8/Laravel. Interpretação por regras, recuperação lexical sobre uma base de conhecimento curada e consultas Oracle aos dados do próprio cliente. Respostas montadas por templates, com contrato de resposta validado.
- **Onde entra a IA:** um modelo externo, via API, só classifica a intenção da pergunta, sinaliza risco de prompt injection e desempata respostas candidatas. Ele não gera o texto da resposta e não consulta dados.
- **Controles:** identidade, tenant e permissões resolvidos no servidor. Dados mascarados antes de chegar ao modelo. Respostas tipadas validadas. Timeout, circuit breaker e volta ao caminho determinístico se o modelo falhar. Avaliação offline com conjunto reservado e casos adversariais.
- **Meu papel:** projetei a arquitetura e desenvolvo o módulo como único desenvolvedor, com desenvolvimento assistido por agentes de IA.
- **Status:** em desenvolvimento. Ainda não foi implantado em produção.

[Ler o case completo no portfólio →](https://arturmoreiradecarvalho.github.io/artur-portfolio/#perkus)

## Projetos públicos

| Projeto | O que é | Stack |
| --- | --- | --- |
| [TrilhaDocs](https://github.com/ArturMoreiraDeCarvalho/trilhadocs) | CLI local que valida o inventário de uma carga de documentos contábeis, organiza capas e anexos em ZIPs com manifestos e verifica a integridade do resultado. Dados sintéticos. | Python, pydantic, typer, pypdf, pytest, CI Ubuntu/Windows |
| [Data Quality CLI](https://github.com/ArturMoreiraDeCarvalho/python-data-quality-cli) | Projeto de estudo: valida CSV (colunas obrigatórias, duplicidades, campos vazios, datas) e gera relatório em texto ou JSON. | Python, pytest, GitHub Actions |
| [Task Health API](https://github.com/ArturMoreiraDeCarvalho/node-rest-api-healthcheck) | Projeto de estudo: API REST didática com health check, armazenamento em memória e contrato OpenAPI. | Node.js, node:test, Docker |
| [Portfólio](https://github.com/ArturMoreiraDeCarvalho/artur-portfolio) | Site estático com os cases e a experiência. | HTML, CSS |

## Contato

Busco oportunidades júnior em backend ou desenvolvimento de software, de preferência em sistemas financeiros, dados ou produtos com IA aplicada. O melhor canal é o [LinkedIn](https://www.linkedin.com/in/artur-moreira-de-carvalho3336/).

---

## In English

Junior software developer at PZM Enterprise (Grupo PZM) in Belo Horizonte, Brazil. I work on the backend of a multi-tenant SaaS platform for accounting reconciliation, using PHP 8/Laravel, legacy PHP and Oracle SQL. I use Python for data validation, data curation and developer tooling.

My main project is **PERKUS**, an accounting reconciliation assistant. I designed its architecture and I am the only developer on the module, working with AI coding agents. Its core is deterministic: rules, lexical retrieval over a curated knowledge base, and queries over each tenant's own data with server-side access control. An external AI model is used only to classify intent, flag prompt-injection risk and break ties between candidate answers. Data is masked before it reaches the model, and every call has a timeout, a circuit breaker and a deterministic fallback. It is still in development and has not been deployed to production.

Public code: [TrilhaDocs](https://github.com/ArturMoreiraDeCarvalho/trilhadocs) (Python CLI for verifiable packaging of accounting documents), [Data Quality CLI](https://github.com/ArturMoreiraDeCarvalho/python-data-quality-cli) and [Task Health API](https://github.com/ArturMoreiraDeCarvalho/node-rest-api-healthcheck) (study projects). English level: intermediate.
