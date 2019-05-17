[[Página Inicial](../prog_c/home.md)]


# Estruturas de Dados simples em C

* Existe duas estrutura básicas de dados muitos usadas em c:
    * <code style="color : fuchsia">Vetores</code>
    * <code style="color : lightblue">Matrizes</code>


---

## Vetores em C


Um <code style="color : fuchsia">Vetor</code> é uma estrutura que armazena vários dados de mesmo tipo, ao contrário das variáveis comuns, que só podem armazenar um valor de cada vez

---

* Os elementos são acessados por sua posição dentro do <code style="color : fuchsia">Vetor</code>, onde cada elemento está armazenado em um espaço especifico.

* As posições dos <code style="color : fuchsia">Vetores</code> começa com **Zero** e vai subindo até o **tamanho - 1**


* Visualização:

`| 1 | 2 | 3 | 4 | 5 |`

O valor 1 está na Posição <code style="color : chartreuse">0</code> do Vetor

O valor 2 está na Posição <code style="color : chartreuse">1</code> do Vetor

O valor 3 está na Posição <code style="color : chartreuse">2</code> do Vetor

O valor 4 está na Posição <code style="color : chartreuse">3</code> do Vetor

O valor 5 está na Posição <code style="color : chartreuse">4</code> do Vetor



* Para criar um vetor, faça como a seguinte estrutura:
    * <code style="color : dodgerblue">tipo_estrutura</code> <code style="color : orange">nome_vetor</code> <code style="color : gold ">[numero_elementos]</code>

```c
//exemplo 

int vetor[10];
```

* Para colocar valores em um <code style="color : fuchsia">Vetor</code> existem duas formas:
  * colocando na mão um valor em cada <code style="color : fuchsia">Vetor</code>
  * criando um laço for que irá interagir com cada posição


#### Colocando valores na mão

```c

//vamos colocando valores em cada posição

int vetor[5];

vetor[0] = 1;
vetor[1] = 2;
vetor[2] = 3;
vetor[3] = 4;
vetor[4] = 5;

//Saida: | 1 | 2 | 3 | 4 | 5 |

```

#### Colocando valores com um laço

```c

//Atributo para incrementar o valor
int valor = 1;

// nosso vetor
int vetor[5];

for(int i = 0 ; i < 5 ; i++)
{
    vetor[i] = valor;
    valor++
}

```

---

## Matrizes em C

Uma <code style="color : lightblue">Matriz</code> é um vetor multidimensional, que é um vetor que possui mais do que uma única dimensão

---

* Uma <code style="color : lightblue">Matriz</code> é definida por duas partes principalmente:
  * Primeira parte tu define o Número de <code style="color : gold">Linhas</code>
  * Segunda parte tu define o Número de <code style="color : salmon">Colunas</code>

#### Criando uma Matriz

* Estrutura de construção:
  * <code style="color : dodgerblue">tipo_estrutura </code> <code style="color : orange"> nome_matriz</code> <code style="color : gold">[numero_linhas]</code> <code style="color : salmon">[numero_colunas]</code>

```c
//exemplo

int matriz[3][5];
```

#### Forma da Matriz Visualmente

* Uma matriz, com a do exemplo anterior é apresentado da seguinte forma

```c
int matriz[3][5];
```

* Colocando em forma de Tabela ele fica assim:

Linha/Coluna|Coluna 1 | Coluna 2 | Coluna 3 | Coluna 4 | Coluna 5 
|---|---|---|---|---|---|
Linha 1| Valor 1 |Valor 2|Valor 3|Valor 4|Valor 5
Linha 2|Valor 6|Valor 7|Valor 8|Valor 9|Valor 10
Linha 3|Valor 11|Valor 12|Valor 13|Valor 14|Valor 15


#### Colocando valores manualmente na Matriz

```c

int matriz[3][5];

matriz[0][0] = 1;
matriz[0][1] = 2;
matriz[0][2] = 3;
matriz[0][3] = 4;

matriz[0][4] = 5;
matriz[1][0] = 6;
matriz[1][1] = 7;
matriz[1][2] = 8;
matriz[1][3] = 9;
matriz[1][4] = 10;
matriz[2][0] = 11;
matriz[2][1] = 12;
matriz[2][2] = 13;
matriz[2][3] = 14;
matriz[2][4] = 15;
```

#### Colocando valores com um Laço na Matriz

```c

int matriz[3][5]; //Matriz
int valor = 1 ; //valor a incrementar

for(int i = 0 ; i < 4 ; i++)
{
    for(int j = 0 ; j < 6 ; j++)
    {
        matriz[i][j] = valor;
        valor++;
    }
}
```


