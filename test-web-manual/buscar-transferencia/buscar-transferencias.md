# 📄 QA - Análise da Funcionalidade Buscar Transferências

# 📌 Funcionalidade

Buscar Transferências

---

# 🎯 Objetivo

Validar o comportamento da funcionalidade de consulta de transferências, garantindo que o sistema exiba corretamente as movimentações realizadas, respeitando regras de paginação, navegação e exibição de registros.

---

# 📌 Regras de Negócio

## 🔍 Regras para buscar transferências

* As transferências podem ser consultadas de forma paginada.
* Deve existir limite por página.
* Deve existir navegação por página especificada.
* Deve ser possível consultar todas as transferências realizadas.

---

# 📥 Entradas Identificadas

* Página atual
* Navegação entre páginas
* Quantidade de registros
* Transferências cadastradas

---

# ✔️ Validações Identificadas

* Exibição da listagem de transferências
* Quantidade de registros por página
* Navegação da paginação
* Exibição de transferências cadastradas
* Consistência visual da listagem
* Exibição correta em diferentes páginas
* Comportamento quando não existirem registros

---

# 🟢 Cenários Positivos Identificados

* Exibir transferências cadastradas
* Navegar para próxima página
* Navegar para página anterior
* Exibir quantidade correta de itens por página
* Consultar todas as transferências cadastradas

---

# 🔴 Cenários Negativos Identificados

* Exibir comportamento quando não existirem transferências
* Navegar para página inexistente
* Validar inconsistência visual da paginação
* Validar comportamento da interface em resoluções menores

---

# 🧠 Técnicas de Design de Teste Aplicadas

# 📌 Particionamento de Equivalência (PE)

## 📄 Paginação

### Classes válidas

* Página existente
* Página com registros
* Última página parcialmente preenchida

### Classes inválidas

* Página inexistente
* Página sem registros
* Navegação inválida

---

## 📋 Quantidade de registros

### Classes válidas

* Quantidade de itens dentro do limite esperado

### Classes inválidas

* Quantidade inconsistente de itens
* Registros duplicados
* Registros ausentes

---

# 📋 Tabela de Decisão

| Caso de Teste | Transferências Existentes | Página                | Resultado Esperado                       |
| ------------- | ------------------------- | --------------------- | ---------------------------------------- |
| CT001         | Sim                       | Primeira página       | Exibir transferências cadastradas        |
| CT002         | Sim                       | Próxima página        | Exibir próximos registros                |
| CT003         | Sim                       | Página anterior       | Exibir registros anteriores              |
| CT004         | Sim                       | Última página         | Exibir registros restantes               |
| CT005         | Sim                       | Todas as páginas      | Exibir todas as transferências           |
| CT006         | Não                       | Primeira página       | Exibir mensagem de nenhuma transferência |
| CT007         | Sim                       | Atualização da página | Manter consistência da listagem          |
| CT008         | Sim                       | Resolução menor       | Interface permanece utilizável           |

