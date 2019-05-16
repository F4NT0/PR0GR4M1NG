[[Página Inicial](../prog_java/home.md)]

# Polimorfismo

* **Polimorfismo** é a capacidade de assumir formas diferentes
* Uma linguagem orientada a objetos deve permitir a utilização de **variáveis polimórficas**
* Existem dois tipos de Polimorfismo:
    * Polimorfismo Estático ou Sobrecarga
    * Polimorfismo Dinâmico ou Sobreposição

* **Polimorfismo Estático** se dá quando temos a mesma operação implementada várias vezes na mesma classe
* A escolha de qual operação será chamada depende da assinatura dos métodos sobrecarregados
* Foram feitos exemplos sobre Sobrecarga na Parte de [Interface](https://github.com/F4NT0/Java_Basics/wiki/interface)

```java
 //exemplo com um construtor:
 
 public TesteClasse(){...}
 public TesteClasse(int n){...}
//isso se pode fazer devido ao polimorfismo
```

* **Polimorfismo Dinâmico** acontece na herança,quando a SubClasse sobrepõe o método original
* Agora o método escolhido se dá em tempo de execução e não mais em tempo de compilação
* A escolha de qual método será chamado depende do tipo do objeto que recebe a mensagem
* Também foi apresentado na Parte sobre [Herança](https://github.com/F4NT0/Java_Basics/wiki/heranca)
* Também foi apresentado na Parte sobre [Classes Abstratas](https://github.com/F4NT0/Java_Basics/wiki/abstract)

```java
//esse caso é quando fazemos Override de métodos nas SubClasses
//exemplo feito até agora: toString()

@Override //foi sobreposto o método nesta classe
public String toString(){...}

//outro exemplo é fazer sobreposição devido a classe abstrata

// Na classe Abstrata:
public abstract String nomeMetod();

//na classe conectada a Classe Abstrata:
public String nomeMetod(){...}
```

