# Artur Moreira de Carvalho

**Desenvolvedor de Software Júnior** · Backend PHP/Laravel, SQL/Oracle e Python · Sistemas financeiros e contábeis

Belo Horizonte, MG · [Portfólio](https://arturmoreiradecarvalho.github.io/artur-portfolio/) · [CV (PDF)](https://arturmoreiradecarvalho.github.io/artur-portfolio/assets/cv/artur-moreira-de-carvalho-curriculo-pt-BR.pdf) · [LinkedIn](https://www.linkedin.com/in/artur-moreira-de-carvalho3336/) · [English](#in-english)

Desenvolvo o backend de uma plataforma SaaS multi-tenant de conciliação contábil na PZM Enterprise (Grupo PZM), com PHP 8/Laravel, PHP legado e Oracle SQL. Entrei como estagiário em 2024 e hoje sou desenvolvedor júnior.

- **Backend e regras de negócio:** conciliação contábil, cronograma de fechamento, tributos e obrigações e lançamentos manuais, com isolamento por cliente (tenant) e autorização no servidor.
- **SQL/Oracle:** consultas, views, sequences e scripts de migração; importação de balancetes com verificação de duplicidade e validação de entrada.
- **Testes automatizados:** PHPUnit/Pest e Cypress (introduzi o Cypress no projeto); pytest nos projetos Python.
- **Sustentação:** investigo divergências de dados e falhas até a causa raiz.
- **Python:** scripts de validação e curadoria de dados e ferramentas de desenvolvimento.
- **Desenvolvimento assistido por agentes de IA:** escrevo as regras e o contexto que os agentes de código seguem. Criei um servidor MCP local, somente leitura, e um grafo de conhecimento do código (ferramentas internas, não publicadas).

## Case: Assistente de Contabilidade com IA

Projetei a arquitetura e desenvolvo, como único desenvolvedor, o Assistente de Contabilidade com IA, um sistema de apoio à conciliação contábil. O núcleo é determinístico: regras, recuperação lexical em uma base de conhecimento curada e consultas Oracle aos dados do próprio cliente, com permissões resolvidas no servidor. Um modelo de IA externo só classifica a intenção da pergunta, sinaliza risco de prompt injection e desempata respostas candidatas, sempre sobre dados mascarados e com fallback determinístico. Está em desenvolvimento e ainda não foi implantado em produção. O código é proprietário.

[Ler o case no portfólio →](https://arturmoreiradecarvalho.github.io/artur-portfolio/#assistente-conciliacao) · [Ver a demonstração em vídeo (35 s, dados fictícios) →](https://arturmoreiradecarvalho.github.io/artur-portfolio/#demonstracao)

## Projetos públicos

| Projeto | O que é | Stack |
| --- | --- | --- |
| [TrilhaDocs](https://github.com/ArturMoreiraDeCarvalho/trilhadocs) | CLI local que valida o inventário de uma carga de documentos contábeis, organiza capas e anexos em ZIPs com manifestos e verifica a integridade do resultado. Dados sintéticos. | Python, pydantic, typer, pypdf, pytest, CI Ubuntu/Windows |
| [Data Quality CLI](https://github.com/ArturMoreiraDeCarvalho/python-data-quality-cli) | Projeto de estudo: valida CSV (colunas obrigatórias, duplicidades, campos vazios, datas) e gera relatório em texto ou JSON. | Python, pytest, GitHub Actions |
| [Task Health API](https://github.com/ArturMoreiraDeCarvalho/node-rest-api-healthcheck) | Projeto de estudo: API REST didática com health check, armazenamento em memória e contrato OpenAPI. | Node.js, node:test, Docker |
| [Portfólio](https://github.com/ArturMoreiraDeCarvalho/artur-portfolio) | Site estático com os cases, a experiência e o currículo. | HTML, CSS |

## Stack

| Onde | Tecnologias |
| --- | --- |
| Trabalho | PHP 8, Laravel, PHP legado, Oracle SQL, JavaScript, Python (scripts e ferramentas), PHPUnit/Pest, Cypress, Docker (ambiente local), Git |
| Projetos públicos | Python 3.11+, pytest, ruff, pydantic, typer, Node.js, OpenAPI, Docker, GitHub Actions |

## Contato

[LinkedIn](https://www.linkedin.com/in/artur-moreira-de-carvalho3336/) · [Portfólio](https://arturmoreiradecarvalho.github.io/artur-portfolio/) · Currículo em PDF: [português](https://arturmoreiradecarvalho.github.io/artur-portfolio/assets/cv/artur-moreira-de-carvalho-curriculo-pt-BR.pdf) · [inglês](https://arturmoreiradecarvalho.github.io/artur-portfolio/assets/cv/artur-moreira-de-carvalho-resume-en.pdf)

---

## In English

Junior software developer at PZM Enterprise (Grupo PZM) in Belo Horizonte, Brazil. I work on the backend of a multi-tenant SaaS platform for accounting reconciliation, using PHP 8/Laravel, legacy PHP and Oracle SQL, with automated tests (PHPUnit/Pest, Cypress). I use Python for data validation, data curation and developer tooling, and I work daily with AI coding agents.

My main project is the AI Accounting Assistant, a support system for accounting reconciliation ([35-second demo video](https://arturmoreiradecarvalho.github.io/artur-portfolio/en/#demo), fictional data). I designed its architecture and I am the only developer on the module. Its core is deterministic; an external AI model only classifies intent, flags prompt-injection risk and breaks ties between candidate answers, on masked data and with a deterministic fallback. It is still in development and has not been deployed to production. English level: intermediate.

[Portfolio (EN)](https://arturmoreiradecarvalho.github.io/artur-portfolio/en/) · [Résumé (PDF)](https://arturmoreiradecarvalho.github.io/artur-portfolio/assets/cv/artur-moreira-de-carvalho-resume-en.pdf) · [LinkedIn](https://www.linkedin.com/in/artur-moreira-de-carvalho3336/)
