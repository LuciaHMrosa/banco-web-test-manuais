# 📑 Casos de Teste — ISO/IEC/IEEE 29119-3

# CT001 - Realizar transferência com valores válidos

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT001                                                                              |
| Título          | Realizar transferência com valores válidos                                         |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN001, RN004, RN005, RN006                                                         |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor    |
| -------- |
| 10,00    |
| 10,01    |
| 4.999,99 |
| 5.000,00 |

## Procedimento de Teste

| Passo | Ação                                                   | Resultado Esperado                      |
| ----- | ------------------------------------------------------ | --------------------------------------- |
| 1     | Informar um valor válido para transferência            | O valor é aceito pelo sistema           |
| 2     | Selecionar uma conta origem ativa com saldo suficiente | Conta origem selecionada                |
| 3     | Selecionar uma conta destino ativa                     | Conta destino selecionada               |
| 4     | Solicitar a transferência                              | A transferência é realizada com sucesso |
| 5     | Consultar os saldos das contas                         | Os saldos são atualizados corretamente  |

## Pós-Condições

* Transferência registrada.
* Saldos atualizados.

---

# CT002 - Exibir erro ao informar valor abaixo do mínimo permitido

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT002                                                                              |
| Título          | Exibir erro ao informar valor abaixo do mínimo permitido                           |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN001                                                                              |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor |
| ----- |
| -1    |
| 0     |
| 9,99  |

## Procedimento de Teste

| Passo | Ação                             | Resultado Esperado                           |
| ----- | -------------------------------- | -------------------------------------------- |
| 1     | Informar valor abaixo de R$10,00 | Valor informado                              |
| 2     | Selecionar conta origem ativa    | Conta selecionada                            |
| 3     | Selecionar conta destino ativa   | Conta selecionada                            |
| 4     | Solicitar a transferência        | Sistema exibe erro de valor mínimo permitido |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT003 - Exibir erro ao informar valor inválido

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT003                                                                              |
| Título          | Exibir erro ao informar valor inválido                                             |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN001                                                                              |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor |
| ----- |
| abc   |
| @#!   |
| vazio |

## Procedimento de Teste

| Passo | Ação                           | Resultado Esperado                   |
| ----- | ------------------------------ | ------------------------------------ |
| 1     | Informar valor inválido        | Valor informado                      |
| 2     | Selecionar conta origem ativa  | Conta selecionada                    |
| 3     | Selecionar conta destino ativa | Conta selecionada                    |
| 4     | Solicitar a transferência      | Sistema exibe erro de valor inválido |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT004 - Realizar transferência acima de R$5.000,00 com token válido

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT004                                                                              |
| Título          | Realizar transferência acima de R$5.000,00 com token válido                        |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN002, RN003, RN004, RN005, RN006                                                  |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor    | Token  |
| -------- | ------ |
| 5.000,01 | 123456 |
| 7.000,00 | 123456 |

## Procedimento de Teste

| Passo | Ação                                               | Resultado Esperado                  |
| ----- | -------------------------------------------------- | ----------------------------------- |
| 1     | Informar valor acima de R$5.000,00                 | Valor aceito                        |
| 2     | Informar token válido                              | Token aceito                        |
| 3     | Selecionar conta origem ativa com saldo suficiente | Conta selecionada                   |
| 4     | Selecionar conta destino ativa                     | Conta selecionada                   |
| 5     | Solicitar a transferência                          | Transferência realizada com sucesso |

## Pós-Condições

* Transferência registrada.
* Saldos atualizados.

---

# CT005 - Exibir erro ao realizar transferência acima de R$5.000,00 sem token

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT005                                                                              |
| Título          | Exibir erro ao realizar transferência acima de R$5.000,00 sem token                |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN002                                                                              |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor    |
| -------- |
| 5.000,01 |
| 7.000,00 |

## Procedimento de Teste

| Passo | Ação                               | Resultado Esperado                      |
| ----- | ---------------------------------- | --------------------------------------- |
| 1     | Informar valor acima de R$5.000,00 | Valor informado                         |
| 2     | Não informar token                 | Campo permanece vazio                   |
| 3     | Selecionar conta origem ativa      | Conta selecionada                       |
| 4     | Selecionar conta destino ativa     | Conta selecionada                       |
| 5     | Solicitar a transferência          | Sistema exibe erro de token obrigatório |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT006 - Exibir erro ao informar token inválido

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT006                                                                              |
| Título          | Exibir erro ao informar token inválido                                             |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN002, RN003                                                                       |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor    | Token |
| -------- | ----- |
| 5.000,01 | abc   |
| 7.000,00 | 999   |

## Procedimento de Teste

| Passo | Ação                               | Resultado Esperado                   |
| ----- | ---------------------------------- | ------------------------------------ |
| 1     | Informar valor acima de R$5.000,00 | Valor aceito                         |
| 2     | Informar token inválido            | Token informado                      |
| 3     | Selecionar conta origem ativa      | Conta selecionada                    |
| 4     | Selecionar conta destino ativa     | Conta selecionada                    |
| 5     | Solicitar a transferência          | Sistema exibe erro de token inválido |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.
# CT007 - Exibir erro ao realizar transferência com conta origem inativa

| Campo           | Descrição                                                       |
| --------------- | --------------------------------------------------------------- |
| ID              | CT007                                                           |
| Título          | Exibir erro ao realizar transferência com conta origem inativa  |
| Prioridade      | Alta                                                            |
| Rastreabilidade | RN004                                                           |
| Pré-Condições   | Usuário autenticado. Conta origem inativa. Conta destino ativa. |

