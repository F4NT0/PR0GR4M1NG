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
//tipo de inserção 1
char frase[6] = {'f','a','n','t','o','\0'};

//tipo de inserção 2

char frase[] = "fanto";
```

3) Agora podemos pegar cada caractere do Vetor, onde cada posição é uma Letra

```c
#include<stdio.h>
#include<string.h>

int main()
{
    //Atributos
    char nome[] = "fanto"; //colocamos a string direto no Vetor
    char nome2[6] = {'p','e','d','r','o','\0'};
    int i;
    
    //vamos usar a função strlen() do pacote string.h

    for(i = 0 ; i < strlen(nome) ; i++){
        printf("%c na posicao %u \n", nome[i],i);
    }
}
```

#### Funções Principais da Biblioteca string.h

Existem as Seguintes Funções na Biblioteca:

Função|Descrição
|---|---|
<code style="color : deepskyblue">strcpy(s1,s2)</code>|Copia a String do vetor s1 no vetor s2
<code style="color : deepskyblue">strcat(s1,s2)</code>|Concatena a String do vetor s1 no final da String do vetor s2
<code style="color : deepskyblue">strlen(s1)</code>| apresenta o tamanho do vetor da String
<code style="color : deepskyblue">strcmp(s1,s2)</code>|Retorna 0 se s1 é igual a s2, menor que zero se s1 < s2 e maior que zero se s1 > s2
<code style="color : deepskyblue">strchr(s1,ch)</code>| Retorna o Ponteiro da primeira ocorrencia do caractere na variavel ch na String s1
<code style="color : deepskyblue">strstr(s1,s2)</code>| Retorna o Ponteiro da primeira ocorrencia da String s2 na String s1




 