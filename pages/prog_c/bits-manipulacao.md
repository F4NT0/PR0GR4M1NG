[[Página Inicial](../prog_c/home.md)]

---

# Manipulação de Bits em C

---

Manipulação de Bits é o ato de algoritimicamente manipular Bits ou outros pedaços de dados menores que uma palavra.

---

Precisa se entender o Básico das Seguinte Páginas Já adicionadas:

[Bases Numéricas](../prog_c/bases-numericas.md)

[Usando Bases Numéricas em C](../prog_c/bases-uso.md)

---

## Trabalhando com Bitwise

* <code style="color: gold">Operadores Bitwise</code> são operadores que manipulam individualmente cada bit ou Operandos
* Podem ser usados com os Seguinte valores:
  * <code style="color: lightblue">unsigned int</code>
  * <code style="color: lightblue">unsigned char</code>
  * <code style="color: lightblue">unsigned short int</code>
  * <code style="color: lightblue">unsigned long int</code>
* Iremos usar o Bitwise bit a bit em sua Necessidade, por isso Bitwise

* Existe Dois tipos de Operadores:
  * <code style="color: fuchsia">Operadores Lógicos</code>
  * <code style="color: aquamarine">Operadores de Deslocamento</code>


---

<center>
    <code style="color: fuchsia">Operadores Bitwise Lógicos</code>
</center>

---

Iremos usar os Operadores Lógicos já usuais por nós, só que de vez de verificar um única vez(um único valor) iremos verificar bit a bit de um valor Binário, como iremos mostrar mais a frente

<code style="color : gold">Se é testado Bit á Bit da Direita para a Esquerda</code>


Operadores Lógicos que iremos usar:

* <code style="color: tomato">AND bitwise</code>
  * Sempre trabalhamos com o AND em programação usando dois ampersands(<code style="color: tomato">&&</code>)
  * Como estamos trabalhando com Bitwise, iremos usar um único ampersand(<code style="color: tomato">&</code>)
  * Serve principalmente para verificar se teremos 8 bits no Resultado

* <code style="color: cyan">OR bitwise</code>
  * Sempre trabalhamos com o OR em programação usando duas Barras(<code style="color: cyan">||</code>)
  * Como estamos trabalhando com Bitwise, iremos usar uma única Barra(<code style="color: cyan">|</code>)

* <code style="color: darkorange">XOR bitwise</code>
  * Usamos o Operador <code style="color: darkorange">^</code>
  * Funciona da mesma forma que o OR, mas quando ambos forem 1 ele gera zero

* <code style="color: red">NOT bitwise</code>
  * Usamor o Operador <code style="color: red">~</code>
  * Serve da mesma função que a negação dos Lógico

**Exemplos Lógicos:**

* Valores de Entrada:
    * <code style="color: lightblue">unsigned</code> <code style="color: lightblue">int</code> Valor1 = <code style="color: greenyellow">01001010</code>
    * <code style="color: lightblue">unsigned</code> <code style="color: lightblue">int</code> valor2 = <code style="color: greenyellow">10010010</code>


* Teste do <code style="color: tomato">AND</code>:

Entrada 1 | Entrada 2 | Resultado Lógico
|---|---|---|
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">0</code>

Resultado do <code style="color: tomato">AND bitwise</code>: <code style="color: fuchsia">00000010</code>

* Teste do <code style="color: cyan">OR bitwise</code>:

Entrada 1 | Entrada 2 | Resultado Lógico
|---|---|---|
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>

Resultado do <code style="color : cyan">OR bitwise</code>: <code style="color : fuchsia">11011010</code>

* Teste do <code style="color : darkorange">XOR bitwise</code>:


Entrada 1 | Entrada 2 | Resultado Lógico
|---|---|---|
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">0</code>
<code style="color: greenyellow">1</code>|<code style="color: greenyellow">0</code>|<code style="color: fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color: greenyellow">1</code>|<code style="color: fuchsia">1</code>

Resultado do <code style="color : darkorange">XOR bitwise</code>: <code style="color : fuchsia">11011000</code>

* Teste do <code style="color : red">NOT bitwise</code>:


Entrada 1 | Resultado Lógico
|---|---|
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>


Entrada 2 | Resultado Lógico
|---|---|
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>
<code style="color: greenyellow">1</code>|<code style="color : fuchsia">0</code>
<code style="color: greenyellow">0</code>|<code style="color : fuchsia">1</code>

* Resultados do <code style="color : red">NOT bitwise</code> da Entrada 1 : <code style="color : fuchsia">10110101</code>
* Resultados do <code style="color : red">NOT bitwise</code> da Entrada 2 : <code style="color : fuchsia">10110101</code>


---

<center>
    <code style="color : aquamarine">Operadores de Deslocamento (shifting)</code>
</center>

---

<code style="color : aquamarine">Deslocamento(shifting)</code> deslocam os bits para a <code style="color : gold">Direita</code> ou para a <code style="color : gold">Esquerda</code> dependendo do que se Deseja fazer

