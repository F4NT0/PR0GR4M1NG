[[Página Inicial](../prog_java/home.md)]

# Sobrecarga(Overloading)

* Sobrecarga significa a existência de vários Métodos com o mesmo nome,mas com Parâmetros diferentes
* é um recurso útil e amplamente utilizado nas APIs do Java

```java
//podemos usar em Métodos Construtores
public nomeClasse(){...}
public nomeClasse(int numero){...}
public nomeClasse(int numero,String nome){...}

//podemos usar em Métodos normais
public int numero(int n){...}
public int numero(int n1,int n2){...}
```

# Atributos e Métodos de Classe

## Métodos de Classe

* Um método de Classe é um método que não depende de atributos de um objeto
* Pode ser chamado apenas pelo nome da Classe
* Para isso Funcionar se deve usar a palavra reservada **static** na classe

```java
public class TesteDeClasse{
  //Métodos exemplos
   public static int numero(...){...} 
   public static String nome(...){...}    
}

//como chamar esses Métodos
TesteDeClasse.numero(...);
TesteDeClasse.nome(...);
```

## Atributos de Classe

* Atributos de Classe são atributos armazenados na classe e não nas instâncias(objetos)
* tem Duas Aplicações:
   * Criar constantes, que podem ser acessadas apenas com o nome da Classe
   * Criar atributos que possam ser acessados por qualquer instância da classe
* Para criar uma Constante, se utiliza a palavra reservada **final** e não pode ser mais alterado

```java
//criando uma constante
public static final double valor = 3.5;

//criando um atributo que pode ser acessado em qualquer lugar
//exemplo de uma variavel contador para o método construtor

public class TesteDeClasse{
 private static int contador = 0; //iniciado o contador em zero

 public TesteDeClasse(...){
  contador++; //cada vez que o contrutor for usado, incrementa o contador
  ...
 }
   ...
  public int getContador(){return contador;} //retorna o contador
  //se depois de 10 entradas do construtor, o contador esta em 10
}
```