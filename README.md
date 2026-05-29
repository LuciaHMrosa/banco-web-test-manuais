# 🧪 banco-web-tests-manuais

Projeto de estudos e prática em Qualidade de Software (QA), utilizando a aplicação Banco Web desenvolvida pelo professor Júlio de Lima na Mentoria 2.0.

🔗 Aplicação base:
https://github.com/juliodelimas/banco-web

---

# 🎯 Objetivo

Este repositório tem como objetivo simular um ambiente real de trabalho de QA, aplicando técnicas de testes manuais em uma aplicação web bancária.

O projeto contempla todo o ciclo de testes:

- Análise de funcionalidades
- Levantamento de regras de negócio
- Escrita de cenários BDD (Gherkin)
- Casos de teste baseados na ISO 29119-3 (Login)
- Execução de testes manuais
- Registro de evidências
- Testes exploratórios (Session-Based Testing)
- Identificação e documentação de defeitos (bugs)
- Aplicação de técnicas de design de testes

---

# 📚 Funcionalidades Testadas

## 🔐 Login

Cobertura da autenticação de usuários:

- Cenários positivos e negativos
- Validação de credenciais
- Campos obrigatórios
- Fluxo de autenticação
- Casos de teste estruturados (ISO 29119-3)
- Testes exploratórios
- Registro de defeitos encontrados

---

## 💸 Realizar Transferência

Cobertura da funcionalidade de transferência bancária:

- Validação de valor mínimo (R$10,00)
- Regra de token acima de R$5.000,00
- Validação de contas ativas
- Validação de saldo suficiente
- Fluxos positivos e negativos
- Testes exploratórios
- Registro de bugs funcionais e de validação

---

## 📄 Buscar Transferências

Cobertura da listagem de transferências:

- Exibição de registros
- Paginação (próxima/anterior página)
- Limite de itens por página
- Consistência de dados
- Responsividade da interface
- Testes exploratórios de UI/UX

---

# 🧠 Técnicas de Teste Aplicadas

- BDD (Behavior Driven Development)
- Gherkin
- Particionamento de Equivalência (PE)
- Análise de Valor Limite (AVL)
- Tabela de Decisão
- Testes Exploratórios
- Session-Based Test Management (SBTM)
- ISO/IEC/IEEE 29119-3 (casos de teste estruturados)

---

# 🐞 Defeitos Documentados

Durante os testes foram identificados e registrados defeitos como por exemplo:

- Validação incorreta de regra de token (limite de R$5.000,00)
- Falta de limite em campos de valor e token
- Problemas de atualização de saldo em tempo real
- Permissão de transferência para mesma conta
- Inconsistências visuais em responsividade
- Comportamento inesperado em paginação

Todos os defeitos estão documentados na pasta `/defeitos` com evidências em `/evidencias`.

---

# 📁 Estrutura do Projeto

```txt
banco-web-tests-manuais/
│
├── login/
│   ├── analise-login.md
│   ├── login.feature
│   ├── login-caso-de-teste.md
│   ├── execucao-testes-login.md
│   ├── relatorio-sessao-login.md
│   ├── defeitos/
│   └── evidencias/
│
├── realizar-transferencia/
│   ├── analise-realizar-transferencia.md
│   ├── realizar-transferencia.feature
│   ├── execucao-testes-realizar-transferencia.md
│   ├── relatorio-sessao-realizar-transferencia.md
│   ├── defeitos/
│   └── evidencias/
│
├── buscar-transferencia/
│   ├── analise-buscar-transferencia.md
│   ├── buscar-transferencia.feature
│   ├── execucao-testes-buscar-transferencia.md
│   ├── relatorio-sessao-buscar-transferencia.md
│   ├── defeitos/
│   └── evidencias/
│
├── README.md


```


# 🥒 BDD / Gherkin

Os cenários foram escritos utilizando Gherkin com foco em comportamento da aplicação.

Exemplo:

```gherkin
Cenário: Realizar transferência com valor válido
  Quando informar valor "10,00"
  E selecionar conta origem ativa
  Então o sistema deve realizar transferência com sucesso
```

---

# 📑 Casos de Teste — ISO 29119-3

A funcionalidade de Login também possui documentação de casos de teste estruturados seguindo o padrão ISO 29119-3, com:

* pré-condições
* passos de execução
* resultados esperados
* pós-condições
* rastreabilidade

---

# 🔍 Testes Exploratórios

As sessões exploratórias foram documentadas utilizando abordagem baseada em Session-Based Test Management (SBTM), contendo:

* charter
* heurísticas utilizadas
* cobertura explorada
* riscos identificados
* defeitos encontrados
* observações da sessão

---

# 📌 Objetivo Educacional

Este projeto possui finalidade exclusivamente educacional e foi desenvolvido como prática de estudos em Qualidade de Software (QA), aplicando conceitos utilizados no dia a dia de times de testes.

---

# 👩‍💻 Autora

Desenvolvido por Lúcia de Melo como prática de estudos em QA e Engenharia de Testes.
