# Java Bank Account

Exercício de fixação em Java: cadastro de uma conta bancária com depósito e saque. Baseado em um exercício do curso do Prof. Dr. Nelio Alves.

## O que o programa faz

- Cadastra uma conta com **número**, **titular** e **depósito inicial opcional** (sem depósito, o saldo começa em 0).
- Permite fazer um **depósito** e um **saque**, mostrando os dados da conta depois de cada operação.
- Valida a resposta de `y/n` do depósito inicial: Enter vazio e letras inválidas repetem a pergunta, e maiúsculas são aceitas.

## Regras de negócio

- O número da conta **não pode ser alterado** depois de criada (só tem `get`).
- O saldo **não pode ser alterado livremente**: só muda por depósito (aumenta) e saque (diminui).
- Depósito e saque só aceitam valores **maiores que zero**.
- Cada saque cobra uma **taxa fixa de $ 5.00**.
- A conta **pode ficar com saldo negativo** se o saldo não cobrir o saque e a taxa.

## Conceitos praticados

- Classes e objetos
- Encapsulamento (`private`, `get` e constantes com `final`)
- Sobrecarga de construtores
- Sobrescrita do `toString`
- Validação de entrada com `while` e `Scanner`

## Como rodar

Requisito: JDK instalado (versão recente, porque o `main` está na forma simplificada).

```
javac Bank.java Main.java
java Main
```

## Exemplo de execução

```
Enter account number: 8532
Enter account holder: Alex Green
Is there an initial deposit (y/n)? y
Enter initial deposit value: 500.00
Account data:
Account 8532, Holder: Alex Green, Balance: $ 500.00
Enter a deposit value: 200.00
Updated account data:
Account 8532, Holder: Alex Green, Balance: $ 700.00
Enter a withdraw value: 300.00
Updated account data:
Account 8532, Holder: Alex Green, Balance: $ 395.00
```
