    [[Página Inicial](../tut_pages/home.md)]

---

# Comandos Básicos de Markdown

---

Aqui irei te apresentar comandos Básicos de o que se pode fazer em Markdown.


## Como marcar uma palavra:

```
**Texto em Negrito**

_Texto em Italico_

`Texto em Especial`
```

Exemplo:

**Texto em Negrito**

_Texto em Italico_ 

`Texto em Especial`


## Como colocar links em Markdown

Podemos colocar links usando a seguinte estrutura

```
[nome do link](url)
```

Exemplo

[Isto é um Link para o google](https://www.google.com)

```
[Isto é um Link para o google](https://www.google.com)
```


## Como colocar código em Markdown

* Siga a seguinte estrutura: 

<code style="color : gold">```nome_linguagem</code>

<code style="color : lightgreen">Código em Si</code>

<code style="color : gold">```</code>

Exemplos:

```java
//Programa em Java
public static void main(String args[]){
    System.out.println("Hello World");
}

```

```c
//Programa em C

#include<stdio.h>

int main(){
    printf("Hello World");
}
```

```python
# Programa em Python

class teste:
    def __init__:
        # Teste somente 
```

## Como colocar uma Tabela no Markdown

```
Coluna 1|Coluna 2
|---|---|
Linha 1 Parte 1|Linha 1 Parte 2

```

Exemplo:

Coluna 1|Coluna 2
|---|---|
Linha 1 Parte 1|Linha 1 Parte 2

## Como colocar tópicos em Markdown

Tópicos são uma forma de se poder demonstrar passos onde eles ficam marcados passo a passo

Tópicos com Asteriscos

```
* Tópico 1
    * Tópico 1 a
    * Tópico 1 b
* Tópico 2
    * Tópico 2 a
    * Tópico 2 b

```

Exemplo:

* Tópico 1
  * Tópico 1 a
  * Tópico 1 b
* Tópico 2
  * Tópico 2 a
  * Tópico 2 b

Tópicos com Números

```
1. Tópico 1
    1. Tópico 1 a
    2. Tópico 1 b
2. Tópico 2
```

Exemplo:

1. Tópico 1
   1. Tópico 1 a
   2. Tópico 1 b
2. Tópico 2

## Como colocar imagem em Markdown

Eu irei mostrar duas formas de se colocar imagem


#### Usando Tags

A tag `<img>` funciona em Markdown, como mostrado abaixo

**Imagem Simples**

```html
<img src="../../img/md-icon.png">
```

* `src` irá chamar o local onde a imagem está armazenada, onde pode ser em um diretorio interno ou um url de uma imagem da internet
* `../..` serve para dizer que o direto do img está a dois diretorios externos de onde se encontra esse arquivo
* `img` é o nome do Diretório onde guardei as imagens desse site
* `md-icon.png` é o nome e a extensão da imagem que eu desejo apresentar na tela

Exemplo:

<img src="../../img/md-icon.png">

**Imagem Diminuida**

Podemos mudar o tamanho de nossa imagem usando a tag `<img>` onde dentro dela usaremos os comandos `width` e o `heigth` para determinar o tamanho desejado da imagem:

```html
Tamanhos sao em megapixels

<img src="../../img/md-icon.png" width="100"> 100 megapixels
<img src="../../img/md-icon.png" width="200"> 200 megapixels
<img src="../../img/md-icon.png" width="300"> 300 megapixels
 ```

Exemplo

<img src="../../img/md-icon.png" width="100"><img src="../../img/md-icon.png" width="200"><img src="../../img/md-icon.png" width="300">

**Centralizando imagens**

Podemos centralizar uma imagem usando a tag `<center>` que irá nos auxiliar em direcionar a imagem para o centro da tela.

```html
<center>
    <img src="../../img/md-icon.png" width="200">
</center>
```

Exemplo:

<center>
    <img src="../../img/md-icon.png" width="200">
</center>


## Sistema de Cores em Páginas no Markdown

Agora irei mostrar como colocar cores nos textos do Markdown

OBS: isso funciona em arquivos comuns de Markdown e no Github Pages, nas Wikis do Github infelimente essa tag não funciona

iremos usar a tag `<code>` para podermos determinar a cor de um texto

```html
<code style="color : nome_cor">Texto desejado</code>
```

Existem várias cores que Podemos usar, para isso mostrarei a tabela abaixo:


Nome da Cor|Teste de Testo|Código
|---|---|---|
<code style="color : aqua">Aqua</code>|<code style="color : aqua">TESTE</code>|`<code style="color : aqua">TESTE</code>`
<code style="color : aquamarine">Aquamarine</code>|<code style="color : aquamarine ">TESTE</code>|`<code style="color : aquamarine">TESTE</code>`
<code style="color : blue">Blue</code>|<code style="color : blue">TESTE</code>|`<code style="color : blue">TESTE</code>`
<code style="color : cyan">Cyan</code>|<code style="color : cyan">TESTE</code>|`<code style="color : cyan">TESTE</code>`
<code style="color : darkorange">Darkorange</code>|<code style="color : darkorange">TESTE</code>|`<code style="color : darkorange">TESTE</code>`
<code style="color : green">Green</code>|<code style="color : green">TESTE</code>|`<code style="color : green">TESTE</code>`
<code style="color : greenyellow">Greenyellow</code>|<code style="color : greenyellow">TESTE</code>|`<code style="color : greenyellow">TESTE</code>`
<code style="color : fuchsia">Fuchsia</code>|<code style="color : fuchsia">TESTE</code>|`<code style="color : fuchsia">TESTE</code>`
<code style="color : gold">Gold</code>|<code style="color : gold">TESTE</code>|`<code style="color : gold">TESTE</code>`
<code style="color : lightskyblue">LightSkyBlue</code>|<code style="color : lightskyblue">TESTE</code>|`<code style="color : lightskyblue">TESTE</code>`
<code style="color : magenta">Magenta</code>|<code style="color : magenta">TESTE</code>|`<code style="color : magenta">TESTE</code>`
<code style="color : orangered">Orangered</code>|<code style="color : orangered ">TESTE</code>|`<code style="color : orangered">TESTE</code>`
<code style="color : purple">Purple</code>|<code style="color : purple">TESTE</code>|`<code style="color : purple">TESTE</code>`
<code style="color : red">Red</code>|<code style="color : red">TESTE</code>|`<code style="color : red">TESTE</code>`
<code style="color : yellowgreen">Yellowgreen</code>|<code style="color : yellowgreen">TESTE</code>|`<code style="color : yellowgreen">TESTE</code>`


## Subdivisão de Informações

Podemos dividir informações usando `---` encima e embaixo de uma informação


```html

---

<center>
    <code style="color : gold">GLOSSÁRIO</code>
</center>

---

```

Exemplo:


---

<center>
    <code style="color : gold">GLOSSÁRIO</code>
</center>

---