[[Página Inicial](../prog_c/home.md)]

---

# Revisão de Bases Numéricas

---

### Revisando Bases Numéricas

* Dados numéricos podem ser representados através de várias bases:
  * Decimal
  * Hexadecimal
  * Binário

* Uma base numérica é apenas uma forma de interpretar os dados, não mudando o valor armazenado
* Todo número apresentado como Binário é o mesmo valor como Decimal, sem sofrer mudanças bruscas:
* 0001 é o mesmo que 1 só que binário

#### Decimal

* Bom para humanos, péssimos para Desenvolvedores
* Decimal é muito ruim de converter para outros valores, então nãoé eficiente para Desenvolvimento.

Decimal é bom para <code style="color : green">Humanos</code>, Péssimo para <code style="color : yellow">Desenvolvedores</code>.

#### Binários de Base 2

Binário é bom para <code style="color : lightblue">Computadores</code> e péssimo para <code style="color : red">Todo Mundo</code>

#### Hexadecimal de Base 16

Hexadecimal oferece um equilibrio entre a facilidade do decimal e a visão direta do Binário. Ele é excelente para guardar números muito grandes

---

## Manipulação de Binários

Podemos transformar valores Binários em Decimais, mas para o caso de manipular bits não serve muito, mas é sempre bom relembrar:

**Transformar de Binário para Decimal**

Pegamos de Exemplo o valor em Binário <code style="color : lightblue">1011</code>:

Passos:

1. Pegamos cada Dígito do valor e númeramos a sua posição começando da <code style="color : greenyellow">Direita</code> para a <code style="color : greenyellow">Esquerda</code>
2. Pegamos cada posição e colocamos o 2 como Base e a Posição como Expoente da Exponenciação(<code style="color : red">2^Posição</code>)
3. Multiplicamos o Dígito da Posição com a Exponenciação e armazenamos o valor
4. Depois de ter sido feito em todas as posições, somamos o valor armazenado de cada posição e temos o valor em Decimal do Binário

Exemplo:

* Valor = <code style="color : lightblue">1011</code>

* Colocamos em um Vetor:

Posição 3|Posição 2|Posição 1|Posição 0
|---|---|---|---|
<code style="color : lightblue">1</code>|<code style="color : lightblue">0</code>|<code style="color : lightblue">1</code>|<code style="color : lightblue">1</code>


* Cálculo Feito:

Posição|Dígito|Cálculo|Resposta da Posição
|---|---|---|---|
<code style="color : gold">0</code>|<code style="color : lightblue">1</code>| 2^0 * 1| <code style="color : red">1</code>
<code style="color : gold">1</code>|<code style="color : lightblue">1</code>| 2^1 * 1| <code style="color : red">2</code>
<code style="color : gold">2</code>|<code style="color : lightblue">0</code>| 2^2 * 0| <code style="color : red">0</code>
<code style="color : gold">3</code>|<code style="color : lightblue">1</code>| 2^3 * 1| <code style="color : red">8</code>

* Somamos Tudo : <code style="color : green">1 + 2 + 0 + 8 = 11</code>

* Resultado = <code style="color : lightblue">1011</code> = <code style="color : green">11</code>

**Transformar Decimal em Bináio**

Este é um pouco chatinho de Fazer, um pouco mais do que o Anterior

Vamos pegar por Exemplo o Valor Decimal <code style="color : lightblue">11</code>


Passos: 


1. Transformar um valor Decimal em Binário envolve Divisões Sucessivas
2. Devemos fazer várias <code style="color : gold">Divisões por 2</code> Até não poder ser mais dividido.
3. Iremos pegar os Restos de Cada Divisão de <code style="color : gold">Baixo para cima</code>
4. Concatenando esses Dígitos dos Restos teremos nosso Valor em Binário

Exemplo:

Divisão|Dividendo|Resto da Divisão|Construção do Binário Passo-a-Passo
|---|---|---|---|
11 / 2|5|1|<code style="color : lightblue">1</code>
5 / 2|2|1|<code style="color : lightblue">11</code>
2 / 2|1|0|<code style="color : lightblue">011</code>
1 / 2|0|1|<code style="color : lightblue">1011</code>

Foi sendo colocado o novo dígito do Resto da Divisão a Esquerda do Valor anterior

Resultado: <code style="color : lightblue">11</code> = <code style="color : lightblue">1011</code>



### Bits Significativos dos Binários

Iremos trabalhar com algo chamado Bits significativos, que nos auxiliam a entender melhor o que o Binário representa como Número, onde existe dois Segmentos:

<center>
    <code style="color : yellowgreen">LSB</code>
</center>

* <code style="color : yellowgreen">LSB</code> significa <code style="color : yellowgreen">L</code>east <code style="color : yellowgreen">S</code>ignificant <code style="color : yellowgreen">B</code>it
* Ele respresenta o Bit na extrema Direita do Binário, onde ele interfere menos no valor total do Binário em Si
* Com ele podemos por exemplo saber se o Valor em Binário é Par ou Impar

