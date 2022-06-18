## Finance API - Financeira

---

### Requisitos:

- ✅ Deve ser possível criar uma conta
- ✅ Deve ser possível buscar o extrato bancário do cliente
- ✅ Deve ser possível realizar um depósito
- ❌ Deve ser possível realizar um saque
- ❌ Deve ser possível buscar o extrato bancário do cliente por data
- ❌ Deve ser possível atualizar dados da conta do cliente
- ❌ Deve ser possível deletar uma conta
- ❌ Cada conta de ve possuir os seguintes atributos:

```js
    {
        cpf: string,
        name: string,
        id: uuid,
        statement: [{
            amount: number,
            description: string,
            created_at: date,
            type: string //credit || debit
        }] //extrato da conta
    }
```

---

### Regras de negócio

- ✅ Não deve ser possível cadastrar uma conta com CPF já existente
- ✅ Não deve ser possível buscar extrato em um conta não existente
- ✅ Não deve ser possível fazer depósito em uma conta não existente
- ❌ Não deve ser possível fazer saque em uma conta não existente
- ❌ Não deve ser possível excluir uma conta não existente
- ❌ Não deve ser possível fazer saque quando o saldo for
