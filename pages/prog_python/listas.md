[[Página Inicial](../prog_python/home.md)]

---

# TRABALHANDO COM LISTAS

---

* As listas permitem armazenar conjuntos de informações em um só lugar
* As listas possuem uma organização em espaços de **posição de 0 á quanto for necessário**
* Podemos colocar **qualquer tipo de informação** dentro de uma lista
* é importante colocar o **nome da lista no plural** para facilitar o trabalho com for

### Criando uma Lista

* Podemos criar 3 tipos de listas:
  * **Lista Vazia**: é uma lista que foi criada sem nenhum elemento dentro
  * **Lista de tipo Único**: é uma lista que possui somente um tipo de dado(inteiro ou float ou String)
  * **Lista de vários tipos**: é uma lista que armazena valores de vários tipos de dados diferentes 

* Exemplo:

```python
# CRIANDO UMA LISTA VAZIA
valores = []

# CRIANDO UMA LISTA DE TIPO UNICO
valores = [1,2,3,4,5,6]

# CRIANDO UMA LISTA DE VÁRIOS TIPOS
valores = ['Nome',12,3.5]

```

### Percorrendo uma Lista

* Podemos percorrer uma lista de 2 formas:
  * **Chamando uma posição especifica da lista**: toda lista começa com a `posição zero`, e se queremos pegar um elemento de uma posição especifica da lista temos que chamar a posição entre colchetes uma por uma 
  * **Criando um Laço For para imprimir o valor das posições**: desta forma criamos um laço que definimos um `range()` a uma variavel que ira andar pela lista ou iremos criar uma variavel que chama elemento por elemento, esta variavel é o nome no singular da lista no plural para facilitar o entendimento

* Exemplo:

```python
# PERCORRENDO UMA LISTA POSICAO POR POSICAO E IMPRIMINDO
valores = [1,2,3,4]

print(valores[0]) # SAIDA: 1
print(valores[1]) # SAIDA: 2
print(valores[2]) # SAIDA: 3

# PERCORRENDO UMA LISTA E SALVANDO O VALOR DA POSICAO

valores = [1,2,3,4]

primeira_posicao = valores[0]
print(primeira_posicao) # SAIDA: 1



# USANDO UM LAÇO FOR PARA PERCORRER A LISTA COM UMA VARIAVEL CRIADA 
valores = [1,2,3,4]

for valor in valores:
    print(valor)


# USANDO A FUNÇÃO RANGE() PARA PODER ANDAR POR TODA A LISTA

valores = [1,2,3,4]

for i in range(len(valores)):
    print(valores[i])

```

### Adicionando valores na Lista

* Em uma lista tem algumas formas de adicionar novos valores, sendo 4 formas básicas de se fazer:
  * 1) **Adicionando valores com a função append(valor)**: essa função serve para adicionar o novo elemento no final da lista
  * 2) **Adicionando valores com a função insert(posicao,valor)**: essa função serve para adicionar o novo elemento na lista na posição que desejamos
  * 3) **Adicionando valores com a função input()**: é uma forma de adicionar elementos deixando que o usuário defina quais ele deseja
  * 4) **Adicionando valores com uma função criada**: podemos criar uma funcao que ira adicionar elementos

* Exemplos

```python
# MÉTODO 1: ADICIONANDO VALORES COM APPEND(VALOR)

valores = [] # criacao de uma lista vazia

valores.append(1)
valores.append(2)
valores.append(3)

print(valores) # SAIDA: [1,2,3]

# MÉTODO 2: ADICIONANDO VALORES COM INSERT(POSICAO,VALOR)

valores = [1,3,4,5] # lista já com valores

# queremos colocar o valor 2 depois do valor 1 na lista
# dizemos que queremos colocar o valor 2 na posicao 1 da lista

valores.insert(1,2)

print(valores) # SAIDA: [1,2,3,4,5]

# MÉTODO 3: ADICIONANDO VALORES COM INPUT()
# o usuario vai adicionar valores
numeros = []

numero = input('Adicione um numero na lista: ') # exemplo: usuario coloca 1

numeros.append(numero) # adicionando no fim da lista
numeros.insert(0,numero) # adicionando na lista na primeira posicao 

# MÉTODO 4: CRIANDO UMA FUNÇÃO PARA ADICIONAR VALORES

# criamos uma função para adicionar no final da lista

def adiciona_final(valor,lista):
    lista.append(valor)
    print('Adicionado um valor!!')

# criamos uma função para adicionar um valor em uma posição especifica

def adicina_posicao(lista,valor,posicao):
    lista.insert(int(posicao),valor)
    print('Adicionado um valor!')


# Chamando as funções
numeros = []

adiciona_final(1,numeros) # saida: Adicionado um valor!
adiciona_posicao(numeros,2,1) # saida: Adicionado um valor!

print(numeros) # saida: [1,2]
```


### Removendo valores da Lista

* Iremos utilizar uma função chamada `pop()`, que passando como parametro uma posição ele irá retirar o elemento da posição especifica.
  * Se não passar uma posicao especifica, ele irá remover o ultimo elemento da lista

* Podemos retirar elementos usando a função `remove()` que dizemos exatamente qual elemento retirar e ele procura em cada posição onde este elemento se encontra
  
```python

numeros = [1,2,3,4,5]

# Retirando com pop()
elemento_retirado = numeros.pop(0)
print(elemento_retirado) # Saida: 1
print(numeros) # saida: [2,3,4,5]

elemento_retirado_2 = numeros.pop()
print(elemeto_retirado_2) # Saida: 5
print(numeros) # saida: [2,3,4]

# Retirando com remove()
numeros.remove(2)

print(numeros) # saida: [3,4]
```

### Descobrindo o tamanho de uma Lista

* É bem simples descobrir o tamanho de uma lista, utilizamos o método `len()` para poder descobrir o tamanho da lista(numero de elementos internos)

```python
numeros = [1,2,3,4,5,6]
tamanho = len(numeros)
print(tamanho) # Saida: 6
```

### Ordenando uma Lista 

* Se quisermos ordenar em ordem alfabetica ou numerica, podemos usar a função `sort()` para poder arrumar
* Se quisermos ordenar os elementos de ordem inversa, podemos usar a função `reverse()`

```python
# Testando o método sort()
letras = ['b','a','d','c']
letras.sort()
print(letras) # Saida: [a,b,c,d]

# Testando o método reverse()
letras = ['a','b','c','d']
letras.reverse()
print(letras) # Saida: [d,c,b,a]
```


# Trabalhando com partes de uma lista

* Com python podemos dividir uma lista de forma muito simples
* Podemos criar novas listas facilmente usando um limitador para dizer até onde vai a lista desejada
* construção de um limitador: `lista[posicao inicial: posicao final]`
  * se quiser pegar tudo do inicio e ir ate uma posicao especifica: `lista[:pf]`
  * se quiser pegar de uma posicao e ir ate o fim: `lista[2:]`
  * Se quisermos pegar a lista toda de uma vez , definimos vazio de todos os lados: `lista[:]`

```python
numeros = [1,2,3,4,5,6]

print(numeros[1:3]) # Saida: [2,3,4]
print(numeros[:4])  # Saida: [1,2,3,4,5]
print(numeros[1:])  # Saida: [2,3,4,5,6]

nova_lista = numeros[1:3]
print(nova_lista) # Saida: [2,3,4]

copia_lista = numeros[:]
print(copia_lista) 
```