---

<center>
    100<code style="color : red">1</code>
</center>

---

<center>
    <code style="color : yellowgreen">MSB</code>
</center>

* <code style="color : yellowgreen">MSB</code> significa <code style="color : yellowgreen">M</code>ost <code style="color : yellowgreen">S</code>ignificant <code style="color : yellowgreen">B</code>it
* Ele respresenta o Bit na extrema Esquerda do Binário, onde ele Define o valor total do Binário em Si
* Com ele podemos por exemplo saber se o Valor em Binário é <code style="color : gold">Negativo</code>(<code style="color : red">1</code>) ou <code style="color : gold">Positivo</code>(<code style="color : green">0</code>) 

---

<center>
    <code style="color : red">1</code>001
</center>

---


---

## Mexendo com Hexadecimal de Base 16

* Hexadecimal Oferece um Equilibrio entre a Facilidade do Decimal e a Visão direta do Binário

* Hexadecimal se mantem com Dígitos Decimais até o Número 9, Depois será Transferidos para Letras que terão o Significado daquele Número em Decimal de Dois Digitos.

* Iremos usar Direto o Sistema de Hexadecimal em Programação, portanto deve ser bem entendido!

* Como estamos falando de <code style="color : gold">Base 16</code> temos que os valores Hexadecimais irão de <code style="color : gold">0 á 15</code> como mostrado abaixo:

<code style="color : fuchsia">0</code> <code style="color : fuchsia">1</code> <code style="color : fuchsia">2</code> <code style="color : fuchsia">3</code> <code style="color : fuchsia">4</code> <code style="color : fuchsia">5</code> <code style="color : fuchsia">6</code> <code style="color : fuchsia">7</code> <code style="color : fuchsia">8</code> <code style="color : fuchsia">9</code> <code style="color : fuchsia">A</code> <code style="color : fuchsia">B</code> <code style="color : fuchsia">C</code> <code style="color : fuchsia">D</code> <code style="color : fuchsia">E</code>

* Base 16 é uma Potência de 2 elevado na Quarta Potência(<code style="color : fuchsia">2^4</code>), portanto a Conversão entre BInário e Hexadecimal é feita de <code style="color : gold">4 em 4 Bits</code>:

<code style="color : "></code>

Decimal|Binário|Hexadecimal
|---|---|---|
<code style="color : yellow">0</code>| <code style="color : greenyellow">0000</code>|  <code style="color : fuchsia">0</code>
<code style="color : yellow">1</code>| <code style="color : greenyellow">0001</code>|  <code style="color : fuchsia">1</code>
<code style="color : yellow">2</code>| <code style="color : greenyellow">0010</code>|  <code style="color : fuchsia">2</code>
<code style="color : yellow">3</code>| <code style="color : greenyellow">0011</code>|  <code style="color : fuchsia">3</code>
<code style="color : yellow">4</code>| <code style="color : greenyellow">0100</code>|  <code style="color : fuchsia">4</code>
<code style="color : yellow">5</code>| <code style="color : greenyellow">0101</code>|  <code style="color : fuchsia">5</code>
<code style="color : yellow">6</code>| <code style="color : greenyellow">0110</code>|  <code style="color : fuchsia">6</code>
<code style="color : yellow">7</code>| <code style="color : greenyellow">0111</code>|  <code style="color : fuchsia">7</code>
<code style="color : yellow">8</code>| <code style="color : greenyellow">1000</code>|  <code style="color : fuchsia">8</code>
<code style="color : yellow">9</code>| <code style="color : greenyellow">1001</code>|  <code style="color : fuchsia">9</code>
<code style="color : yellow">10</code>| <code style="color : greenyellow">1010</code>|  <code style="color : fuchsia">A</code>
<code style="color : yellow">11</code>| <code style="color : greenyellow">1011</code>|  <code style="color : fuchsia">B</code>
<code style="color : yellow">12</code>| <code style="color : greenyellow">1100</code>|  <code style="color : fuchsia">C</code>
<code style="color : yellow">13</code>| <code style="color : greenyellow">1101</code>|  <code style="color : fuchsia">D</code>
<code style="color : yellow">14</code>| <code style="color : greenyellow">1110</code>|  <code style="color : fuchsia">E</code>
<code style="color : yellow">15</code>| <code style="color : greenyellow">1111</code>|  <code style="color : fuchsia">F</code>

**Transformação de Binário em Hexadecimal**

Se quiser transformar um Binário muito grande em Hexadecimal para diminuir o tamanho armazenado, iremos fazer o seguinte:

Passos:

1. Pegue o Número Binário desejado
2. Separe o valor de 4 em 4 bits começando pelo Bit mais Significativo(Extrema Esquerda)
3. Transformamos o Valor desses 4 bits em seu Valor Hexadecimal Referente
4. Depois é só juntar todos os valores Concatenados e Teremos nosso valor Hexadecimal Referente

