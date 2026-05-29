# 📄 Execução de Testes — Buscar Transferências

# 📌 Funcionalidade

Buscar Transferências

---

# ▶️ Resultado da Execução dos Testes

| ID    | Cenário                                      | Status        | Observações                                                                 |
|------|---------------------------------------------|--------------|------------------------------------------------------------------------------|
| CT001 | Exibir lista de transferências realizadas   | ✅ Passou     | Lista exibida corretamente com registros de transferências.                 |
| CT002 | Navegar para próxima página da listagem     | ✅ Passou     | Paginação funcionando corretamente, avançando para próxima página.          |
| CT003 | Navegar para página anterior da listagem    | ✅ Passou     | Retorno para página anterior funcionando corretamente.                       |
| CT004 | Validar limite de itens por página          | ✅ Passou     | Sistema exibe 5 registros por página consistentemente.                      |
| CT005 | Exibir mensagem sem transferências          | ⛔ Não executado | Necessita limpeza de dados no banco de dados para execução.                 |
| CT006 | Validar consistência após atualização       | ✅ Passou     | Dados permanecem consistentes após atualização da página.                   |

---

# 📊 Resumo da Execução

| Métrica                      | Quantidade |
|----------------------------|------------|
| Total de cenários executados | 6          |
| Cenários aprovados           | 5          |
| Cenários reprovados          | 0          |
| Cenários não executados      | 1          |

---

# 👩‍💻 Responsável pela Execução

* Lúcia de Melo