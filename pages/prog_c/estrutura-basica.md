[[Página Inicial](../prog_c/home.md)]

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

