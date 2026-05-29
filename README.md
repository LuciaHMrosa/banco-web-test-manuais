# 🧪 banco-web-tests-manuais

Projeto voltado para estudos e práticas de Qualidade de Software (QA), utilizando a aplicação Banco Web desenvolvida pelo professor Júlio de Lima durante a Mentoria 2.0.

Repositório original da aplicação:

* Banco Web: https://github.com/juliodelimas/banco-web

---

# 🎯 Objetivo

Este repositório foi criado com o objetivo de praticar diferentes abordagens de testes manuais aplicadas à aplicação Banco Web, simulando atividades executadas por profissionais de QA em ambientes reais.

O projeto contempla:

* Análise de funcionalidades
* Levantamento de regras de negócio
* Escrita de cenários BDD com Gherkin
* Escrita de casos de teste seguindo ISO 29119-3
* Aplicação de técnicas de design de testes
* Tabelas de decisão
* Análise de Valor Limite (AVL)
* Particionamento de Equivalência (PE)
* Testes exploratórios
* Documentação de sessões exploratórias
* Organização de evidências de testes

---

# 📚 Funcionalidades Cobertas

## 🔐 Login

Cobertura da funcionalidade de autenticação:

* Cenários positivos e negativos
* Campos obrigatórios
* Credenciais inválidas
* Fluxo de autenticação
* Testes exploratórios de comportamento
* Casos de teste documentados seguindo ISO 29119-3

---

## 💸 Realizar Transferência

Cobertura das regras de negócio relacionadas às transferências:

* Valor mínimo permitido
* Token obrigatório
* Validação de token
* Saldo suficiente
* Contas ativas
* Fluxos positivos e negativos
* Testes exploratórios

---

## 📄 Buscar Transferências

Cobertura da funcionalidade de listagem e paginação:

* Exibição de transferências
* Navegação entre páginas
* Paginação
* Responsividade
* Consistência visual
* Testes exploratórios

---

# 🧠 Técnicas de Teste Aplicadas

Durante a construção dos cenários foram utilizadas técnicas como:

* BDD (Behavior Driven Development)
* Gherkin
* Tabela de Decisão
* Particionamento de Equivalência (PE)
* Análise de Valor Limite (AVL)
* Testes Exploratórios
* Session-Based Test Management (SBTM)

---

# 📁 Estrutura do Projeto

```txt
banco-web-tests-manuais/
│
├── login/
│   ├── analise.md
│   ├── login.feature
│   ├── login-caso-de-teste.md
│   ├── relatorio-sessao-login.md
│   └── evidencias/
│
├── realizar-transferencia/
│   ├── analise.md
│   ├── realizar-transferencia.feature
│   ├── relatorio-sessao-realizar-transferencia.md
│   └── evidencias/
│
├── buscar-transferencia/
│   ├── analise.md
│   ├── buscar-transferencia.feature
│   ├── relatorio-sessao-buscar-transferencia.md
│   └── evidencias/
│
├── README.md
```

---

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
