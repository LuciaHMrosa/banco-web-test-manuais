# 📑 Casos de Teste — ISO/IEC/IEEE 29119-3

# CT001 - Exibir lista de transferências realizadas

| Campo           | Descrição                                                           |
| --------------- | ------------------------------------------------------------------- |
| ID              | CT001                                                               |
| Título          | Exibir lista de transferências realizadas                           |
| Prioridade      | Alta                                                                |
| Rastreabilidade | RN001                                                               |
| Pré-Condições   | Usuário autenticado. Existem transferências cadastradas no sistema. |

## Procedimento de Teste

| Passo | Ação                                   | Resultado Esperado                            |
| ----- | -------------------------------------- | --------------------------------------------- |
| 1     | Acessar a página de transferências     | Página exibida com sucesso                    |
| 2     | Consultar a listagem de transferências | O sistema exibe as transferências cadastradas |

## Pós-Condições

* Nenhuma alteração nos dados.

---

# CT002 - Navegar para próxima página da listagem

| Campo           | Descrição                                                                   |
| --------------- | --------------------------------------------------------------------------- |
| ID              | CT002                                                                       |
| Título          | Navegar para próxima página da listagem                                     |
| Prioridade      | Média                                                                       |
| Rastreabilidade | RN002, RN003                                                                |
| Pré-Condições   | Usuário autenticado. Existem registros suficientes para mais de uma página. |

## Procedimento de Teste

| Passo | Ação                                 | Resultado Esperado                             |
| ----- | ------------------------------------ | ---------------------------------------------- |
| 1     | Acessar a página de transferências   | Página exibida com sucesso                     |
| 2     | Acionar o controle de próxima página | O sistema exibe os registros da próxima página |

## Pós-Condições

* Usuário permanece na listagem.

---

# CT003 - Navegar para página anterior da listagem

| Campo           | Descrição                                                      |
| --------------- | -------------------------------------------------------------- |
| ID              | CT003                                                          |
| Título          | Navegar para página anterior da listagem                       |
| Prioridade      | Média                                                          |
| Rastreabilidade | RN002, RN003                                                   |
| Pré-Condições   | Usuário autenticado. Estar em uma página posterior à primeira. |

## Procedimento de Teste

| Passo | Ação                                     | Resultado Esperado                              |
| ----- | ---------------------------------------- | ----------------------------------------------- |
| 1     | Acessar uma página posterior da listagem | Página exibida                                  |
| 2     | Acionar o controle de página anterior    | O sistema exibe os registros da página anterior |

## Pós-Condições

* Usuário permanece na listagem.

---

# CT004 - Validar limite de itens por página

| Campo           | Descrição                                                                               |
| --------------- | --------------------------------------------------------------------------------------- |
| ID              | CT004                                                                                   |
| Título          | Validar limite de itens por página                                                      |
| Prioridade      | Alta                                                                                    |
| Rastreabilidade | RN004                                                                                   |
| Pré-Condições   | Usuário autenticado. Existirem registros suficientes para preencher mais de uma página. |

## Procedimento de Teste

| Passo | Ação                                            | Resultado Esperado                                             |
| ----- | ----------------------------------------------- | -------------------------------------------------------------- |
| 1     | Acessar a página de transferências              | Página exibida com sucesso                                     |
| 2     | Contabilizar a quantidade de registros exibidos | Quantidade apresentada respeita o limite definido pelo sistema |
| 3     | Navegar para outras páginas                     | O limite continua sendo respeitado                             |

## Pós-Condições

* Nenhuma alteração nos dados.

---

# CT005 - Exibir mensagem quando não existirem transferências

| Campo           | Descrição                                                      |
| --------------- | -------------------------------------------------------------- |
| ID              | CT005                                                          |
| Título          | Exibir mensagem quando não existirem transferências            |
| Prioridade      | Alta                                                           |
| Rastreabilidade | RN005                                                          |
| Pré-Condições   | Usuário autenticado. Não existirem transferências cadastradas. |

## Procedimento de Teste

| Passo | Ação                               | Resultado Esperado                                                             |
| ----- | ---------------------------------- | ------------------------------------------------------------------------------ |
| 1     | Acessar a página de transferências | Página exibida com sucesso                                                     |
| 2     | Consultar a listagem               | O sistema exibe mensagem informando que não existem transferências cadastradas |

## Pós-Condições

* Nenhuma alteração nos dados.

---

# CT006 - Validar consistência após atualização da página

| Campo           | Descrição                                                  |
| --------------- | ---------------------------------------------------------- |
| ID              | CT006                                                      |
| Título          | Validar consistência após atualização da página            |
| Prioridade      | Média                                                      |
| Rastreabilidade | RN006                                                      |
| Pré-Condições   | Usuário autenticado. Existirem transferências cadastradas. |

## Procedimento de Teste

| Passo | Ação                               | Resultado Esperado                                                |
| ----- | ---------------------------------- | ----------------------------------------------------------------- |
| 1     | Acessar a página de transferências | Página exibida com sucesso                                        |
| 2     | Observar os registros apresentados | Registros exibidos corretamente                                   |
| 3     | Atualizar a página do navegador    | Página recarregada com sucesso                                    |
| 4     | Verificar novamente os registros   | As informações permanecem consistentes e sem alterações indevidas |

## Pós-Condições

* Nenhuma alteração nos dados.
