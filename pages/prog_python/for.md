[[Página Inicial](../prog_python/home.md)]

---

## Como funciona o Laço For em Python

---

DEFINIÇÃO DE LAÇOS: é uma forma comum de fazer com que o computador automatize tarefas repetitivas

Como funciona o Laço FOR: 
* dentro da construção do for ele irá continuar se:
    * não for parado com um `break`
    * não for parado por um `return`
    * quando acabar os elementos da lista
    * quando chegar no tamanho definido


Lendo uma lista de elementos com For e printar

```python
# Lendo uma lista de nomes, um nome por vez
nomes = ['Gabriel','Lili','Pedro']
for nome in nomes:
    print(nome)

# Lendo uma lista de numeros, um numero por vez
numeros = ['1','2','3','4','5']
for numero in numeros:
    print(numero)
```

Python possui várias ferramentas para listas de números
* Usando a função `range()`
    * com a função **range()** podemos criar elementos numéricos com limites entre dois valores definidos, o inicial e o final-1 
* Usando a função `list()`
    * com a função **list()** podemos criar uma lista dos números criados pelo range

```python
# lendo o range que começa com 1 e vai até 4 no For
for valor in range(1,5):
    print(valor)

# criando uma lista com esses valores
valores = list(range(1,5))
# Lendo cada valor da lista
for valor in valores:
    print(valor)

# EXEMPLO TOTAL: 
# colocando pares dentro de uma lista vazia
pares = [] # inicialização da lista vazia
for valor in range(1,11):
    # colocando o valor par em uma variavel
    par = valor*2
    # adicionando o valor na lista com append()
    pares.append(par)
# podemos imprimir de várias formas
print('print tipo 1: ', pares)
print('print tipo 2: ')
for par in pares:
    print(par)
```
