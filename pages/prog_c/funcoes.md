[[Página Inicial](../prog_c/home.md)]

# Mexendo com Funções em C

Funções são importantes em Programação Estruturadas, pois permitem a reutilização de código, chamando a função com o bloco de código desejado.

Uma Função pode ser chamada quantas vezes forem necessitadas

#### Conceituando

<code style="color : lightblue">Funções</code> são trechos(blocos) de código que diminuem a complexidade de um programa ou evitam repetição excessiva de determinada parte do aplicativo.

<code style="color : greenyellow">Modularização</code> se aplica ás linguagens estruturadas, em que as Funções são elementos fundamentais para a construção de blocos ordenados e organizados

#### Construção geral de uma Função

```
<tipo de retorno> nome(parametros)
{
    corpo da função
    retorno(não obrigatório)
}
```
* **Tipo de Retorno** determina qual tipo de valores que se deseja que saia da Função, sendo os tipos de dados primitivos explicados [Aqui](../prog_c/estrutura.md)

* **nome** é o nome da Função, onde iremos utilizar ela para chamar a função em outros programas e arquivos

* **Parametros** são os valores de entrada que iremos precisar para o bloco de código interno da Função

* **corpo da função** é todo o código interno da Função usado, sendo o que quisermos que a função faça
* **retorno** é a saida da função, não é obirgatório mas existem muitas funções que se precisa ter uma Saida para outros blocos de códigos

### Exemplo de Funções

* A principal função dos arquivos C é a função <code style="color : gold">main()</code>, que é a função que iremos utilizar para compilar nossos Códigos em C

```c
int main(){
    //bloco de código
}
```

* Aqui uma Função de Cálculos Matemáticos e sua Biblioteca Necessária

```c
#include <math.h>

int multiplica(int a,int b){
    int resultado;
    resultado = a * b;
    return resultado;
}
```

* Agora iremos chamar a função multiplica() dentro da função <code style="color : gold">main()</code>
  * Todas as funções que forem ser usadas devem ser elaboradas e organizadas antes da Função main para que funcionem

```c
#include<stdio.h>
#include<math.h>

int multiplica(int a,int b){
    int resultado;
    resultado = a * b;
    return resultado;
}


int main(){
    int a,b;
    a = 1;
    b = 2;
    printf("%d" , multiplica(a,b));
}

```

* Se quisermos construir uma Função depois do <code style="color : gold">main()</code>, devemos criar um prototipo da Função que será criada depois, como abaixo:

```c
int multiplicacao(int a,int b);
```

* EXEMPLO COMPLETO

```c
#include<stdio.h>


//Protótipos

int multiplicacao(int a, int b);

//Função Main

int main(){
    //Variaveis
    int a,b,mult;
    
    //Trazendo valor externo ás variaveis
    printf("Digite o Valor 1: ");
    scanf("%d", &a);
    printf("Digite o Valor 2: ");
    scanf("%d", &b);

    //Adicionando os valores na Função multiplicacao()
    int mult = multiplicacao(a,b);

    printf("\n");
    printf("Saida da Multiplicacao %d",mult);
}

// Criando agora a Função multiplicacao

int multiplicacao(int a , int b){
    int valor;
    valor = a * b;
    return valor;
}
```