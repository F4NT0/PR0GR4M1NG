[[Página Inicial](../prog_c/home.md)]

# Mexendo com Structs(Registros)

<code style="color : gold">Struct</code> é uma estrutura que permite o armazenamento de diversos tipos de dados diferentes na mesma estrutura.

Structs ajudam muito na capacidade de um programa na manipulação de dados, onde podemos colocar varios dados em uma unica estrutura e chama-los quando quisermos.

Aqui temos um estrutura basica de um Struct:

```c

struct nome_struct{
    tipo_variavel nome_variavel1;
    tipo_variavel nome_variavel2;
    ...
}

```

Com os Structs iremos facilmente ter varios tipos de dados a disposição quando quisermos.


#### Criando uma Struct de Exemplo

Iremos construir uma Struct com dados essenciais de uma Pessoa Física:

```c
struct Pessoa{
    int idade;
    char nome[30];
    float tamanho;
}
```

Agora iremos criar uma pessoa encima desse Struct:

```c
struct Pessoa Pedro;
```

Agora que criamos a Struct do Pedro encima da Struct Básica podemos adicionar valores nela:

```c

//Criando uma String com o nome completo do Pedro

char nome_completo[] = "Pedro da Silva";

//Criando valores para a Struct

Pedro.idade = 20; //Colocando valor na idade
strcpy(nome_completo,Pedro.nome); //Pegamos a String criara de colocamos no Struct
Pedro.tamanho = 1.90;
```

Agora se quisermos pegar os valores de um Struct colocamos o Seguinte:

```c
#include<stdio.h>

printf("Nome completo do Pedro: %s", Pedro.nome);
printf("Idade do Pedro: %d", Pedro.idade);
printf("Tamanho total do Pedro: %f", Pedro.tamanho);
```

### Construindo valores em um Struct com Scanf()

* Eis um exemplo completo de como usar Struct usando entrada de usuario:

```c
#include<stdio.h> 
// I/O do programa
#include<string.h> 
// Tratamento de Strings

//TESTE COM STRUCTS


//Criação de um Struct de Pessoa, fica fora da função Main

struct Pessoa{
    int idade;
    char nome[100];
    float tamanho;
};

int main(){

//Chamada do Struct na Pessoa Pedro

struct Pessoa Pedro;

// Entrada de Valores pelo Terminal


//Como pegar a idade
int idade;
printf("Qual a idade do Pedro? ");
scanf("%d", &idade);
Pedro.idade = idade;


//Como pegar uma String com C

char nome[100]; //Criamos um vetor auxiliar

printf("Qual o Nome Completo do Pedro? ");
scanf(" %[^\n]s", nome); // [^\n] serve para evitar que ele pule com espaços as palavras
strcpy(Pedro.nome,nome);


//Como pegar o tamanho 
float tamanho;
printf("Qual o Tamanho do Pedro? ");
scanf("%f", &tamanho);
Pedro.tamanho = tamanho;

//Saida de Valores

printf("\nNome Completo: %s\n", Pedro.nome);
printf("Idade: %d\n", Pedro.idade);
printf("Tamanho: %1.2f\n", Pedro.tamanho);


}
```

