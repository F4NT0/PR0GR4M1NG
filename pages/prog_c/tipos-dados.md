[[Página Inicial](../prog_c/home.md)]

---

## Tipos de Dados em C

---

Existem os seguintes tipos de dados com C

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
 <code style="color : red">Hexadecimal sem sinal(minusculas)</code>|<code style="color : red">%x</code>
 <code style="color : tomato">Hexadecimal sem sinal(maiusculas)</code>|<code style="color : tomato">%X</code>

---

## Exemplos

---

```c

//TESTES DE VARIAVEIS COM OS TIPOS DE DADOS PRIMITIVOS

short int max_short_int = 32767; //tamanho maximo de um inteiro com sinal (32Kb)

signed short int min_short_int= -32768; //tamanho minimo de um inteiro curto com sinal (32Kb)

unsigned short int max_short_un_int = 65535; //tamanho maximo de um inteiro curto sem sinal (64Kb)

unsigned int max_un_int= 4294967295; //tamanho maximo de um inteiro sem sinal(4Gb) depois ele não aceita mais

int max_int = 2147483647; //tamanho maximo de um inteiro (2Gb)

int min_int = -2147483648; //tamanho minimo de um inteiro (2Gb)

float pontoflutuante = 2.1234567; // float possui 7 casas de precisão

double pontoflutuante2 = 2.123456789123456; // double possui 15 casas de precisão

```

```c

// TESTE DE SAIDA DESSAS VARIAVEIS CRIADAS

printf("Maximo inteiro curto: %d\n", max_short_int);
    
printf("Minimo inteiro curto com sinal: %d\n", min_short_int);
    
printf("Maximo inteiro curto sem sinal: %d\n", max_short_un_int);

printf("Maximo inteiro sem sinal: %d\n", max_un_int);

printf("Maximo inteiro com sinal: %d\n", max_int);
    
printf("Minimo inteiro com sinal: %d\n", min_int);

printf("Valor de Ponto Flutuante: %f\n", pontoflutuante);
    
printf("Valor de Ponto Flutuante Double: %1.15f\n", pontoflutuante2); //determinar o numero total de casas no double

```

---

## SOBRE STRINGS E CHARS SERÁ DITO MAIS ADIANTE

---

