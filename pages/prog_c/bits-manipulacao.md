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
    <code style="color : aquamarine">Operadores de Deslocamento</code>
</center>

---




