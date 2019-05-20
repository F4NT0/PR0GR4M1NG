[[Página Inicial](../prog_python/home.md)]

---

# Utilizando Dicionários em Python

---

* `Dicionários` são Estruturas de Dados usados para `mapear chaves arbitrárias com valores`
* as `Chaves Arbitrárias` só podem ser elementos que são **Imutáveis**(que não mudam)

**Como construir um Dicionário**

* São utilizados `{}` para se dizer que estamos indexando um dicionário

```python
dicionario = {chave_arbitraria : valor}
```

* podemos colocar quantos valores queremos dentro de um dicionario
* existem duas formas de organizar um dicionário

```python
dicionario = {
    1 : 'Gabriel',
    2 : 'Pedro',
    3 : 'Larissa',
    4 : 'Vinicius'  
}
```
```python
dicionario = {1:'Gabriel',2:'Pedro',3:'Larissa',4:'Vinicius'}
```

**Como pegar valores de um Dicionário**

* Utilizamos a forma de chamar como em uma lista para poder pegar elementos
* `De vez de posição, chamamos a chave_arbitraria`

```python
dicionario = {chave_arbitraria : valor}
print(dicionario[chave_arbitraria])
```
* Exemplo
```python
dicionario = {
    1 : 'Gabriel'
    2 : 'Pedro'
    3 : 'Larissa'
}
print(dicionario[1]) # Saida: Gabriel
```

**Alterando e Criando valores no Dicionário**

* Podemos criar e alterar valores em um dicionário chamando a chave arbitrária

```python
dicionario = {
    1 : 1,
    2 : 2,
    3 : 3,
    4 : 4
}
print(dicionario) # saida: {1: 1,2: 2,3: 3,4: 4}

# Alterando valores
dicionario[1] = 0
dicionario[2] = 1
dicionario[3] = 2
dicionario[4] = 3
print(dicionario) # saida: {1: 0,2: 1,3: 2,4: 3}

# Adicionando valores
dicionario[5] = 4
dicionario[6] = 5
dicionario[7] = 6
dicionario[8] = 7
print(dicionario) # saida: {1: 0,2: 1,3: 2,4: 3,5: 4,6: 5,7: 6,8: 7}
```

**Verificação de chave no dicionário**

* Podemos descobrir se existe uma chave arbitrária em um Dicionário
* usamos `in` e `not in` para verificar se existe a chave no dicionario

```python
dicionario = {
    1 : 1,
    2 : 2,
    3 : 3,
    4 : 4
}
print(1 in dicionario) # True
print(6 in dicionario) # False
print(1 not in dicionario) # False
print(6 not in dicionario) # True
```

**Funções do Dicionário**

* Temos a função `get()` para usar em dicionarios
* Passamos por parâmetro o valor da chave arbitrária
* Se não existir a chave, o valor retornado é `None`

```python
dicionario = {
    1 : 'Gabriel',
    2 : 'Pedro',
    3 : 'Larissa'
}

print(dicionario.get(1)) # Gabriel
print(dicionario.get(4)) # None
print(dicionario.get(4, 'Vinicius')) # Vinicius
print(dicionario) # {1: Gabriel, 2: Pedro, 3: Larissa, 4: Vinicius}
```


