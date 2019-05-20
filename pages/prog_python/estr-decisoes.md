[[Página Inicial](../prog_python/home.md)]

---

# Estrutura de Decisões

---

if/else é uma estrutura de decisão que permite verificar qualquer condição, onde ele ele faz uma avaliação booleana (<code style="color : lightgreen">True</code> ou false) chamada de **teste condicional**

Se o resultado do teste condicional for **<code style="color : lightgreen">True</code>**, ele entra na instrução do `if`

Se o resultado do teste condicional for **False**, ele entra na instrução do `else`

Os **testes condicionais** que se usa em Python são:
* **Igualdade**
  * o simbolo para igualdade é `==`
  * o teste retorna <code style="color : lightgreen">True</code> se as duas informações forem iguais
* **Diferença**
  * o simbolo para diferenca é `!=`
  * o teste retorna <code style="color : lightgreen">True</code> se as duas informações forem diferentes
* **Comparações**
  * existem 5 tipos de comparações
    * IGUAL: funciona como a igualdade, o simbolo é `==`
    * MENOR: verifica se o valor é menor que o outro, simbolo: `<`
    * MAIOR: verifica se o valor é maior que o outro, simbolo: `>`
    * MENOR OU IGUAL: simbolo: `<=`
    * MAIOR OU IGUAL: simbolo: `>=`

Podemos testar várias condições ao mesmo tempo utiizamos as seguintes palavras reservadas:
    
* Multiplos testes com `and`: **and** testa para que todos os testes das variaveis ou valores deem verdadeiro ou falso como na tabela lógica
* Multiplos testes com `or`: **or** testa para que pelo menos uma das variaveis ou valores sejam <code style="color : lightgreen">True</code> para poder ser True
* Podemos usar o `not`: **not** recebe somente uma variavel e troca o valor booleano dela pelo seu oposto
### EXEMPLO DE TESTES CONDICIONAIS

```python

# IGUALDADE

3 == 3 # True
4 == 3 # False

# DIFERENÇA

3 != 4 # True
4 != 4 # False

# COMPARAÇÕES

a = 3
b = 4

a < b # True
a > b # False

a <= b # True
a >= b # False

# TESTE DE VÁRIAS CONDIÇÕES
a = 1
b = 2
c = 1
d = 3

a >= c # True
b == d # False
d > a  # True
a > b  # False


# TESTE DO AND

b == d and a > b  # False and False = False
a >= c and b == d # True  and False = False
a > b and d > a   # False and True  = False
a >= c and d > a  # True  and True  = True

# TESTE DO OR

b == d or a > b   # False or False = False
a >= c or b == d  # True  or False = True
a > b  or d > a   # False or True  = True
a >= c or d > a   # True  or True  = True   
```
### Verificando elementos em uma lista

Podemos verificar elementos de uma lista no if/else tambem

**Verificando se está na lista:**
* usamos a palavra reservada `in` para ver se existe o elemento
```python
# PRIMEIRA FORMA
lista = ['Gabriel','Pedro','Igor']

'Gabriel' in lista  # True
'Fulano'  in lista  # False

lista2 = [1,2,3,4]

1 in lista2  # True
6 in lista2  # False

# SEGUNDA FORMA
lista = ['Gabriel','Pedro','Igor']
variavel_1 = 'Gabriel'
variavel_2 = 'Fulano'

variavel_1 in lista # True
variavel_2 in lista # False

lista2 = [1,2,3,4]
variavel_1 = 1
variavel_2 = 6

variavel_1 in lista2 # True
variavel_2 in lista2 # False
```
**Verificando se não está na lista:**
* usamos a palavra reservada `not in` para ver se não existe o elemento
```python
# PRIMEIRA FORMA
lista = ['Gabriel','Pedro','Igor']

'Gabriel' not in lista  # False
'Fulano'  not in lista  # True

lista2 = [1,2,3,4]

1 not in lista2  # False
6 not in lista2  # True

# SEGUNDA FORMA
lista = ['Gabriel','Pedro','Igor']
variavel_1 = 'Gabriel'
variavel_2 = 'Fulano'

variavel_1 not in lista # False
variavel_2 not in lista # True

lista2 = [1,2,3,4]
variavel_1 = 1
variavel_2 = 6

variavel_1 not in lista2 # False
variavel_2 not in lista2 # True

```

### Usando variaveis booleanas 

