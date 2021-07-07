# Condicionais

## Operadores Lógicos

Em programação, condicionais são esturtura de decisões. O código executo de uma maneiro ou de outra a depender de uma condição, que por sua vez será interpretada como verdadeiro ou falso. Esse tipo de dado é chamado de booleano e possui valor true ou false. Uma condição é uma operação lógica que tem como resultado um valor booleano. Os operadores de comparação em JavaScript são:

| Operador | Nome                      | Exemplo   | Exemplo |
| -------- | ------------------------- | --------- | ------- |
| >        | Maior                     | 2 > 0     | true    |
| >=       | Maior ou igual            | 2 >= 2    | true    |
| <        | Menor                     | 2 < 0     | false   |
| <=       | Menor ou igual            | 2 <= 1    | false   |
| ==       | Igual                     | 1 == '1'  | true    |
| ===      | Igual em valor e tipo     | 1 === '1' | false   |
| !=       | Diferente                 | 1 != 2    | true    |
| !==      | Diferente em valor e tipo | '5' !== 5 | false   |

Os operadores lógicos em JavaScript são:

- && => AND
- || => OR
- ! => NOT

Os operadores de comparação retornam um booleano a depender do resultado da comparação. E os operados lógicos fazem operações sobre valores booleano. O operador && só retorna verdadeiro se as duas condições forem verdadeira. Enquanto para o operador || basta uma das condições ser para o resultado ser verdadeiro. O operador ! inverte o valor lógico, ou seja, verdadeiro vira falso e vice-versa. Confira as tabelas verdades:

| A     | B     | A(AND)B | A(OR)B |
| ----- | ----- | ------- | ------ |
| false | false | false   | false  |
| false | true  | false   | true   |
| true  | false | false   | true   |
| true  | true  | true    | true   |

## If/Else

A estrutura condicional em JavaScript é da seguinte maneira:

```js
let condicao = x > 0

if (condicao) {
  console.log('X é maior do que zero')
} else {
  console.log('X é menor ou igual a que zero')
}
```

A condição deve estar entre parêntesis. Para fim de ilustração o resultado condição foi guardada em uma variável (linha 1), porém é prática escrever diretamente dentro dos parêntesis. Caso a condição seja true o código dentro do if é executado, senão o do else é executado.

Ainda é possível fazer estruturas que verifiquem mais de uma condição usando o else if:

```js
if (x > 0) {
  console.log('X é positivo')
} else if (x == 0) {
  console.log('X é zero')
} else {
  console.log('X é negativo')
}
```

Caso a condição do if for false, é verificado a condição do else if, se esta por sua vez for falsa é verificado a condição do próximo else if, se houver, senão é executado o else, também se houver.

## Operador Ternário

Para atribuição condicional de valor o JavaScript possui um operador que permite fazer uma if else inline, isto é, em uma única linha. Operador tenário é representado por ?:

```js
let paridade = x % 2 === 0 ? 'par' : 'impar'
```

Primeiro colocamos a condição a ser verificada, no caso x % 2 === 0 onde % é o operador que retorna o resto da divisão. Ou seja, a condição é se o resto da divisão é igual a zero. Se sim, guardamos a string 'par' na variável, se não, 'impar'. Note que os valores são separados por : (dois pontos).

## Switch

O Switch é uma estrutura condicional que recebe um valor e executa um código quebrando os casos que a variável pode receber. Por exemplo:

```js
let hoje = new Date().getDay()
let dia

switch (hoje) {
  case 0:
    dia = 'Domingo'
    break
  case 1:
    dia = 'Segunda'
    break
  case 2:
    dia = 'Terça'
    break
  case 3:
    dia = 'Quarta'
    break
  case 4:
    dia = 'Quinta'
    break
  case 5:
    dia = 'Sexta'
    break
  case 6:
    dia = 'Sábado'
}
```

O comando new Date().getDay() retorna o dia atual como um inteiro, começando em 0 no domingo e indo até 6 para o sábado. O switch recebe a variável e quebra casos. Caso seja 1, por exemplo, definimos a variável dia como "Segunda". O break representa o fim do case. Caso seja omitido o computador executará o caso seguinte. Por isso é dispensável no último caso. Ainda é possível definir um padrão caso nenhum dos casos exista usando o default.

```js
let sinal = 'azul'
switch (sinal) {
  case 'verde':
    console.log('pode passar')
    break
  case 'amarelo':
    console.log('prestes a fechar, cuidado...')
    break
  case 'vermelho':
    console.log('fechado, não passe')
    break
  default:
    console.log('esse não é um valor válido')
    break
}
```

## Truthy e Falsy

Além do true e do false, o JavaScript aceita outras informações que não são booleanos e os interpreta como se fosse true ou false. Esses casos chamamos de truthy e falsy. Por exemplo, o JavaScript interpreta os seguintes valores como falso:

- O
- "ou"
- null
- undefined
- NaN

Todos os demais são interpretados como verdadeiro. Alguns exemplos de truthy:

- []
- {}
- function(){}

Uma utilidade dessa característica é verificar se uma variável está definida antes de usá-la. Assim evitando erro.
