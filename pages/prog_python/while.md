[[Página Inicial](../prog_python/home.md)]

---
# Como fazer um Laço While em python

---

* A estrutura de um while é bem simples
* Um `Laço While` serve para manter algo acontecendo quanto tempo quisermos
* sempre que a instrução dada a um while for um **True booleano** ele se mantem rodando o while

```python
# Construção básica de um while
while instrucao:
    infos
```
Se não colocarmos uma forma de para o while iremos fazer um `loop infinito`

```python
# EXEMPLO DE LOOP INFINITO
booleano = True
valor = 0
while booleano:
    valor += 1
    print('Valor agora é: ',str(valor))
```

Para podermos parar um while, tem algumas formas:
* Definimos que a instrução do while tem um `momento limite`(ou seja, a instrucao vai parar sozinha depois de um tempo)
* Alteramos o valor booleano de uma variavel, onde antes era `True` e colocamos como `False`
* Podemos usar a palavra reservada `break` para finalizar o laço bruscamente, onde ele ira continuar o código escrito fora do while
* Podemos usar a palavra reservada `continue` para voltar ao inicio do laço quando quisermos, ignorando o resto que vem após

```python
# EXEMPLO 1

valor = 2
contador = 1 # serve para dizer quantas vezes aconteceu o while

# quando o valor chegar em zero, o while irá parar
while valor > 0:
    print('Interacao do while ',str(contador),':')
    contador += 1
    valor -= 1 

# EXEMPLO 2

booleano = True

while booleano:
    stop = input('Deseja parar o while? S/N: ')
    if stop == 'S':
        print('Parando o While...')
        booleano = False 
    elif stop == 'N':
        print('Continuando o While...')
        # Não precisa alterar o valor do booleano
    else:
        print('Valor não aceito!')
        break #para o while bruscamente

# EXEMPLO 3
 booleano = True
 while booleano:
     if booleano == True:
        parada = input('Deseja iniciar de novo? S/N : ')
        if parada == 'S' or parada == 's':
            continue
        elif parada == 'N' or parada == 'n':
            booleano = False
        else:
            print('Entrada invalida! encerrando...')
            break
```

