
# Resumo de Estruturas de Controle em Python

## Objetivo

Nesta aula, vamos revisar as estruturas de controle de fluxo em Python: **condicionais** (`if`, `else`, `elif`) e **laços de repetição** (`while` e `for`). O objetivo é garantir que os alunos compreendam bem como essas estruturas funcionam e possam aplicá-las em diversos problemas.

## 1. Revisão de Condicionais

As estruturas condicionais são usadas para decidir se um bloco de código será executado ou não, com base em uma condição. A mais comum é a estrutura `if`.

### Sintaxe

```python
if condicao:
    # Bloco de código
elif outra_condicao:
    # Outro bloco de código
else:
    # Bloco de código se nenhuma das condições for verdadeira
```

### Exemplo 1

```python
idade = int(input("Digite sua idade: "))
if idade >= 18:
    print("Você é maior de idade.")
else:
    print("Você é menor de idade.")
```

### Exemplo 2 (usando `elif`)

```python
nota = float(input("Digite a nota do aluno: "))

if nota >= 7:
    print("Aprovado")
elif nota >= 5:
    print("Recuperação")
else:
    print("Reprovado")
```

### Operadores de Comparação e Lógicos

Os operadores de comparação (`==`, `!=`, `>`, `<`, `>=`, `<=`) e operadores lógicos (`and`, `or`, `not`) são essenciais para construir condições mais complexas.

### Exemplo 3 (usando operadores lógicos)

```python
idade = int(input("Digite sua idade: "))
if idade >= 18 and idade <= 65:
    print("Você está em idade produtiva.")
else:
    print("Fora da faixa produtiva.")
```

## 2. Revisão de Laços de Repetição

Os laços de repetição permitem executar um bloco de código várias vezes. Em Python, temos os laços **`while`** e **`for`**.

### 2.1. Laço `while`

O laço `while` executa o bloco de código repetidamente enquanto a condição for verdadeira.

### Sintaxe

```python
while condicao:
    # Bloco de código
```

### Exemplo 4

```python
contador = 0
while contador < 5:
    print(contador)
    contador += 1
```

### Cuidado com Loops Infinitos

É importante garantir que a condição do `while` se tornará falsa em algum momento para evitar loops infinitos.

### Exemplo 5 (loop infinito)

```python
while True:
    print("Este loop nunca vai parar!")
```

### 2.2. Laço `for`

O laço `for` é usado para iterar sobre uma sequência (como uma lista, tupla ou string).

### Sintaxe

```python
for variavel in sequencia:
    # Bloco de código
```

### Exemplo 6

```python
for letra in "Python":
    print(letra)
```

### Função `range()`

Para laços que envolvem uma sequência de números, o `range()` é muito útil.

### Exemplo 7

```python
for i in range(5):
    print(i)
```

## 3. Controle de Fluxo com `break` e `continue`

- **`break`**: Sai do laço imediatamente.
- **`continue`**: Pula para a próxima iteração do laço.

### Exemplo 8 (usando `break`)

```python
for i in range(10):
    if i == 5:
        break
    print(i)
```

### Exemplo 9 (usando `continue`)

```python
for i in range(5):
    if i == 3:
        continue
    print(i)
```

## 4. Exemplos Práticos e Exercícios

### Exemplo 10 (Verificar número primo)

```python
num = int(input("Digite um número: "))
if num > 1:
    for i in range(2, num):
        if num % i == 0:
            print(f"{num} não é primo")
            break
    else:
        print(f"{num} é primo")
else:
    print(f"{num} não é primo")
```

### Exercícios Propostos

1. Faça um algoritmo que leia dois números do usuário e escreva o resultado da multiplicação deles.
2. Faça um algoritmo que leia dois números do usuários e escreva o resultado das operações soma, subtração, multiplicação e divisão deles.
3. Faça um algoritmo que leia 5 notas, calcule e mostre a média aritmética delas.
4. Crie um programa que peça ao usuário um número inteiro e verifique se ele é positivo, neutro ou negativo, usando condicionais.
5. Escreva um algoritmo que leia dois números e verifique qual é o maior deles.
6. Crie um programa escreva todos os números entre 1 e 100.
7. Faça um programa que simule uma contagem regressiva de 10 até 0 usando um laço `for`.
8. Escreva um programa que peça ao usuário um número inteiro e mostre todos os números de 1 até esse número usando um laço `while`.
9. Escreva um algoritmo que receba números do usuário enquanto eles forem positivos. Quando o usuário digitar um número negativo o algoritmo deve finalizar e  imprimir quantos números foram digitados.
10. Escreva um algoritmo que receba números do usuário enquanto eles forem positivos. Quando o usuário digitar um número negativo o algoritmo deve finalizar e  imprimir a média dos números positivos digitados.