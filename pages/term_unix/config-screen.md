[[Página Inicial](../term_unix/home.md)]

# Como configurar seu Visual do Terminal

Podemos fazer várias modificações no Terminal, mas iremos ver algumas nessa Página


## Minha configuração do meu Terminal

---

* MEU PS1 NO ARQUIVO <code style="color: lightgreen">PS1='${debian_chroot:+($debian_chroot)}F4NT0:\W $(__git_ps1 " (%s)") >'</code>
* entre cada info tem uma cor, ficando assim:
<img src="../../../img/ubuntu_fanto.png">

---


## Customizando as informações do prompt

---

Quando iniciamos um Terminal, no Lado esquerdo podemos ver informações sobre o Terminal em si, onde podemos ver o seguinte:

```bash
nome_usuario@nome_host caminho/dos/diretorios $
```

Existem códigos de como funciona essa visualização, que chamamos Saída de Prompt <code style="color : lightgreen">PS1</code>

Se deseja saber quais comandos usados no PS1 do seu Usuário, utilize o seguinte comando

```bash
echo $PS1
```

O tipo de Saída será algo como isso: <code style="color : lightblue">\u@\h \W \$</code>

Aqui tem uma Lista de Comandos que podemos usar no nosso PS1

Código|Informação
|---|---|
<code style="color : red">\d</code>| Apresenta a data atual (dia mes ano)
<code style="color : red">\h</code>| Apresenta o nome do dono do sistema(hostname)
<code style="color : red">\t</code>| O horário atual em formato de 24h (HH:MM:SS)
<code style="color : red">\u</code>| Apresenta o Nome do Usuário atual logado
<code style="color : red">\w</code>| Apresenta o caminho até o Diretório atual e a pasta Home é abreviada com <code style="color : gold">~</code>
<code style="color : red">\W</code>| Mostra somente o Diretório Atual e se deseja ver o caminho todo use o comando <code style="color: gold">pwd</code>
<code style="color : red">\\[</code> e <code style="color : red">\\]</code>| Coloca toda a informação dentro de dois [ ] no Terminal

#### Encontrando o PS1

Para acessar o <code style="color : lightgreen">PS1</code> para poder modificar o Sistema,coloque o seguinte programa:

* <code style="color : lightblue">sudo nano ~/.bashrc</code>

Porcure o primeiro PS1 que aparece e Modifique como deseja

#### Código ANSI de Cores

Código ANSI é um código de Cores que serve para poder colocar saida de cores no terminal como desejado

* A estrutura do Sistema ANSI é o seguinte: <code style="color : gold">\e[<code style="color : orange">background</code> ; <code style="color : cyan">foreground</code>m</code>
  * Não é preciso adicionar a cor de fundo se não quiser

* Para parar uma Cor vazada, usamos o seguinte comando: <code style="color : gold">\e[0m</code>

* Podemos adicionar os valores em uma Variável que irá auxiliar nas Saidas de Cores: <code style="color : greenyellow">RED='\e[40;31m'</code>

* Podemos testar as Saídas no terminal as Cores da seguinte forma

```bash
echo -e "\e[40;31mVERMELHO"

# ou

echo -e "\e[31mVERMELHO"
```

* Abaixo segue a Tabela com as Cores Principais

Tipo da Cor|Código da Cor|Nome da Cor
|---|---|---|
Foreground|31| VERMELHO FORTE
Foreground|32| VERDE FORTE
Foreground|33| AMARELO FORTE
Foreground|34| AZUL FORTE
Foreground|35| MAGENTA FORTE
Foreground|36| CIANO FORTE
Foreground|91| VERMELHO FRACO
Foreground|92| VERDE FRACO
Foreground|93| AMARELO FRACO
Foreground|94| AZUL FRACO
Foreground|95| MAGENTA FRACO
Foreground|96| CIANO FRACO
Foreground|97| BRANCO

---

Tipo da Cor|Código da Cor|Nome da Cor
|---|---|---|
Background| 40| PRETO
Background| 41| VERMELHO
Background| 42| VERDE
Background| 43| AMARELO
Background| 44| AZUL
Background| 45| MAGENTA
Background| 46| CIANO
Background| 101| VERMELHO FRACO
Background| 102| VERDE FRACO
Background| 103| AMARELO FRACO
Background| 104| AZUL FRACO
Background| 105| MAGENTA FRACO
Background| 106| CIANO FRACO
Background| 107| BRANCO

Exemplo total de um PS1:

```bash
PS1='${debian_chroot:+($debian_chroot)}\[\e[01;31m\]\u\[\e[0m\]'
```

---


## Configurando o GIT no Terminal

---

* Agora irei mostrar como botar o programa no git para aparecer no Terminal
* Esse sistema serve para verificarmos o Status e a Branch que estamos trabalhando
  * `*` = mostra que tem coisas novas na Branch que devem ser salvas com _git add_
  * `+` = mostra que foi salvo as coisas novas e está tudo pronto para fazer _git commit_
  * `(master)` = é o nome da Branch atual no Repositório que você está trabalhando

* Abra o arquivo <code style="color: lightblue">sudo vim ~/.bashrc</code>
* Dentro do arquivo clique em <code style="color: lightgreen">i</code>
* Vá até o fim do arquivo e coloque <code style="color: orange">export</code><code style="color: lightblue">GIT_PS1_SHOWDIRTYSTATE=1</code> 
* então vai até o fim do PS1 apresentado anteriormente e coloque o seguinte comando: <code style="color: lightblue">$(__git_ps1 " (%s)")</code>
* saia do modo inserção com <code style="color: lightgreen">ESC</code> e depois coloque o comando <code style="color: orange">:wq</code>
* coloque no terminal o comando <code style="color: lightblue">source ~/.bashrc</code>

<img src="../../../img/git_system.png">

---

## Colocando uma Mensagem na Tela do Terminal

---

Vamos Colocar uma Mensagem no Terminal, para que toda vez que eu abrir um Terminal apresente a mensagem na Tela

* Baixando o Programa <code style="color : lightgreen">FIGLET</code>:

* <code style="color : red">sudo apt-get install</code> <code style="color : lightblue">figlet</code>

* Para ver todos os tipos de fontes do Figlet: <code style="color : blue">showfigfonts</code>


Agora iremos usar esse programa no Nosso Sistema para aparecer na Tela

* Entre no Arquivo onde fica o Sistema do Terminal: <code style="color : gold">sudo nano /etc/bash.bashrc</code>

* Desce até o fim do código e no fim deixe uma linha vazia

* Abaixo tem um exemplo de código para colocar no Arquivo

```bash
# Cores ANSI para usar

ORANGE="\e[33m" #Cor laranja
STOP="\e[0m" # Para parar a Saida de Cores

# Mensagem

printf "${ORANGE}" # Saída da Cor Laranja no Terminal

figlet -f standard "FANTO" # Aqui colocamos os comandos da mensagem
# o texto deve ser entre " " e standard é o nome da Fonte

printf "${STOP}" # Para finalizar a Saída da Cor

```


---