## Dados de Teste

| Valor    |
| -------- |
| 10,00    |
| 5.000,01 |

## Procedimento de Teste

| Passo | Ação                                 | Resultado Esperado                                            |
| ----- | ------------------------------------ | ------------------------------------------------------------- |
| 1     | Informar um valor para transferência | Valor aceito pelo sistema                                     |
| 2     | Selecionar uma conta origem inativa  | Conta selecionada                                             |
| 3     | Selecionar uma conta destino ativa   | Conta selecionada                                             |
| 4     | Solicitar a transferência            | Sistema exibe erro informando que a conta origem está inativa |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT008 - Exibir erro ao realizar transferência com saldo insuficiente

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT008                                                                              |
| Título          | Exibir erro ao realizar transferência com saldo insuficiente                       |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN006                                                                              |
| Pré-Condições   | Usuário autenticado. Conta origem ativa sem saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor    |
| -------- |
| 10,00    |
| 5.000,01 |

## Procedimento de Teste

| Passo | Ação                                                   | Resultado Esperado                       |
| ----- | ------------------------------------------------------ | ---------------------------------------- |
| 1     | Informar um valor para transferência                   | Valor aceito pelo sistema                |
| 2     | Selecionar uma conta origem ativa sem saldo suficiente | Conta selecionada                        |
| 3     | Selecionar uma conta destino ativa                     | Conta selecionada                        |
| 4     | Solicitar a transferência                              | Sistema exibe erro de saldo insuficiente |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT009 - Exibir erro ao realizar transferência para conta destino inativa

| Campo           | Descrição                                                                            |
| --------------- | ------------------------------------------------------------------------------------ |
| ID              | CT009                                                                                |
| Título          | Exibir erro ao realizar transferência para conta destino inativa                     |
| Prioridade      | Alta                                                                                 |
| Rastreabilidade | RN005                                                                                |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino inativa. |

## Dados de Teste

| Valor    |
| -------- |
| 10,00    |
| 5.000,01 |

## Procedimento de Teste

| Passo | Ação                                                   | Resultado Esperado                                             |
| ----- | ------------------------------------------------------ | -------------------------------------------------------------- |
| 1     | Informar um valor para transferência                   | Valor aceito pelo sistema                                      |
| 2     | Selecionar uma conta origem ativa com saldo suficiente | Conta selecionada                                              |
| 3     | Selecionar uma conta destino inativa                   | Conta selecionada                                              |
| 4     | Solicitar a transferência                              | Sistema exibe erro informando que a conta destino está inativa |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT010 - Exibir erro ao não informar valor da transferência

| Campo           | Descrição                                                                          |
| --------------- | ---------------------------------------------------------------------------------- |
| ID              | CT010                                                                              |
| Título          | Exibir erro ao não informar valor da transferência                                 |
| Prioridade      | Alta                                                                               |
| Rastreabilidade | RN007                                                                              |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. Conta destino ativa. |

## Dados de Teste

| Valor |
| ----- |
| vazio |

## Procedimento de Teste

| Passo | Ação                                                   | Resultado Esperado                          |
| ----- | ------------------------------------------------------ | ------------------------------------------- |
| 1     | Não informar valor da transferência                    | Campo permanece vazio                       |
| 2     | Selecionar uma conta origem ativa com saldo suficiente | Conta selecionada                           |
| 3     | Selecionar uma conta destino ativa                     | Conta selecionada                           |
| 4     | Solicitar a transferência                              | Sistema exibe mensagem de campo obrigatório |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT011 - Exibir erro ao não selecionar conta origem

| Campo           | Descrição                                  |
| --------------- | ------------------------------------------ |
| ID              | CT011                                      |
| Título          | Exibir erro ao não selecionar conta origem |
| Prioridade      | Alta                                       |
| Rastreabilidade | RN007                                      |
| Pré-Condições   | Usuário autenticado. Conta destino ativa.  |

## Dados de Teste

| Valor  |
| ------ |
| 100,00 |

## Procedimento de Teste

| Passo | Ação                               | Resultado Esperado                          |
| ----- | ---------------------------------- | ------------------------------------------- |
| 1     | Informar valor da transferência    | Valor aceito pelo sistema                   |
| 2     | Não selecionar conta origem        | Campo permanece sem preenchimento           |
| 3     | Selecionar uma conta destino ativa | Conta selecionada                           |
| 4     | Solicitar a transferência          | Sistema exibe mensagem de campo obrigatório |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

---

# CT012 - Exibir erro ao não selecionar conta destino

| Campo           | Descrição                                                     |
| --------------- | ------------------------------------------------------------- |
| ID              | CT012                                                         |
| Título          | Exibir erro ao não selecionar conta destino                   |
| Prioridade      | Alta                                                          |
| Rastreabilidade | RN007                                                         |
| Pré-Condições   | Usuário autenticado. Conta origem ativa com saldo suficiente. |

## Dados de Teste

| Valor  |
| ------ |
| 100,00 |

## Procedimento de Teste

| Passo | Ação                                                   | Resultado Esperado                          |
| ----- | ------------------------------------------------------ | ------------------------------------------- |
| 1     | Informar valor da transferência                        | Valor aceito pelo sistema                   |
| 2     | Selecionar uma conta origem ativa com saldo suficiente | Conta selecionada                           |
| 3     | Não selecionar conta destino                           | Campo permanece sem preenchimento           |
| 4     | Solicitar a transferência                              | Sistema exibe mensagem de campo obrigatório |

## Pós-Condições

* Nenhuma transferência realizada.
* Nenhum saldo alterado.

