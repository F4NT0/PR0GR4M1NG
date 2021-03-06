[[**Página inicial**](https://f4nt0.github.io/PR0GR4M1NG)]

<br>

# Página sobre VI e VIM


<br>

<center>
    <img src="../../img/vim_icon.png" width="200">
</center>

<br>
<br>

<code style="color : yellow">Editor de Texto via Terminal para desenvolvimento de codigo mais Rapido</code> 

<br>
<br>

<center>
    <code style="color : yellowgreen">Instalando via Terminal: </code>
    <br>
    <br>
    <code style="color : lightblue">sudo apt-get install vim</code>
</center>

<br>
<br>

<center>
    <code style="color : yellowgreen">Iniciando via Terminal: </code>
    <br>
    <br>
    <code style="color : lightblue">vim </code><code style="color : magenta">nomedoarquivo.extensao</code>
</center>

<br>
<br>

## MODO DE INSERCAO

<br>
<br>

<center>
    <code style="color : yellowgreen">Iniciando o modo de insercao</code>
    <br>
    <code style="color : magenta">i</code>
    <br>
    <br>
    <code style="color : yellow">Clique no botao do teclado </code><code style="color : magenta">i</code><code style="color : yellow"> no VI e VIM para ativar o modo de insercao de texto</code>
    <br>
    <br>
    <code style="color : yellow">Para Sair do modo de Insercao clique em </code><code style="color : lightblue">ESC</code>
    <br>
    <code style="color : yellow">O modo de comandos so funciona fora do modo de insercao</code>
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
    <code style="color : magenta">:</code>
    <br>
    <br>
    <code style="color : yellow">Apos ativar o modo de comando com </code><code style="color : magenta">:</code><code style="color : yellow"> escreva o comando que deseja.</code>
    <br>
    <br>
    <code style="color : yellow">Para ativar o comando clique em </code><code style="color : lightblue">ENTER</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <img src="../../gifs/commands.gif">
</center>

<br>

<center>
    <br>
    <code style="color : yellow">Para ativar os numeros das paginas, digite o seguinte comando:</code>
    <br>
    <br>
    <code style="color : magenta">:</code><code style="color : magenta">set nu</code>
    <br>
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
    <code style="color : magenta">/</code>
    <br>
    <br>
    <code style="color : white">Exemplo:</code>
    <br>
    <br>
    <code style="color : magenta">/</code><code style="color : lightblue">palavra</code>
    <br>
</center>
<br>
<br>
<center>
    <code style="color : yellowgreen">Pesquisa procurando palavras mais a frente </code>
    <br>
    <code style="color : magenta">?</code>
    <br>
    <br>
    <code style="color : white">Exemplo:</code>
    <br>
    <br>
    <code style="color : magenta">?</code><code style="color : lightblue">palavra</code>
</center>
<br>
<br>
<center>
    <code style="color : orange">Exemplo</code>
    <br>
    <br>
    <code style="color : yellow">Apos escolhido uma das opcoes, coloque a palavra que procura e clique em </code><code style="color : lightblue">ENTER</code><code style="color : yellow"> para ir a palavra que procura</code>
    <br>
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
    <code style="color : yellow">Estes comandos servem para modificar o texto fora da forma de insercao, muito uteis para trabalhar com os arquivos</code>
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
<code style="color : magenta">u</code>| Desfaz uma modificacao no arquivo

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
    <code style="color : yellow">1. Ative o modo visual com a tecla </code><code style="color : magenta ">v</code>
    <br>
    <code style="color : yellow">2. Ande com o as setas ate selecionar tudo que deseja copiar</code>
    <br>
    <code style="color : yellow">3. Selecione a tecla</code><code style="color : magenta"> y</code>
    <br>
    <code style="color : yellow">4. Ative a area de comando com</code><code style="color : magenta"> :</code>
    <br>
    <code style="color : yellow">5. Coloque o comando</code><code style="color : magenta"> sh</code>
    <br>
    <code style="color : yellow">6. Va ate o arquivo desejado que deseja colar o texto</code>
    <br>
    <code style="color : yellow">7. Abra o arquivo no VI ou VIM</code>
    <br>
    <code style="color : yellow">8. Apos aberto o arquivo va ate a linha desejada com as setas ou com j,k,h,l</code>
    <br>
    <code style="color : yellow">9. Cole o texto com</code><code style="color : magenta"> p</code><code style="color : yellow"> ou</code><code style="color : magenta"> P</code>
    <br>
    <code style="color : yellow">10. Salve o Arquivo</code>
    <br>
    <code style="color : yellow">11. Se quiser voltar ao arquivo anterior, volte ao terminal e selecione no teclado</code><code style="color : magenta"> CTRL + D</code>
    <br>
    <br>
    <code style="color : orange">Exemplo</code>
    <br>
    <img src="../../gifs/copy_paste_2.gif">

</center>
<br>
<br>

## CONFIGURANDO O VIM

<center>
    <code style="color : yellow">Existe um arquivo de configuracao para podermos contruir um VIM  configuravel</code>
    <br>
    <br>
    <code style="color : lightgreen">Criando arquivo para configurar</code>
    <br>
    <br>
    <code style="color : yellow">Crie um arquivo oculto no Diretorio</code><code style="color : lightblue"> HOME</code><code style="color : yellow"> chamado </code><code style="color : lightblue">.vimrc</code>
    <br>
    <br>
    <code style="color : yellow">Digite nesse arquivo as configuracoes desejadas que precisa</code>
    <br>
    <br>
    <code style="color : yellow">Abaixo um exemplo de configuracao</code>
    <br>
    <br>
    <code style="color : yellow">Apos escrito a configuracao, salve o arquivo, se nao salvar automativamente, digite no terminal:</code>
    <br>
    <br>
    <code style="color : lightgreen">source ~/.vimrc</code>
    
</center>

```vim

" -------------------------------
"  ARQUIVO DE CONFIGURACAO DO VIM
" -------------------------------

" iniciar a sintaxe das linguagens de programacao
syntax on

" Apresentar o numero das linhas
set number

" Indentar novas linhas
set autoindent

" Verifica o que e escrito
set spell

" Indentacao automatica
set smartindent

" highlight todas as buscas
set hlsearch

" salva automaticamente
set autowriteall
```

