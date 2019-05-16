[[Página Inicial](../prog_java/home.md)]

# Classes Genéricas:

* Programação genérica consiste na criação de estruturas de programação 
* que podem ser usadas com tipos de dados diferentes
* existem estruturas que podem ser instanciadas para coleções de diferentes tipos de dados
* o tipo é verificado durante a compilação do programa 
* evitam a escrita de código repetitivo e sujeito a erros de execução do uso excessivo de conversores de tipo(cast)


### Convenção dos Genéricos:

* usam-se letras maiúsculas individuais para especificar parâmetros de tipo

Nome da Variável de Tipo|Significado
--------|-----------
E | Elemento de uma coleção
K | Chave de um mapa
V | Valor em um mapa
T | Tipo genérico
S,U |Tipos Adicionais

* Parâmetros de tipo são declarados entre **<** e **>** ao lado do nome da classe
* Uma vez declarado, um parâmetro de tipo pode ser usado no lugar de qualquer tipo de dado

### Criando uma classe Genérica que aceite qualquer tipo:

```java
public class Dado<E>{
  private E dado;

public Dado(E d){ dado = d;}

public E getDado() {return dado;}

public void setDado(E dado){this.dado = dado;}

}
```

### Instanciando uma Classe Genérica:

* o tipo E é a especificação do parâmetro de tipo(pode ser qualquer um)

* como instanciar(iniciar a classe em outra classe):

```java

Dado<String> d = new Dado<>("Teste String"); //para usar String
Dado<Objeto> d = new Dado<>(new Objeto(parametro)); //para usar com objetos chamados 

//para chamar o valor gerado, se deve chamar o método getter da classe:

String x = d.getDado(); //para o caso de String
Objeto x = d.getDado(); //para o caso de objetos

```

### Classes de Produto Genérico 

```java
public class Dado<T>{
 private T dado;

public Dado(T dado){this.dado = dado;}

public T getDado(){return dado;}

public void getDado(T dado){this.dado = dado;}

}

```

* Nas classes com o Símbolo T podemos chamar qualquer tipo de dado
* Se deseja usar int ou double, deve chamar as classes onde eles foram definidos

### Instanciando uma classe genérica de qualquer tipo:

```java

Dado<String> dado1 = new Dado<String>("Teste de String");

Dado<Integer> dado2 = new Dado<Integer>(123);

Dado<Double> dado3 = new Dado<Double>(12.3);

```

### Classe com mais de um parâmetro de tipo:

```java

public class Dado<T,U>{
 private T dado1;
 private U dado2;

public Dado(T dado1, U dado2){
 this.dado1 = dado1;
 this.dado2 = dado2; 
}

public T getDado1(){ return dado1; }

public U getDado2(){return dado2; }

public void setDado1(T dado1){this.dado1 = dado1;}

public void setDado2(U dado2){this.dado2 = dado2;}

}

```

* Dessa forma conseguimos utilizar mais de uma variável genérica de uma vez

```java

Dado<Integer,Integer> d1 = new Dado<>(3,4);

Dado<String,String> d2 = new Dado<>("Valor1,Valor2");

Dado<Integer,Double> d3 = new Dado<>(2,3.5);

Dado<String,Integer> d4 = new Dado<>("Teste",3);

``` 