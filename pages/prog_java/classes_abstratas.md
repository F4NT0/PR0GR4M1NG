[[Página Inicial](../prog_java/home.md)]

# Classes Abstratas
* Classes Abstratas são Classes que passam informações para outras classes
* Uma Classe abstrata **não deve ser Instânciada**,ou seja, chamada como abaixo:

```java
nomeClasse t1 = new nomeClasse(...); //ELA NÃO DEVE SER INSTANCIADA DESSE JEITO
```
* de vez de ser uma classe public, ela possui a palavra reservada **abstract**
* as Classes abstratas possuem um ou mais Métodos abstratos 
* todas as classes que herdarem essa classe abstratas devem reescrever as classes abstratas que foram definidas
* nessas classes que herdarem devem tornar a reescrita do método de forma publica

* **Exemplo:**

```java
abstract class Conta{
 private double saldo;
 
 //getter
 public double getSaldo(){
  return saldo;
 }

 //setter
 public void setSaldo(double saldo){
  this.saldo = saldo;
 }

 //Classe abstrata(deve ter a palavra abstract e terminar com ;)

 public abstract void imprimeExtrato();
}
```

* Agora, criaremos uma Classe normal e chamaremos a classe abstrata
* Para chamarmos uma classe abstrata em outra classe, usamos a palavra reservada **extends**
```java
public class TesteConta extends Conta{
 ...
 //se deve fazer um Override do Método abstrato da Classe Conta:
 @Override
 public void imprimeExtrato(){ //temos que transformar o método abstrato em publico nessa classe
  ...
 } 
 

}

```