Quando é movido os bits podem ficar espaços vazios e se existirem <code style="color : gold">são preenchidos com zeros</code>

Podemos utilizar Deslocamento junto com Operadores Lógicos

## Shift para a Esquerda

Usamos o operador específico <code style="color : aqua"><<</code>

* Argumentos necessários para fazer o Shift:
    * Valor a ser deslocado
    * Quantidades de bits para a esquerda desejados
    * O valor original não é mexido, deve ser criado outra variavel com o Valor

Exemplo:

Pegamos o valor <code style="color : yellow">23</code> 

Armazenamos esse valor Decimal em Hexadecimal em uma Variável:

```c
unsigned int x = 0x17;
```

* O programa irá fazer o Seguinte:
    * Transformar o Valor em Binário
    * Mover o Número de bits para a esquerda pelo número de casas especificado
    * Adicionar zeros nos espaços vazios
    * Armazenar o novo valor na nova Variável

<code style="color : yellow">23</code> em Binário é <code style="color : greenyellow">00010111</code>

Queremos mover <code style="color : gold">Uma</code> casa a esquerda, ele irá pegar bita á bit e empurrar para a esquerda

Vetor Original:

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Vetor fazendo o <code style="color : aquamarine">shifting</code>:

Etapa 1: Será adicionado uma nova posição na Extrema Esquerda

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : red">NULL</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 2: Será movido o valor da Posição 7 para a nova posição

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 3: Será movido o valor da Posição 6 para a Posição 7

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 4: Será movido o valor da Posição 5 para a Posição 6

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 5: Será movido o valor da Posição 4 para a Posição 5

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 6: Será movido o valor da Posição 3 para a Posição 4

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 7: Será movido o valor da Posição 2 para a Posição 3

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|

Etapa 8: Será movido o valor da Posição 1 para a Posição 2

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : greenyellow"></code>|<code style="color : greenyellow">1</code>|

Etapa 9: Será movido o valor da Posição 0 para a Posição 1

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : red">NULL</code>|

Etapa 10: Adicionar Zeros nos Espaços vazios

pos 8|pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|---|
<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|

Valor Armazenado na nova Variável será <code style="color : fuchsia">0x2E</code> em Decimal <code style="color : yellow">46</code>

**Fazendo isso em C**

```c
#include<stdio.h>

unsigned int valor = 0x17; //23 em Decimal
unsigned int novoValor = valor << 1;

printf("Valor antigo: %d\n", valor);
printf("Valor apos shifting: %d\n", novoValor);
```

## Shift para a Direita

Usamos o Operador Especifico <code style="color : aquamarine">>></code>

* Argumentos necessários para fazer o <code style="color : aquamarine">shitf</code>
    * Valor a ser deslocado
    * Quantidades de bits para deslocar
    * O valor original fica inalterado, já que estamos trabalhando com outra Variavel

Exemplo:

Pegamos o valor <code style="color : yellow">46</code>

Armazenamos esse valor Decimal em Hexadecimal

```c
unsigned int valor = 0x2E;
```

* O que o programa irá fazer:
    * Será apagado o Valor da primeira Posição na Extrema Direita(LSB)
    * Ele irá pegar os bits na extrema direita e mover para a Direita bit a bit
    * Irá adicionar Zeros em todos os espaços vazios deixados
    * Irá armazenar o valor na nova variavel

<code style="color : yellow">46</code> em Binário é <code style="color : yellowgreen">00101110</code>

Queremos mover <code style="color : gold">Uma</code> casa a Direita, então ele irá pegar bit á bit e empurrar para a Esquerda

Vetor Original:

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|

Etapa 1: Será Apagado o Valor da Primeira Posição na Extrema Direita

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : red">NULL</code>|

Etapa 2: Será movido o valor da Posição 1 para a Posição 0

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">1</code>|

Etapa 3: Será movido o valor da Posição 2 para a Posição 1

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 4: Será movido o valor da Posição 3 para a Posição 2

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 5: Será movido o valor da Posição 4 para a Posição 3

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">1</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 6: Será movido o valor da Posição 5 para a Posição 4

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow">0</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 7: Será movido o valor da Posição 6 para a 5

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow">0</code>|<code style="color : greenyellow"></code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 8: Será movido o valor da Posição 7 para a Posição 6

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : greenyellow"></code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 9: A posição 7 ficará NULL

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : red">NULL</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

Etapa 10: Será adicionado um zero na posição Vazia

pos 7|pos 6|pos 5|pos 4|pos 3|pos 2|pos 1|pos 0
|---|---|---|---|---|---|---|---|
|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">0</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|<code style="color : aquamarine">1</code>|

O Novo valor que será armazenado na Nova variavel será <code style="color: fuchsia">0x17</code> que em Decimal é <code style="color : yellow">23</code>

**Fazendo isso em C**

```c
#include<stdio.h>

unsigned int valor = 0x2E; //46 em Hexadecimal
unsigned int novoValor = valor >> 1; //mover um bit a direita

printf("Valor Original: %d\n", valor);
printf("Valor Novo: %d\n", novoValor);
```



