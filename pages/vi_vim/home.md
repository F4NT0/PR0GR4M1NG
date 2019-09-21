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

<br>
<br>

## COMANDOS DE TECLADO UTEIS

<center>
    Estes comandos servem para modificar o texto fora da forma de insercao, muito uteis para trabalhar com os arquivos
</center> 

<br>

Comando|Para que serve
|---|---|
<code style="color : magenta">dd</code> | Deleta uma linha inteira
<code style="color : magenta">x</code>| Deleta a letra vinda depois do cursor
<code style="color : magenta">l</code>| Move o Cursor para a Direita na Linha Atual
<code style="color : magenta">h</code>| Move o Cursor para a Esquerda na Linha Atual
<code style="color : magenta">j</code>| Move o Cursor para a Linha Abaixo
<code style="color : magenta">k</code>| Move o Cursor para a Linha Acima

<br>

## CTRL C + CTRL V NO VI E VIM

<center>
    <code style="color : lightgreen">ATIVE O MODO DE VISUAL</code>
    <br>
    <br>
    <code style="color : magenta">v</code>
    <br>
    <code style="color : yellow">Marca palavra por palavra na linha(use as setas para ir marcando)</code>
    <br>
    <br>
    <code style="color : magenta">V</code>
    <br>
    <code style="color : yellow">Marca a Linha inteira onde o Cursor estiver</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/visual_mode.gif">
</center>
<br>
<center>
    <code style="color : lightgreen">COMANDO DE COPIA</code>
    <br>
    <br>
    <code style="color : magenta">y</code>
    <br>
    <code style="color : yellow">No modo Visual, apos selecionado o texto desejado, clique em y para copiar o texto</code>
    <br>
    <br>
    <code style="color : magenta">yy</code>
    <br>
    <code style="color : yellow">Fora de qualquer sistema, copia toda a linha do cursor</code>
</center>
<br>
<br>
<center>
    <code style="color : lightgreen">COMANDO DE COLAR</code>
    <br>
    <br>
    <code style="color : magenta">p</code>
    <br>
    <code style="color : yellow">Se direcione a linha que deseja e clique em p para colar o que foi copiado antes do cursor</code>   
    <br>
    <br>
    <code style="color : magenta">P</code>
    <br>
    <code style="color : yellow">Se direcione a linha que deseja e clique em p para colar o que foi copiado depois do cursor</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/copy_paste.gif">
</center>
<br>
<br>
<center>
    <code style="color : lightgreen">COPIANDO E SALVANDO EM OUTRO ARQUIVO</code>
    <br>
    <br>
    <code style="color : lightblue">1. Ative o modo visual com a tecla </code><code style="color : red ">v</code>
    <br>
    <code style="color : lightblue">2. Ande com o as setas ate selecionar tudo que deseja copiar</code>
    <br>
    <code style="color : lightblue">3. Selecione a tecla</code><code style="color : red"> y</code>
    <br>
    <code style="color : lightblue">4. Ative a area de comando com</code><code style="color : red"> :</code>
    <br>
    <code style="color : lightblue">5. Coloque o comando</code><code style="color : red"> sh</code>
    <br>
    <code style="color : lightblue">6. Va ate o arquivo desejado que deseja colar o texto</code>
    <br>
    <code style="color : lightblue">7. Abra o arquivo no VI ou VIM</code>
    <br>
    <code style="color : lightblue">8. Apos aberto o arquivo va ate a linha desejada com as setas ou com j,k,h,l</code>
    <br>
    <code style="color : lightblue">9. Cole o texto com</code><code style="color : red"> p</code><code style="color : lightblue"> ou</code><code style="color : red"> P</code>
    <br>
    <code style="color : lightblue">10. Salve o Arquivo</code>
    <br>
    <code style="color : lightblue">11. Se quiser voltar ao arquivo anterior, volte ao terminal e selecione no teclado</code><code style="color : red"> CTRL + D</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/copy_paste_2.gif">

</center>


