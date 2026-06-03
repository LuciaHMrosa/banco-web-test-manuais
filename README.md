# 🏦 Banco Web - Projeto de Testes Manuais

Projeto de estudos e prática em Qualidade de Software (QA), utilizando a aplicação Banco Web desenvolvida pelo professor Júlio de Lima na Mentoria 2.0.

🔗 Aplicação base:
https://github.com/juliodelimas/banco-web

---

# 🎯 Objetivo

Este repositório tem como objetivo simular um ambiente real de trabalho de QA, aplicando técnicas de testes manuais em uma aplicação web bancária.

O projeto contempla todo o ciclo de testes:

* Análise de funcionalidades
* Levantamento de requisitos e regras de negócio
* Escrita de cenários BDD (Gherkin)
* Elaboração de casos de teste estruturados seguindo a ISO/IEC/IEEE 29119-3
* Aplicação de técnicas de design de testes
* Execução de testes manuais
* Registro de evidências
* Testes exploratórios (Session-Based Testing)
* Identificação, análise e documentação de defeitos (bugs)

---

# 📚 Funcionalidades Testadas

## 🔐 Login

Cobertura da autenticação de usuários:

* Cenários positivos e negativos
* Validação de credenciais
* Campos obrigatórios
* Fluxo de autenticação
* Casos de teste estruturados (ISO/IEC/IEEE 29119-3)
* Testes exploratórios
* Registro de defeitos encontrados

---

## 💸 Realizar Transferência

Cobertura da funcionalidade de transferência bancária:

* Validação de valor mínimo (R$10,00)
* Regra de autenticação por token para valores acima de R$5.000,00
* Validação de contas ativas
* Validação de saldo suficiente
* Fluxos positivos e negativos
* Casos de teste estruturados (ISO/IEC/IEEE 29119-3)
* Testes exploratórios
* Registro de defeitos funcionais e de validação

---

## 📄 Buscar Transferências

Cobertura da consulta e listagem de transferências:

* Exibição de registros
* Paginação (próxima e página anterior)
* Limite de itens por página
* Consistência de dados
* Comportamento quando não existem registros
* Casos de teste estruturados (ISO/IEC/IEEE 29119-3)
* Testes exploratórios de UI/UX

---

# 🧠 Técnicas de Teste Aplicadas

* BDD (Behavior Driven Development)
* Gherkin
* Particionamento de Equivalência (PE)
* Análise de Valor Limite (AVL)
* Tabela de Decisão
* Testes Exploratórios
* Session-Based Test Management (SBTM)
* ISO/IEC/IEEE 29119-3
* Análise de Requisitos
* Rastreabilidade de Regras de Negócio

---

# 🐞 Defeitos Documentados

Durante a execução dos testes foram identificados e documentados defeitos funcionais e de usabilidade, como por exemplo:

* Validação incorreta da regra de token para transferências acima de R$5.000,00
* Falta de limite para campos de valor e token
* Problemas de atualização de saldo em tempo real
* Permissão indevida de transferência para a mesma conta
* Inconsistências visuais em diferentes resoluções
* Comportamentos inesperados na paginação da listagem

Todos os defeitos possuem documentação detalhada e evidências anexadas.

---

# 📁 Estrutura do Projeto

```txt
banco-web-tests-manuais/
│
├── login/
│   ├── analise-login.md
│   ├── login.feature
│   ├── login-casos-de-teste.md
│   ├── execucao-testes-login.md
│   ├── relatorio-sessao-login.md
│   ├── defeitos/
│   └── evidencias/
│
├── realizar-transferencia/
│   ├── analise-realizar-transferencia.md
│   ├── realizar-transferencia.feature
│   ├── transferencia-casos-de-teste.md
│   ├── execucao-testes-realizar-transferencia.md
│   ├── relatorio-sessao-realizar-transferencia.md
│   ├── defeitos/
│   └── evidencias/
│
├── buscar-transferencia/
│   ├── analise-buscar-transferencia.md
│   ├── buscar-transferencia.feature
│   ├── buscar-transferencia-casos-de-teste.md
│   ├── execucao-testes-buscar-transferencia.md
│   ├── relatorio-sessao-buscar-transferencia.md
│   ├── defeitos/
│   └── evidencias/
│
└── README.md
```

---

# 🥒 BDD / Gherkin

Os cenários foram escritos utilizando Gherkin com foco no comportamento da aplicação, permitindo uma documentação clara e compreensível para pessoas técnicas e não técnicas.

Exemplo:

```gherkin
Cenário: Realizar transferência com valor válido

Quando informar valor "10,00"
E selecionar conta origem ativa
Então o sistema deve realizar transferência com sucesso
```

---

# 📑 Casos de Teste — ISO/IEC/IEEE 29119-3

As funcionalidades de Login, Realizar Transferência e Buscar Transferências possuem documentação de casos de teste estruturados seguindo o padrão ISO/IEC/IEEE 29119-3.

Os casos de teste incluem:

* Identificação única do teste
* Objetivo do teste
* Prioridade
* Rastreabilidade com regras de negócio
* Pré-condições
* Dados de teste
* Procedimento de execução
* Resultados esperados
* Pós-condições

Os cenários documentados foram derivados das análises de requisitos, regras de negócio e cenários BDD desenvolvidos para cada funcionalidade.

---

# 🔍 Testes Exploratórios

As sessões exploratórias foram documentadas utilizando a abordagem Session-Based Test Management (SBTM), contendo:

* Charter da sessão
* Heurísticas utilizadas
* Áreas exploradas
* Riscos identificados
* Defeitos encontrados
* Evidências coletadas
* Observações da sessão

---

# 📌 Técnicas de Design de Teste Utilizadas

Durante o projeto foram aplicadas diferentes técnicas para modelagem e cobertura dos testes:

* Particionamento de Equivalência (PE)
* Análise de Valor Limite (AVL)
* Tabela de Decisão
* Testes Baseados em Regras de Negócio
* Testes Baseados em Cenários
* Testes Exploratórios

---

# 📚 Aprendizados Aplicados

Este projeto permitiu praticar atividades comuns ao dia a dia de um Analista de Testes (QA), incluindo:

* Análise de requisitos
* Identificação de regras de negócio
* Modelagem de cenários de teste
* Escrita de cenários BDD
* Criação de casos de teste estruturados
* Execução de testes manuais
* Testes exploratórios
* Documentação de defeitos
* Rastreabilidade entre requisitos e testes

---

# 📌 Objetivo Educacional

Este projeto possui finalidade exclusivamente educacional e foi desenvolvido como prática de estudos em Qualidade de Software (QA), aplicando conceitos, técnicas e processos utilizados no dia a dia de equipes de testes de software.

---

# 👩‍💻 Autora

Desenvolvido por **Lúcia de Melo** como prática de estudos em QA e Engenharia de Testes.