Exemplo:

Valor em Binário: <code style="color : greenyellow">11110000101011100001010011101100</code>

Dividimos os valores em 4 em 4 bits, começando pelo Bit mais Significativo(Extrema Esquerda)

<code style="color : greenyellow">1111</code> <code style="color : greenyellow">0000</code> <code style="color : greenyellow">1010</code> <code style="color : greenyellow">1110</code> <code style="color : greenyellow">0001</code> <code style="color : greenyellow">0100</code> <code style="color : greenyellow">1110</code> <code style="color : greenyellow">1100</code>

Agora pegamos Esses valores e Transformamos em Hexadecimal, como na Tabela Abaixo:

Binário|Hexadecimal
|---|---|
<code style="color : greenyellow">1111</code>|<code style="color : fuchsia">F</code>
<code style="color : greenyellow">0000</code>|<code style="color : fuchsia">0</code>
<code style="color : greenyellow">1010</code>|<code style="color : fuchsia">A</code>
<code style="color : greenyellow">1110</code>|<code style="color : fuchsia">E</code>
<code style="color : greenyellow">0001</code>|<code style="color : fuchsia">1</code>
<code style="color : greenyellow">0100</code>|<code style="color : fuchsia">4</code>
<code style="color : greenyellow">1110</code>|<code style="color : fuchsia">E</code>
<code style="color : greenyellow">1100</code>|<code style="color : fuchsia">C</code>

Resultado: O valor em Hexadecimal do Valor em Binário é <code style="color : fuchsia">F0AE14EC</code>

Com isso Conseguimos armazenar valores grandes em Binário em um Valor menor em Hexadecimal


**Convertendo Hexadecimal para Decimal**

Devemos seguir os seguintes passos para fazer com que o Valor em Hexa fique exatamente o valor em Decimal

Passos:

1. Pegamos o valor em Hexadecimal e Dividimos ele em Posições, começando da Direita para a Esquerda
2. Cada posição é o <code style="color : gold">Expoente</code> da Exponenciação de <code style="color : gold">Base 16</code>
3. Após colocar direitinho as Exponenciações, devemos multiplicar com o valor que está dentro da Posição,onde se for uma letra deve ser transformado em seu Número especifico
4. Após feitos os calculos de cada Posição, se soma todos os valores e dará o resultado desejado

Exemplo:

Valor Desejado = <code style="color : fuchsia">F0AE14EC</code>

Colocando em suas Posições Específicas:


Posição 7|Posição 6|Posição 5|Posição 4|Posição 3|Posição 2|Posição 1|Posição 0
|---|---|---|---|---|---|---|---|
<code style="color : fuchsia">F</code>|<code style="color : fuchsia">0</code>|<code style="color : fuchsia">A</code>|<code style="color : fuchsia">E</code>|<code style="color : fuchsia">1</code>|<code style="color : fuchsia">4</code>|<code style="color : fuchsia">E</code>|<code style="color : fuchsia">C</code>

Agora iremos colocar todas as posições em seus calculos devidos

Posição|Valor da Posição|Cálculo|Resultado da Posição
|---|---|---|---|
0|<code style="color : fuchsia">C</code>|<code style="color : fuchsia">16^0 + 12(C)</code>|<code style="color : gold">12</code>
1|<code style="color : fuchsia">E</code>|<code style="color : fuchsia">16^1 + 14(E)</code>|<code style="color : gold">224</code>
2|<code style="color : fuchsia">4</code>|<code style="color : fuchsia">16^2 + 4</code>|<code style="color : gold">1.024</code>
3|<code style="color : fuchsia">1</code>|<code style="color : fuchsia">16^3 + 1</code>|<code style="color : gold">4.096</code>
4|<code style="color : fuchsia">E</code>|<code style="color : fuchsia">16^4 + 14(E)</code>|<code style="color : gold">917.504</code>
5|<code style="color : fuchsia">A</code>|<code style="color : fuchsia">16^5 + 10(A)</code>|<code style="color : gold">10.485.760</code>
6|<code style="color : fuchsia">0</code>|<code style="color : fuchsia">16^6 + 0</code>|<code style="color : gold">0</code>
7|<code style="color : fuchsia">F</code>|<code style="color : fuchsia">16^7 + 15(F)</code>|<code style="color : gold">4.026.531.840</code>

Agora iremos somar todos os valores de todas as posições e teremos o valor em Decimal:

<code style="color : gold">12</code> + <code style="color : gold">224</code> + <code style="color : gold">1.024</code> + <code style="color : gold">4.096</code> + <code style="color : gold">917.504</code> + <code style="color : gold">10.485.760</code> + <code style="color : gold">0</code> + <code style="color : gold">4.026.531.840</code> = <code style="color : gold">4.037.940.460</code>

Resultado: <code style="color : gold">4.037.940.460</code>

---