[[Página Inicial](../prog_java/home.md)]

# Interfaces

* Em java, Interfaces são tipos de referência que só podem conter:
    * Constantes
    * Assinaturas de Métodos(Sem implementação)
    * Dois tipos especiais de Métodos(default e static)
* Interfaces definem como se dá a interação mas sem especificar a implementação
* Colocamos o nome dos Métodos na classe interface e alterar em cada outra classe implementada
* para implementar a classe interface usamos a palavra reservada **implements**
* Uma classe normal pode ter implementado quantas classes de interface que quiser
```java
//classe interface:

interface Imprimivel
{
  void imprimir();
}

//conectando a classe interface em outra classe

public class TesteDeClasse implements Imprimivel{
 ...
 //alterando o Método definido na Classe Interface
 public void imprimir(){
  System.out.println("Saida de texto"); //pode ser o que quiser aqui
  }
}
```

# Interfaces da API java
### Comparadores
* A API java utiliza extensivamente interfaces em diversas situações
* Usei duas Interfaces dela até agora: a **Comparable** e a **Comparator**
```java
//Classe Comparable:
public interface Comparable<T>{
 public int compareTo(T other); //irá comparar um com outro
}

//Classe comparator:
public interface Comparator<T>{
 public int compare(T o1, T o2); //irá pegar dois e comparar um com o outro
}
```
* Na classe que implementar a classe interface comparable será capaz de realizar comparações entre elementos
* como na matéria sobre Genéricos: a construção **<T>** permite qualquer tipo de dado utilizado
 
# Ordenação

* para fazer ordenações, iremos utilizar as Expressões lambdas(desde o java 8)
* expressões lambdas são funções anonimas(será explicado mais tarde)
* abaixo se encontra uma expressão lambda dentro de um método sort() de ArrayList:
```java
nomeArray.sort((nomeClasse c1, nomeClasse c2) -> c1.metodoUsadoParaOrdenar().compareto(c2.metodoUsadoParaOrdenar()));
```
**OU**
```java
nomeArray.sort((nomeClasse c1, nomeClasse c2) -> {
  ... código de ordenação ...
}
```
* **Exemplo:**
```java
//classe de teste:

public class TesteClasse{
 private int valor;
  ...
 public int getValor(){return valor;}
  ...
}

//criando um ArrayList

ArrayList<TesteClasse> vetor = new ArrayList<TesteClasse>();

TesteClasse t1 = new TesteClasse(...);
TesteClasse t2 = new TesteClasse(...);
vetor.add(t1);
vetor.add(t2);

// criando um método onde compara o valor de cada objeto criado da classe TesteClasse

public void ordenaValor(){
 vetor.sort((TesteClasse t1, TesteClasse t2) -> t1.getValor().compareTo(t2.getValor()));
} 
```

# Métodos static em interfaces

* As interfaces normalmente não implementam métodos,mas é conveniente haver a implementação de alguns métodos
* A interface comparator possui um método static chamado comparing.
* o método comparing tem acesso a função que retorna o critério de comparação
* usando a ideia anterior mas utilizando um ordenador com esse método estatico
```java
//classe de teste:

public class TesteClasse{
 private int valor;
  ...
 public int getValor(){return valor;}
  ...
}

//criando um ArrayList

ArrayList<TesteClasse> vetor = new ArrayList<TesteClasse>();

TesteClasse t1 = new TesteClasse(...);
TesteClasse t2 = new TesteClasse(...);
vetor.add(t1);
vetor.add(t2);

// Método de Ordenação usando o Método static da classe de interface
// o método comparing() é um método static da Classe interface Comparator

public void ordenaValor(){
 vetor.sort(Comparator.comparing(a -> a.getValor()));
 //o parâmetro a é a entrada dessa função anônima
} 
```
* Referência de Método

* se desejarmos ordenar o ArrayList pelo valor usando uma referência de Método
```java
vetor.sort(Comparator.comparing(TesteClasse::getValor));
```
* se desejarmos ordenar o ArrayList para inverter o critério de ordenação]
```java
vetor.sort(Comparator.comparing(TesteClasse::getValor).reversed());
```
* se Desejarmos usar mais de um critério de ordenação ao mesmo tempo
* Usamos o método thenComparing
```java
//se na Classe TesteClasse tivesse dois metodos:
public int getValor(){...}
public String getNome(){...}

//utilizando a ordenação:
 vetor.sort(Comparator.comparing(TesteClasse::getValor).thenComparing(TesteClasse::getNome));
```

# Métodos default em interfaces

* Há um terceiro tipo de método disponivel em Interfaces, o **Método Default**
* Foi criado para que fosse possivel estender uma interface já existente
* Se estende uma interface existente sem a necessidade de alterar todas as classes que a implementam
* Os métodos default exigem que já exista uma chamada de método anterior
* Nós vimos um método default na ultima parte da matéria que é o método thenComparing() da Classe Interface
```java
vetor.sort(Comparator.comparing(TesteClasse::getValor).thenComparing(TesteClasse::getNome));
//o método thenComparing necessita que tenha sido feito a chamada de método do comparing()
```