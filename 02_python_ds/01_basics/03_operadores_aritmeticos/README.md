# Operadores aritméticos

```python
# Podemos fazer operações aritméticas simples
a = 2 + 3  # Soma
b = 2 - 3  # Subtração
c = 2 * 3  # Multiplicação
d = 2 / 3  # Divisão
e = 2 // 3 # Divisão inteira
f = 2 ** 3 # Potência
g = 2 % 3  # Resto de divisão

print (a, b, c, d, e, f, g)

# Podemos fazer operações dentro do print

print (a+1, b+1)

#Podemos fazer operações com variáveis não inteiras
nome = input('Digite seu primeiro nome:')
nome = nome + ' Schmitt'
print(nome)
```

## Operadores relacionais

Observe o código abaixo:

```python
comparacao1 = 5 > 3
print(comparacao1)
comparacao2 = 5 < 3
print(comparacao2)
```

Ao ser executado, a saída que teremos na tela será:

```python
True
False
```

Isso ocorre porque 5 é maior que 3. Portanto, comparacao1 recebeu uma expressão cujo valor lógico é verdadeiro, portanto seu resultado foi True, e o oposto ocorreu para comparacao2.

O Python possui 6 operadores relacionais:

- Maior que: >
- Maior ou igual: >=
- Menor que: <
- Menor ou igual: <=
- Igual: ==
- Diferente: !=

Note que o operador para comparar se 2 valores são iguais é ==, e não =. Isso ocorre porque o operador = é o nosso operador de atribuição: ele diz que a variável à sua esquerda deve receber o valor da expressão à direita. O operador == irá testar se o valor à sua esquerda é igual ao valor à sua direita e irá responder True ou False, como todos os outros operadores de comparação.

## Operadores lógicos

Em alguns casos também precisamos testar se duas ou mais condições são verdadeiras. Para isso utilizaremos as conjunções lógicas:

- and: verdadeiro se condição 1 for verdadeira e condição 2 for verdadeira
- or: verdadeiro se condição 1 for verdadeira ou condição 2 for verdadeira

No exemplo abaixo, o resultado é verdadeiro para comparacao1 e falso para comparacao2.

```python
comparacao1 = 5 > 3 and 6 > 3
comparacao2 = 5 < 3 and 6 > 3
```

Já no exemplo seguinte, tanto comparacao1 quanto comparacao2 retornam o valor verdadeiro.

```python
comparacao1 = 5 > 3 or 6 > 3
comparacao2 = 5 < 3 or 6 > 3
```

Também é possível negar uma expressão lógica usando o not. Em outras palavras, se comparacao1 = 5 > 3 é verdadeira, comparacao1 = not(5 > 3) será falsa, e vice-versa.