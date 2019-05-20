[[Página Inicial](../prog_python/home.md)]

---

## Trabalhando com arquivos externos em Python

---

* Podemos criar e escrever em arquivos externos em Python

**1) Abrindo Arquivos**

* É muito fácil abrir arquivos em python, utilizamos a função `open()`
* A função **Open()** recebe como parâmetro o nome do arquivo desejado e a forma como deseja mexer nele
* construção básica:
```python
meu_arquivo = open('nomeArquivo.txt','forma')
```
* Se o arquivo não existir, ele criará um arquivo dentro do diretorio atual do programa
* Ele somente consegue ler o arquivo de duas formas:
    * Se o arquivo estiver no mesmo diretorio, só coloque o nome
    * Se estiver em outro diretorio, coloque o caminho até ele tambem

* Formas de Ler o Arquivo:

|Forma| Definição
|---|---|
|r | modo leitura(read)
|w | modo escrita(write)
|b| modo binário(binary)
|a| modo de adição(append)

```python
# para somente ler o arquivo 
arquivo = open('texto.txt','r')
# para somente escrever no arquivo
arquivo = open('texto.txt','w')
# para poder adicionar mais uma linha no arquivo
arquivo = open('texto.txt','a')
```

**2) Fechando arquivos**

* para fechar o arquivo usamos a função `close()`

```python
arquivo = open('texto.txt','w')
...
arquivo.close()
```

**3) Lendo um arquivo**

* usamos a função `read()` para podermos ler um numero de bytes
* definimos quantos bytes leremos ou leremos tudo se nada for definido

```python
arquivo = open('texto.txt','r')
texto = arquivo.read(16) # le 16 bytes 
texto = arquivo.read() # le tudo 
arquivo.close()
```

* Se quiser ler linha por linha, usamos a função `readlines()`

```python
arquivo = open('texto.txt','r')
linha = arquivo.readlines()
arquivo.close()
```

* podemos usar um for para ler tambem:

```python
arquivo = open('texto.txt','r')
for linha in arquivo:
    print(linha)
arquivo.close()
```

* Podemos ler tambem toda a informação de um arquivo com a contrução `with...as...` onde podemos fazer com que o usuário diga o nome do arquivo

```python
arquivo = input('Digite o nome do arquivo: ')

with open(arquivo) as arq:
    texto = arq.read()
print(texto)
```

**4)  Escrevendo em um arquivo**

* podemos escrever em um arquivo usando a função `write()`

```python
valor = 1
valor_2 = 20

arquivo = open('texto.txt','r')
arquivo.write(str(valor) + ' ' + str(valor_2)) # 1 20
arquivo.close()
```
