# 📄 QA - Análise da Funcionalidade Realizar Transferência

# 📌 Funcionalidade

Realizar Transferência

---

# 🎯 Objetivo

Validar o comportamento da funcionalidade de transferência bancária, garantindo que o sistema permita transferências válidas e trate corretamente cenários inválidos conforme as regras de negócio definidas.

---

# 📥 Entradas Identificadas

* Conta origem
* Conta destino
* Valor da transferência
* Token de autenticação

---

# ✔️ Validações Identificadas

* Valor mínimo permitido para transferência
* Obrigatoriedade de token para transferências acima de R$5.000,00
* Validação de token
* Conta origem ativa
* Conta destino ativa
* Saldo suficiente na conta origem
* Campos obrigatórios

---

# 📌 Regras de Negócio Cobertas

## 💸 Regras para realizar transferência

* O valor mínimo para transferências é de R$10,00.
* Transferências acima de R$5.000,00 requerem token de autenticação.
* Token esperado: `123456`
* As contas de origem e destino devem estar ativas.
* A conta origem deve possuir saldo suficiente para realizar a transferência.

---

# 🟢 Cenários Positivos Identificados

* Realizar transferência com valor válido
* Realizar transferência utilizando valor mínimo permitido
* Realizar transferência acima de R$5.000,00 com token válido
* Realizar transferência entre contas ativas
* Realizar transferência com saldo suficiente

---

# 🔴 Cenários Negativos Identificados

* Informar valor abaixo do mínimo permitido
* Informar valor inválido
* Não informar token em transferências acima de R$5.000,00
* Informar token inválido
* Realizar transferência com conta origem inativa
* Realizar transferência com conta destino inativa
* Realizar transferência com saldo insuficiente
* Não informar valor
* Não selecionar conta origem
* Não selecionar conta destino

---

# 🧠 Técnicas de Design de Teste Aplicadas

# 📌 Análise de Valor Limite (AVL)

## Regra: Valor mínimo da transferência = R$10,00

| Tipo            | Valor |
| --------------- | ----- |
| Antes do limite | 9,99  |
| No limite       | 10,00 |
| Após o limite   | 10,01 |

---

## Regra: Transferências acima de R$5.000,00 exigem token

| Tipo            | Valor    |
| --------------- | -------- |
| Antes do limite | 4.999,99 |
| No limite       | 5.000,00 |
| Após o limite   | 5.000,01 |

---

# 📌 Particionamento de Equivalência (PE)

## 💸 Valor da Transferência

### Classes válidas

* Valor igual a R$10,00
* Valor acima de R$10,00
* Valor acima de R$5.000,00 com token válido

### Classes inválidas

* Valor abaixo de R$10,00
* Valor negativo
* Valor vazio
* Valor textual

---

## 🔐 Token

### Classe válida

* 123456

### Classes inválidas

* Não informado
* Token inválido

---

## 🏦 Conta Origem

### Classe válida

* Conta ativa com saldo suficiente

### Classes inválidas

* Conta inativa
* Conta sem saldo suficiente

---

## 🏦 Conta Destino

### Classe válida

* Conta ativa

### Classes inválidas

* Conta inativa

---

# 📋 Tabela de Decisão

| Caso de Teste | Valor         | Token         | Conta Origem | Saldo        | Conta Destino | Resultado Esperado                   |
| ------------- | ------------- | ------------- | ------------ | ------------ | ------------- | ------------------------------------ |
| CT01          | < 10          | Não informado | Ativa        | Suficiente   | Ativa         | Exibir erro de valor mínimo          |
| CT02          | = 10          | Não informado | Ativa        | Suficiente   | Ativa         | Transferência realizada com sucesso  |
| CT03          | > 10 e < 5000 | Não informado | Ativa        | Suficiente   | Ativa         | Transferência realizada com sucesso  |
| CT04          | = 5000        | Não informado | Ativa        | Suficiente   | Ativa         | Transferência realizada com sucesso  |
| CT05          | > 5000        | Não informado | Ativa        | Suficiente   | Ativa         | Exibir erro de token obrigatório     |
| CT06          | > 5000        | Inválido      | Ativa        | Suficiente   | Ativa         | Exibir erro de token inválido        |
| CT07          | > 5000        | Válido        | Ativa        | Suficiente   | Ativa         | Transferência realizada com sucesso  |
| CT08          | Valor válido  | Não informado | Inativa      | Suficiente   | Ativa         | Exibir erro de conta origem inativa  |
| CT09          | Valor válido  | Não informado | Ativa        | Insuficiente | Ativa         | Exibir erro de saldo insuficiente    |
| CT10          | Valor válido  | Não informado | Ativa        | Suficiente   | Inativa       | Exibir erro de conta destino inativa |
| CT11          | Valor vazio   | Não informado | Ativa        | Suficiente   | Ativa         | Exibir mensagem de campo obrigatório |
| CT12          | Valor textual | Não informado | Ativa        | Suficiente   | Ativa         | Exibir erro de valor inválido        |

---

# 🧪 Estratégia de Teste Exploratória

# 🎯 Charter

Explorar o comportamento da funcionalidade de transferência bancária considerando diferentes combinações de valores, autenticação, saldo e status das contas.

---

# 🔍 Heurísticas Utilizadas

* Limites mínimos e máximos
* Valores decimais
* Campos obrigatórios
* Token inválido
* Atualização de saldo
* Consistência entre contas
* Mensagens de erro
* Fluxo de autenticação
* Comportamento após transferência

---

# 📝 Observações

* As regras relacionadas à geração e expiração de token pertencem à camada de API/backend.
* O escopo atual contempla testes funcionais WEB da funcionalidade de transferência.
* Os cenários BDD foram estruturados com foco comportamental, utilizando parametrização através de Esquema do Cenário e tabelas de Exemplos.
