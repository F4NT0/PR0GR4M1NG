[[Página Inicial](../prog_c/home.md)]

# Trabalhando com Strings em C

A linguagem C não determina um tipo especifico para a manipulação de Strings

* <code style="color : lightgreen">Strings</code> são vetores de caracteres terminados pelo caractere **NULL**

* Existe uma Biblioteca de funções especificas que tratam Strings:

```c
#include <string.h>
```

Essas Funções manipulam as Strings e a percorrem até encontrar o Caractere NULL, onde ele irá parar a interação

* O caractere NULL que utilizamos é o da tabela ASCII mostrado abaixo

```
'\0'
```

#### Declarando e Inicializando uma String

<center>
    Passos de Declaração
</center>

1) Criamos um Vetor que seja o tamanho da nossa String + 1 (onde o +1 é para colocar o caractere NULL)

```c
char frase[6];
```

2) Agora armazenamos a nossa String nesse Vetor

```c
char frase[6] = "fanto";
```

3) Agora podemos pegar cada caractere do Vetor, onde cada posição é uma Letra

```c
#include<stdio.h>

char frase[6] = "fanto";

prinf("%c", frase[0]);
```
 