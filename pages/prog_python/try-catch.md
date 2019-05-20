[[Página Inicial](../prog_python/home.md)]

---

# Tratamento de Exceções em Python

---

* Lista de Alguns Tipos de Exceções

Nome|Descrição
|---|---|
ImportError|Quando não consegue importar
IndexError|Quando a lista está indexada fora do tamanho máximo permitido
NameError|Variável desconhecida foi usada
SyntaxError| quando o código não pode ser analisado devidamente
TypeError|Quando uma função é chamada com um tipo inapropriado
ValueError|Quando uma função é chamada do tipo certo, mas o valor errado
ZeroDvisionError|Quando se tenta dividir por zero
OSError | Quando um comando do pacote os não é feito devidamente

**Estrutura try/except**

* `try` é um bloco de comandos que contem um código que talvez possa ocorrer uma exceção,se ocorrer uma exceção, o bloco `except` irá ocorrer, senão o código irá continuar

* `except` é um bloco de comandos que ocorrem somente se uma exceção ocorrer,podendo ter vários para cada tipo de exceção possivel que possa ocorrer, ou se deixar sem uma exceção expecifica, ele irá pegar todos os tipos de exceções

```python
# Tratando divisão por zero
try:
    valor_1 = 7
    valor_2 = 0
    div = 7/0 # vai dividir por zero e puxa uma exceção
except:
    print('Não se pode dividir por zero')

# Tratando valor de saída nao permitido e erro de digitação

try:
    valor = 10
    print(valor + 'é um número') # vai ocorrer uma exceção TypeError
    print(valor / 2) # vai ocorrer uma exceção ValueError
except ZeroDivisionError:  # não irá acontecer
    print('Nao pode dividir por zero!')
except TypeError: # irá ocorrer
    print('Arrumando a saida...')
    print(str(valor) + 'é um número')
except ValueError: # irá ocorrer
    print('Arrumando a Saida...')
    print(str(valor/2))
```

* `finally` é um bloco de comandos que irá acontecer não importando se for acontecer exceções ou não, ele sempre fica no final do `try/except`

```python
try:
    divisao = 10/0
except ZeroDivisionError:
    print('Esta exceção aconteceu')
finally:
    print('Este bloco sempre vai acontecer')
```

**Como fazer raise em uma exceção**

* `raise` é uma forma de criar uma exceção e explicar melhor porque a exceção aconteceu aconteceu
* dizemos qual exceção aconteceu e podemos colocar uma string explicando porque aconteceu
* Tudo que vier depois do `raise` não irá acontecer

```python
nome = input('Digite o seu nome: ')
raise NameError('Esse não é seu nome...')
```

* Podemos usar `raise` dentro de um `except` para trazer para a tela qual erro aconteceu

```python
try:
    numero = 5 / 0
except:
    print('Erro Ocorreu!')
    raise
# Saida:
# Erro Ocorreu!
# ZeroDivisionError: division by zero
```

**Usando Assertion**

* `assertion` serve para verificar e testar se tudo está certo e se der false, uma exceção irá ocorrer, normalmente usado para testar entradas de usuário e saida de funções
* se ocorrer uma exceção, o programa irá parar

```python
assert 2 + 2 == 4 # True
assert 1 + 1 == 3 # False
# programa para

# Saída : AssertionError
```
