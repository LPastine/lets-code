# Estruturas de Repetição

## While

O while é bastante parecido com um 'if': ele possui uma expressão, e é executado caso ela seja verdadeira. Mas o if é executado apenas uma vez, e depois o código segue adiante.

O while não: ao final de sua execução, ele torna a testar a expressão, e caso ela seja verdadeira, ele repete sua execução.

```python
horario = int(input('Qual horario é agora? '))

# Testando a condição uma única vez com o if:
if 0 < horario < 6:
    print('Você está no horario da madrugada')
else:
    print('Você nao está no horario da madrugada')

# Testando a condição em loop com o while:
while 0 < horario < 6:
    print('Você está no horario da madrugada')
    horario = horario + 1
else:
    print('Você nao está no horario da madrugada')

# O while permite continuar decrementando o número de pipocas até chegar em 0:
num_pipocas = int(input('Digite o numero de pipocas: '))

while num_pipocas > 0:
    print('O numero de pipocas é: ', num_pipocas)
    num_pipocas = num_pipocas - 1
```

## Validação de entrada

Uma utilidade interessante do while é obrigar o usuário a digitar apenas entradas válidas.

```python
# o exemplo abaixo não aceita um salário menor do que o mínimo atual:
salario = float(input('Digite seu salario: '))
while salario < 998.0:
    salario = float(input('Entre com um salario MAIOR DO QUE 998.0: '))
else:
    print('O salario que você entrou foi: ', salario)
# o exemplo abaixo só sai do loop quando o usuário digitar "OK":
resposta = input('Digite OK: ')
while resposta != 'OK':
    resposta = input('Não foi isso que eu pedi, digite OK: ')
```

## Contador

Todo tipo de código que deve se repetir várias vezes pode ser feito com o while, como somar vários valores, gerar uma sequência etc. Nestes casos, é normal utilizar um contador:

```python
# Declaramos um contador como 0:
contador = 0
# Definimos o número de repetições:
numero = int(input('Digite um numero: '))
# Rodamos o while até o contador se igualar ao número de repetições:
while contador < numero:
    print(contador)
    contador = contador + 1
```

## Break

Um jeito de forçar um loop a ser interrompido é utilizando o comando 'break'. O loop abaixo em tese seria infinito, mas se a condição do if for verificada, o break é executado e conseguimos escapar do loop:

```python
while True:
    resposta = input('Digite OK: ')
    if resposta == 'OK':
        break
```