* Podemos usar uma variavel booleana e depois alterar seu valor dentro de uma instrução if/else
```python
# Exemplo de Variaveis booleanas
valor  = True
valor_1 = False

# Podemos mudar o valor delas dentro de um if/else
```

## CONSTRUÇÃO DE UMA INSTRUÇÃO IF/ELSE

Existem algumas formas de fazer essas instruções:

**INSTRUÇÃO DE IF UNICO**
* podemos somente ter uma instrução if ou vários if juntos, usando cada um dos testes condicionais
```python
# CONSTRUÇÃO DE UM IF NORMAL VAZIO

if condicao:
    pass
# quando é criado uma instrução vazia usamos pass

# USANDO IF COM CADA CONDIÇÃO VISTA

# IGUALDADE

if 3 == 3: # este if é iniciado porque deu True o teste
    print(3) # imprime na tela o numero

if 3 == 4: # este if NÃO É INICIADO(deu false o teste)
    print(3) # NÃO IMPRIME 

# DIFERENÇA

if 3 != 4: # este if é iniciado porque deu True o teste
    print(3)

if 3 != 3: # este if NÃO É INICIADO(deu false o teste)
    print(3) # NÃO IMPRIME 

# COMPARAÇÃO

a = 3
b = 4

if a < b:  # True, if iniciado
if a > b:  # False, if não iniciado

if a <= b: # True, if iniciado
if a >= b: # False, if não iniciado

# MULTIPLOS TESTES

if a < b and a <= b: # TRUE  AND TRUE  = TRUE
if a > b and a <= b: # FALSE AND TRUE  = FALSE
if a < b and a >= b: # TRUE  AND FALSE = FALSE
if a > b and a >= b: # FALSE AND FALSE = FALSE

if a < b or a <= b: # TRUE  OR  TRUE  = TRUE
if a > b or a <= b: # FALSE OR  TRUE  = TRUE
if a < b or a >= b: # TRUE  OR  FALSE = TRUE
if a > b or a >= b: # FALSE OR  FALSE = FALSE


# TESTE COM NOT

if not 1+1 = 2:
    print('Este print não acontece')
else:
    print('este print acontece')

# VARIOS IFS UNICOS RODANDO EM SERIE

a = 1
b = 2
c = 3
d = 4

if a < b: # podemos colocar um if dentro de outro if
    if d > c: # este if somente ira ocorrer se o primeiro for true
        pass

if a < b: 
    pass
if d > c: # este if é externo, e ocorre msm se o primeiro for false
    pass
```

**INSTRUÇÃO DE IF COM ELSE:**

* quando a instrução do if for false e queremos que o programa faça algo com isso, criamos um `else` que irá ser ativado se o if der false

```python

# ESTRUTURA DE UM IF/ELSE

if instrucao:
    info
else:
    info

# Exemplo completo de um if/else

a = 2
b = 2

if a > b:
    print("Este print não ocorre")
else:
    print("if deu falso, else ativou")
```

**INSTRUÇÃO IF-ELIF-ELSE**

* quando queremos colocar mais opções de instruções, utilizamos o `elif` entre as opções, começando com um `if` e no fim terá um else

_Como é em Java_

```java

// CONSTRUÇÃO DE INSTRUÇÕES EM JAVA
if (intrucao){

}else if(instrucao2){

}else{

}
```
_Como é em Python_

```python
# CONSTRUÇÃO DE MULTIPLAS INSTRUÇÕES EM PYTHON

if instrucao:
    intro
elif instrucao:
    intro
else:
    intro

# EXEMPLO

idade = 20

if idade < 4: 
    preco = 0
elif idade >= 20:
    preco = 40
else:
    preco = 100
print(preco) # a saida vai ser 40

# PODEMOS COLOCAR VARIOS ELIFS

if idade < 4:
    preco = 0
elif idade == 10:
    preco = 10
elif idade <= 15:
    preco = 20
elif idade == 20:
    preco = 40
else:
    preco = 60
```

**IF/ELSE COM LISTAS**

* Podemos verificar se um elemento existe dentro da lista com if/else
* Como o for anda por toda a lista, podemos usar um if para ver dentro da lista

```python
nomes = ['Gabriel','Pedro','Lili','Igor']

for nome in nomes:
    if nome == 'Gabriel':
        print('Nome existe na lista')
    else:
        pass
```