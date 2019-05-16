# Como compilar arquivos em C

* Aqui irei ensinar como se compila um arquivo C para testar seus projetos no terminal, onde pode acontecer de tudo no Terminal:


<center>
<code style="color : lightgreen" font-size="4">Sistema Linux</code>
</center>
<center>
    <img src="../../img/icon-linux.png">
</center>

Baixe o programa **<code style="color : yellow">gcc</code>**

---

<code style="color : yellow">$ sudo apt-get install gcc</code>

---

Após baixado o programa, coloque o seguinte **comando**:

---

<code style="color : red">$ gcc nomeprograma.c -o nomeexecutavel</code>

---

* Explicação:

Comando|Explicação
|---|---|
<code style="color : red">gcc</code>| chamada do programa gcc
<code style="color : red">nomeprograma.c</code>| nome do programa que queremos executar
<code style="color : red">-o</code>| Comando que serve para criar um executor
<code style="color : red">nomeexecutavel</code>| nome do arquivo que irá ser executado

### Agora iremos executar o arquivo executável 

---

<code style="color : lightblue">$ ./nomeexecutavel</code>

---

* Explicação:

Comando|Explicação
|---|---|
<code style="color : lightblue">./</code>| Para rodar o arquivo eecutável
<code style="color : lightblue">nomeexecutavel</code>| nome do arquivo executavel que fizemos