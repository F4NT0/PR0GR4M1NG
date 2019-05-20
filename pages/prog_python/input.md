[[Página Inicial](../prog_python/home.md)]

---

# como fazer input em python

---

* Utilizamos a função `input()` para poder entrar informações do usuário no seu sistema
* Para utilizarmos o input , chamamos a função dentro de uma variável:
```python
variavel = input('mensagem de input')
```
Podemos utilizar funções auxiliares para tratar os inputs

```python
# COMO FUNCIONA A SAIDA DE UM INPUT
valor = input('Entre com um valor com numero: ')
# a entrada será uma string, portanto nao sera um numero

# entrada: 21
# saida: '21'
```
**Função int()**

A função `int()` serve para poder transformar a string de entrada em um valor inteiro.

```python
valor = input('Entre com um valor inteiro: ')
# entrada = '21'

valor = int(valor) # transforma a String em inteiro

if valor == 21:
    print('Funcionou')
else:
    print('Não Funcionou')
```

**Função float()**

A função `float()` serve que nem a função int() só que desta vez para valores de ponto flutuante.

```python
valor = input('Entre com um valor de ponto flutuante')
# entrada: '21.2'

valor = float(valor)

if valor == 21.2:
    print('Funcionou')
else:
    print('Não funcionou')
```

**Função str()**

A função `str()` serve para transformar um valor inteiro ou float em uma string para poder imprimir no print().

```python
valor = input('Entre um valor Inteiro: ')
valor = int(valor)
print('o valor entrado é: ',str(valor))

valor = input('Entre um valor de Ponto Flutuante: ')
valor = float(valor)
print('o valor entrado é: ',str(valor))

# Podemos usar str() sempre que precisar ter uma saida com numeros

valor1 = input('Entre o primeiro numero inteiro: ')
valor2 = input('Entre o segundo numero inteiro: ')

valor1 = int(valor1)
valor2 = int(valor2)

saida = valor1 + valor2

print('A soma dos valores é: ', str(saida))
```

**Funções upper() e lower()**

Como a saida de um input é uma String, podemos modificar se ela é maiuscula ou minuscula.

```python
# Colocando a Saida em Maiuscula

letra = input('Digite uma letra minuscula: ')
# entrada: n

letra.upper()

print('A letra agora é: ', letra)
# Saida: N


# Colocando a Saida em Minuscula

letra = input('Digite uma letra maiuscula: ')
# entrada: N

letra.lower()

print('A letra agora é: ', letra)
# Saida: n
```

**Adicionando valores em uma lista com input()**

Com o input podemos colocar valores dentro de uma lista, onde o usuario pode tranquilamente colocar valores para dentro

```python
# Criando uma Lista Vazia:

numeros = [] 

# criando um contador para podermos ver a posicao

contador_pos = 0 # listas começam com zero

#Queremos adicionar um while para poder adicionar quantos quisermos
booleano = True # serve para manter o while ativo

# contador para quando quisermos ler a posicao em um for
contador_for = 0

while booleano: #enquanto booleano for true ele continua
    print('Diga um numero para a posicao [',contador_pos,']: ')
    entrada = input('Diga o valor: ')

    # vamos definir que todo valor entrado é inteiro
    entrada = int(entrada)

    # adicionamos o valor na lista com append()

    numeros.append(entrada)

    # perguntamos se queremos fazer mais uma entrada
    restart = input('Deseja adicionar mais um valor? S/N : ')
    # verificamos se a entrada do restart é S/s ou N/n
    if restart.upper() == 'S' or restart.lower() == 's':
        contador_pos += 1
        booleano = True
    elif restart.upper() == 'N' or restart.lower() == 'n':
        booleano = False
    else:
        print('Entrada invalida, finalizando...')
        break
# agora que o while fez seu trabalho, podemos ler todas as posições da lista
for numero in numeros:
    print('Posicao [',contador_for,']: ',numero)
    contador_for += 1
```