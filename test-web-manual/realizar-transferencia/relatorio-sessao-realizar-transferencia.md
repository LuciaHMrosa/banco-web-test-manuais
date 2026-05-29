# 📄 Relatório de Sessão Exploratória — Transferências

Inspirado no artigo de John Bach sobre Session-Based Test Management (2001)

| Data e Hora do Início | Nome do Testador | Módulo         |
| --------------------- | ---------------- | -------------- |
| 28/05/2026            | Lúcia de Melo    | Transferências |

---

# 🎯 Test Charter

Explorar o comportamento da funcionalidade de transferência bancária, avaliando atualização de saldo, validação de valores monetários, tratamento de entradas inválidas e consistência das regras de negócio durante a realização de transferências.

---

# ⏱️ Tamanho da Sessão

30 minutos

---

# 🔍 Heurísticas Utilizadas

* Limite mínimo e máximo de valores
* Atualização de informações em tela
* Consistência de saldo
* Validação de campos numéricos
* Quantidade de caracteres
* Validação de casas decimais
* Fluxos inválidos
* Regras de negócio
* Transferência entre contas

---

# 📌 Cobertura Explorada

* Atualização de saldo
* Campo valor da transferência
* Campo token
* Validação de contas
* Precisão decimal
* Fluxo de transferência
* Consistência visual da interface

---

# 📝 Notas*

* (I) Após realizar uma transferência, os valores de saldo das contas origem e destino não são atualizados imediatamente na interface.

* (I) Os saldos somente são atualizados após atualização manual da página.

* (R) O campo de valor da transferência permite inserção de números extremamente longos, mesmo quando a transferência não é concluída.

* (R) O campo de token permite inserção de sequências extremamente longas de caracteres sem limitação aparente.

* (I) O sistema permite informar múltiplas casas decimais no valor da transferência.

* (I) Durante a execução da transferência, o sistema considera apenas duas casas decimais após a vírgula.

* (R) O sistema permite realizar transferência utilizando a mesma conta como origem e destino.

* (R) Não foi apresentada validação impedindo transferências para a própria conta.

(*) Podem ser (I)nformações ou (R)iscos.

---

# 🐞 Defeitos Identificados

1. Os saldos das contas origem e destino não são atualizados automaticamente após a realização da transferência.

2. O campo de valor da transferência não apresenta limite máximo aparente de caracteres ou valor monetário.

3. O campo de token permite inserção excessiva de caracteres sem validação de tamanho.

4. O sistema permite realização de transferência utilizando a mesma conta como origem e destino.

---

# ❓ Perguntas

1. O saldo das contas deveria ser atualizado automaticamente após a transferência?

2. Existe limite máximo esperado para o valor da transferência?

3. Existe limite máximo esperado para o campo token?

4. O sistema deve limitar a quantidade de casas decimais permitidas no campo valor?

5. Transferências entre a mesma conta deveriam ser bloqueadas?

6. Existe regra de negócio específica para transferência entre mesma origem e destino?
