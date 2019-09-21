[[**Página inicial**](https://f4nt0.github.io/PR0GR4M1NG)]

<br>

# Página sobre VI e VIM


<br>

<center>
    <img src="../../img/vim_icon.png" width="200">
</center>

<br>
<br>

Editor de Texto via Terminal para desenvolvimento de codigo mais Rapido 

<br>
<br>

<center>
    <code style="color : yellowgreen">Instalando via Terminal: </code><code style="color : lightblue">sudo apt-get install vim</code>
</center>

<br>
<br>

<center>
    <code style="color : yellowgreen">Iniciando via Terminal: </code><code style="color : lightblue">vim </code><code style="color : tomato">nomedoarquivo.extensao</code>
</center>

<br>
<br>

## MODO DE INSERCAO

<br>
<br>

<center>
    <code style="color : yellowgreen">Iniciando o modo de insercao</code>
    <br>
    <code style="color : tomato">i</code>
    <br>
    <br>
    Clique no botao do teclado <code style="color : tomato">i</code> no VI e VIM para ativar o modo de insercao de texto
    <br>
    <br>
    Para Sair do modo de Insercao clique em <code style="color : lightblue">ESC</code>
    <br>
    O modo de comandos so funciona fora do modo de insercao
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/insertion.gif">
</center>

<br>
<br>

## MODO DE COMANDOS

<br>
<br>

<center>
    <code style="color : yellowgreen">Iniciando modo de comandos do vi e vim </code>
    <br>
    <code style="color : tomato">:</code>
    <br>
    <br>
    Apos ativar o modo de comando com <code style="color : tomato">:</code> escreva o comando que deseja.
    <br>
    <br>
    Para ativar o comando clique em <code style="color : lightblue">ENTER</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <img src="../../gifs/commands.gif">
</center>

<br>

<center>
    <br>
    Para ativar os numeros das paginas, digite o seguinte comando:
    <br>
    <br>
    <code style="color : tomato">:</code><code style="color : magenta">set nu</code>
    <br>
    E depois clique em <code style="color : lightblue">ENTER</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/numbers.gif">
</center>

<br>

### Lista de comandos

Comando | Para que serve
|---|---|
<code style="color : magenta">q</code>| Fecha o arquivo se nada foi modificado
<code style="color : magenta">q!</code>| Encerra o programa forçadamente, apagando todas as mudanças
<code style="color : magenta">w</code>| Salva o arquivo que foi modificado
<code style="color : magenta">wq</code>| Salva o arquivo e o fecha automaticamente
<code style="color : magenta">set nu</code>| Ativa os numeros das linhas do arquivo
<code style="color : magenta">sh</code>| Volta para o shell fora do arquivo, para voltar ao arquivo clique em <code style="color : lightblue">CTRL + D</code>

<br>
<br>

## MODO DE PESQUISA

<br>
<br>

<center>
    <code style="color : yellowgreen">Pesquisa procurando palavras anteriores </code>
    <br>
    <code style="color : tomato">/</code>
    <br>
    <br>
    <code style="color : white">Exemplo:</code>
    <br>
    <br>
    <code style="color : tomato">/</code><code style="color : lightblue">palavra</code>
    <br>
</center>
<br>
<br>
<center>
    <code style="color : yellowgreen">Pesquisa procurando palavras mais a frente </code>
    <br>
    <code style="color : tomato">?</code>
    <br>
    <br>
    <code style="color : white">Exemplo:</code>
    <br>
    <br>
    <code style="color : tomato">?</code><code style="color : lightblue">palavra</code>
</center>
<br>
<br>
<center>
    <code style="color : orange">Exemplo</code>
    <br>
    <br>
    Apos escolhido uma das opcoes, coloque a palavra que procura e clique em ENTER para ir a palavra que procura
    <br>
    <img src="../../gifs/search.gif">
</center>

### Lista de Comandos para pesquisa

Comando|Para que serve
|---|---|
<code style="color : magenta">/</code>| Pesquisa uma palavra que ja foi escrita, antes do mouse
<code style="color : magenta">?</code>| Pesquisa uma palavra que esta escrita depois do mouse
<code style="color : magenta">n</code> | Refaz a pesquisa novamente
