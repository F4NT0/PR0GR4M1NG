[[Página Inicial](../prog_c/home.md)]

---

## Tipos de modificadores de informações

---

Existem os seguintes tipos de estrutura de dados com C

* <code style="color : lightblue">Int</code>(conhecido como Inteiro)
* <code style="color : fuchsia">Float</code>(Conhecido como Ponto Flutuante)
* <code style="color : blue">double</code>(Tambem conhecido como ponto flutuante)
* <code style="color : gold">Char</code>(Conhecido como Caractere)
* <code style="color : orange">Vetores de Chars(String)</code>(Conhecido como Arrays de Chars)

Podemos usar modificadores que auxiliam na definição do tamanho de cada tipo de dado, onde:
* <code style="color : springgreen">short</code> = é a forma curta do dado, onde não apresenta todo o valor
* <code style="color : red">long</code> = é a forma completa do valor 
* <code style="color : cyan">unsigned</code> = são valores sem sinal
* <code style="color : deeppink">signed</code> = são valores com sinal

Agora a tabela abaixo diz o tamanho de cada tipo de formato

Tipo de dado|Número de Bytes|Número de Bits|Intervalo de Tamanho
|---|---|---|---|
<code style="color : springgreen">short</code> <code style="color : lightblue">Int</code>|2|16|-32.768 á 32.767 (32 Kb)
<code style="color : cyan">unsigned</code>  <code style="color : springgreen">short</code> <code style="color : lightblue">Int</code>|2|16| 0 á 65.535 (64 Kb)
<code style="color : cyan">unsigned</code> <code style="color : lightblue">Int</code>|4|32|0 á 4.294.967.295 (4 Gb)
<code style="color : lightblue">Int</code>|4|32|-2.147.483.648 á 2.147.483.647 (2 Gb)
<code style="color : red">long</code> <code style="color : lightblue">Int</code>|4|32|
<code style="color : deeppink">signed</code> <code style="color : gold">Char</code>|1|8| 0 á 255
<code style="color : cyan">unsigned</code> <code style="color : gold">Char</code>|1|8| 0 á 255
<code style="color : fuchsia">Float</code>|4|32| 7 casas de precisão
<code style="color : blue">double</code>|8|64|15 casas de precisão

se deseja verificar o tamanho de uma variável, utilize a função `sizeOf` retorna o tamanho em Bytes

---

## Estrutura Básica de um programa C

---

A linguagem C oferece um biblioteca básica de funções padrões que utilizamos direto.

Todo o arquivo C tem um _header_ onde são importados as bibliotecas básicas utilizadas em C, como mostrado abaixo:

```c
#include<stdio.h> 
//a biblioteca <stdio.h> possui várias funções de entrada e saída de C
#include<math.h> 
//a biblioteca <math.h> possui as funções matemáticas
#include<stdlib.h> 
//a biblioteca <stdlib.h> possui funções básicas de C
#include<string.h> 
//a biblioteca <string.h> se pode usar strings
```

A biblioteca <code style="color: red">stdio.h</code> é a principal biblioteca básica de C que usamos em todos os exemplos, nela existem funções que são utilizadas para fazer a <code style="color : yellow">Entrada</code> e <code style="color: yellow">Saída</code> de informações em nosso Documento em C

Alguns exemplos de Funções muito utilizadas

```c
scanf() //Função para entrada de informações no programa
printf() //Função de Saída de Dados do programa
```

Um exemplo de programa em C usando essas funções

```c
#include<stdio.h>

//Atributos
int i;

scanf("%d", &i); 
// %d significa que vai entrar um dado inteiro
// &i siginifica que o valor vai entrar e ser armazenado no atributo i

printf("%d", i); //irá sair o valor do atributo i como um valor inteiro
```

---

## Tratando os tipos de dados em C

---

Para lidar com esses tipos de estruturas, tem um comando especifico para dizer que tipo de I/O (Entrada(In)/Saida(Out)) estamos trabalhando como na tabela abaixo

Nome do tipo de dado|Comando de I/O
|---|---|
<code style="color : lightblue">Inteiro com Sinal</code>| <code style="color : lightblue">%d</code>
<code style="color : lightgreen">Inteiro sem Sinal</code>|<code style="color : lightgreen">%u</code>
 <code style="color : fuchsia">Float</code>| <code style="color : fuchsia">%f</code>
 <code style="color : gold">Char</code>|<code style="color : gold">%c</code>
 <code style="color : orange">Vetores de Chars(String)</code>|<code style="color : orange">%s</code>
