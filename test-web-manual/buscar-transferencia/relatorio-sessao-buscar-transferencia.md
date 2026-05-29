# 📄 Relatório de Sessão Exploratória — Buscar Transferências

Inspirado no artigo de John Bach sobre Session-Based Test Management (2001)

| Data e Hora do Início | Nome do Testador | Módulo                |
| --------------------- | ---------------- | --------------------- |
| 28/05/2026            | Lúcia de Melo    | Buscar Transferências |

---

# 🎯 Test Charter

Explorar o comportamento da listagem de transferências, avaliando paginação, exibição dos registros, navegação entre páginas e comportamento visual da interface em diferentes resoluções.

---

# ⏱️ Tamanho da Sessão

30 minutos

---

# 🔍 Heurísticas Utilizadas

* Paginação
* Navegação entre páginas
* Responsividade
* Consistência visual
* Quantidade de registros exibidos
* Mensagens de erro
* Comportamento da interface em diferentes resoluções
* Usabilidade da navegação

---

# 📌 Cobertura Explorada

* Listagem de transferências
* Quantidade de itens por página
* Navegação da paginação
* Exibição visual dos botões
* Responsividade da interface
* Comportamento de mensagens de erro

---

# 📝 Notas*

* (I) Cada página da listagem de transferências exibe apenas 5 registros.

* (I) O comportamento observado indica que o limite padrão da paginação pode ser de 5 transferências por página.

* (R) Ao alterar a resolução da tela, os botões da listagem apresentam comportamento visual inconsistente.

* (R) Os botões da paginação apresentam nomenclatura pouco intuitiva.

* (R) Em resoluções menores, mensagens de erro começam a se sobrepor visualmente na interface.

* (R) O acúmulo visual das mensagens pode comprometer usabilidade e experiência do usuário.

(*) Podem ser (I)nformações ou (R)iscos.

---

# 🐞 Defeitos Identificados

1. Inconsistência visual dos botões em resoluções menores.

2. Nomenclatura pouco intuitiva dos botões de paginação.

3. Sobreposição visual de mensagens de erro em telas reduzidas.

---

# ❓ Perguntas

1. O limite esperado da paginação é realmente de 5 itens?

2. Existe definição oficial para nomenclatura dos botões?

3. O comportamento responsivo da interface foi especificado?

4. Existe tratamento planejado para mensagens de erro em telas menores?
