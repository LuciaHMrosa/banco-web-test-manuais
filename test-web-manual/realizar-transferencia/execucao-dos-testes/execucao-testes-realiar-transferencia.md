# 📄 Execução de Testes — Realizar Transferências

# 📌 Funcionalidade

Realizar Transferências

---

# ▶️ Resultado da Execução dos Testes

| ID    | Cenário                                      | Status        | Observações |
|------|---------------------------------------------|--------------|-------------|
| CT001 | Realizar transferência com valores válidos | ❌ Falhou | Sistema exige autenticação para valor exatamente igual a R$5.000,00, porém a regra define que o token só é obrigatório acima de R$5.000,00. |
| CT002 | Exibir erro ao informar valor abaixo do mínimo permitido | ✅ Passou | Sistema exibe mensagem correta de valor mínimo |
| CT003 | Exibir erro ao informar valor inválido | ✅ Passou | Sistema bloqueia valores não numéricos e vazios corretamente |
| CT004 | Realizar transferência acima de R$5.000,00 com token válido | ✅ Passou | Transferência realizada com sucesso |
| CT005 | Exibir erro ao realizar transferência acima de R$5.000,00 sem token | ✅ Passou | Sistema exige autenticação corretamente |
| CT006 | Exibir erro ao informar token inválido | ✅ Passou | Sistema bloqueia autenticação inválida |
| CT007 | Exibir erro ao realizar transferência com conta origem inativa | ✅ Passou | Sistema impede operação corretamente |
| CT008 | Exibir erro ao realizar transferência com saldo insuficiente | ✅ Passou | Sistema bloqueia transferência por saldo insuficiente |
| CT009 | Exibir erro ao realizar transferência para conta destino inativa | ✅ Passou | Sistema bloqueia operação corretamente |
| CT010 | Exibir erro ao não informar valor da transferência | ✅ Passou | Sistema exige valor mínimo corretamente |
| CT011 | Exibir erro ao não selecionar conta origem | ✅ Passou | Sistema retorna erro de conta não encontrada |
| CT012 | Exibir erro ao não selecionar conta destino | ✅ Passou | Sistema retorna erro de conta não encontrada |

---

# 📊 Resumo da Execução

| Métrica                      | Quantidade |
|----------------------------|------------|
| Total de cenários executados | 12 |
| Cenários aprovados           | 11 |
| Cenários reprovados          | 1 |
| Cenários não executados      | 0 |

---

# 👩‍💻 Responsável pela Execução

* Lúcia de Melo