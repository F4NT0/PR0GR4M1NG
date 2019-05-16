[[Página Inicial](../prog_java/home.md)]

# Capturando Exceções

Para capturar e tratar exceções, utiliza-se o bloco de comandos **try...catch...finally** como abaixo:

```java
try
{
 //código que pode gerar exceções
}
catch(Exception e)
{
 //código que trata exceção
}
finally
{
 //tratamento geral
}
```

* **try{}**: Estão colocados os comandos que podem provocar o lançamento de uma exceção.
* **catch{}**: É o bloco que trata das exceções do try, podem ser capturados em mais de um catch ao mesmo tempo.
* **finally()**: É onde contém o código a ser executado, independente dos outros comandos, é opcional, mas quando presente é sempre executado, não importa o que aconteca no código.

## Como funciona a Captura

A captura funciona da seguinte forma: Uma vez lançada, uma exceção capturada no bloco try procura por uma cláusula catch capaz de referência-la e tratá-la. Se não houver, o programa irá parar com erro.

Uma cláusula catch pode referenciar qualquer exceção do tipo que declara ou derivadas.Além disso, um único bloco try pode ter várias cláusulas catch. Nesse caso a ordem em que as cláusulas catch aparecem importa: as exceções mais genéricas devem ser tratadas após as mais específicas.

Irei mostrar como o Código abaixo funciona:

```java
try{
 //Faz algo que pode fazer as exceções X,Y,Z
}
catch (X e){
 //lida com a exceção e de X
}
catch (Y e){
//lida com a exceção e de Y
}
catch (Z e){
//lida com a exceção e de Z
}
finally{
 //sempre vai rodar no fim
}
```  
Então o seguinte código funciona assim:
![](https://www.protechtraining.com/static/bookshelf/java_fundamentals_tutorial/images/TryCatchFinally.png.pagespeed.ce.Yp3kGa30QM.png)

A exceção para no exato ponto de origem da exceção, a máquina virtual procura pelo primeiro bloco catch que se encaixa com a exceção, se encontrar ele trata a exceção e vai para o finally ou ele vai direto para o finally.

É uma excelente idéia tratar exceção por exceção de vez de todas ao mesmo tempo, onde que se tratar todas ao mesmo tempo não tem como saber qual é a exceção exata que ocorreu o imprevisto.

## Entendendo melhor o finally

O comando finally é utilizado para **forçar** a execução de um trecho de código, mesmo que não ocorra uma exceção, podendo ser executado com ou sem o bloco catch. O bloco de comandos é executado nas seguintes condições:
* Fim normal do método
* Instrução _return_ ou _break_
* Caso uma exceção tenha sido gerada

## Exceções como Objetos

Erros e exceções em Java são Ojetos, possuindo atributos e métodos, onde cada exceção armazena um Strig que informa o tipo de erro ocorrido. Essa String pode ser obtida pelo método getMessage().

Exemplo:

```java
//...
catch (ArrayIndexOutOfBoundsException e){
 System.out.println("Mensagem: " + e.getMessage());
}
```

## Propagando Exceções

Pode-se delegar o tratamento de uma exceção para a porção de código do programa que chamou um método que gerou a exceção.
* Se for uma exceção não verificada, não é preciso fazer nada, se a exceção não for capturada,ela será tratada no método anterior, e assim por diante
* Se for uma exceção verificada, é preciso obrigatóriamente capturá-la ou utilizar a cláusula throws na definição do método, que delega a captura para o chamador.

Eis um caso de uma exceção verificada:

```java
public void gravaList() throws IOException {
 PrintWriter arq = new PrintWriter(new FileWriter("texto.txt"));
 for(int i = 0 ; i < lista.size(); i++){
  arq.println(lista.get(i));
 }
}
```
Neste exemplo, sabe-se que o construtor de FileWriter pode gerar uma exceção _IOException_, que é verificada, ou seja, deve ser obrigatoriamente capturada ou propagada. Caso contrário, o compilador acusará **erro de compilação**, por isso é incluida a cláusula throws. Com isso, o tratamento da exceção deverá ser realizado pelo método que chama a gravaLista().

## Gerando Exceções

Qualquer exceção pode ser gerada através do comando **throw**. É possível gerar uma exceção da API Java ou até criar uma exceção própria. Como exceções são Objetos,precisamos criar um novo objeto que é uma instância do tipo de exceção desejada

* Uma aplicação disso é indicar a ocorrência de erros no construtor de uma classe: é a **Única forma** de informar que houve algum problema lá.
* A API Java define alguns tipos de exceções mais genéricas, que podem ser utilizadas se for o caso:
   * _IllegalArgumentException_: indica um parâmetro inválido em um método
   * _IllegalStateException_: indica um estado inválido para executar uma operação
   * _UnsupportedOperationException_: indica que a operação não pode ser realizada pelo método

Vamos pegar como exemplo uma classe Circulo, onde no construtor ele recebe um raio, uma exceção nesse caso é o raio ser zero, o que não pode acontecer:

```java
public class Circulo
{
 private double raio;

 public Circulo(double raio){
   if(raio <= 0){
     throw new IllegalArgumentException("Raio não pode ser menor ou igual a Zero!"); 
   }else{
      this.raio = raio;
    }
 }
//...
}
``` 