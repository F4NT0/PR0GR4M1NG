[[Página Inicial](../prog_java/home.md)]

# Fluxo de dados em Java

Criar um bom sistema de Entrada e Saída é uma das tarefas mais delicadas na programação, pois há diversas abordagens diferentes. Além disso, é necessário tratar várias origens e destinos para os dados. Finalmente, há vários modos de acesso: Sequencial,Aleatório,com ou sem _buffer_,por palavras,binário,etc..

Para resolver esse problema, Java provê uma biblioteca com muitas classes, cada uma com um propósito diferente.

Essas classes estão essencialmente em dois pacotes: **java.io** e **java.nio.files**. De maneira geral, essas estruturas definem E/S em termos de fluxos(chamados de _Streams_)

![](http://www.inf.pucrs.br/flash/progoo/aulas/09_Streams/input-stream.jpg)

**Fluxo de Entrada(Input Stream)**

![](http://www.inf.pucrs.br/flash/progoo/aulas/09_Streams/output-stream.jpg)

**Fluxo de Saída(Output Stream)**

O pacote _java.io_ fornece dois tipos de streams:

* Fluxo de bytes: tratam entrada ou saida de dados em 8 bits
   * Para E/S(I/O) baseada em dados binários(ex: uma imagem)
   * Objetos _InputStream_, _OutputStream_

* Fluxo de caractere: tratam entrada ou saída de caracteres Unicode(16 bits)
   * Para E/S(I/O) baseada em texto(Ex: arquivos .txt ou XML)
   * Objetos _Reader_,_Writer_ 

O pacote java.nio.file foi introduzido no Java 7, e oferece uma interface mais robusta e moderna para a manipulação específica de arquivos, também **corrigindo diversos bugs e incompatibilidades** ainda presentes em java.io, apresentando um desempenho mais elevado , operando diretamente com canais de E/S.

## Classes do pacote java.nio

1. A classe Path

A classe Path representa um caminho em um sistema de arquivos, armazenando o nome de um arquivo e a lista de diretórios usada para construir o caminho para um arquivo ou diretório: Ex: /home/user/...

É usada para examinar,localizar e manipular arquivos, mas seu conteúdo depende do Sistema Operacional. Por exemplo, no Windows os caminhos podem começar pela letra de uma unidade("C:\").

![](http://www.inf.pucrs.br/flash/progoo/aulas/09_Streams/io-dirStructure.png)

2. A classe Paths

Diferente da classe Path, a classe Paths faz operações sobre caminhos, onde com esta classe podemos **Criar caminhos novos**

Ex: Criando um caminho novo:

```java
Path path1 = Paths.get("/home/user2/statusReport");//Linux
Path path2 = Paths.get("/home","user","Desktop"); // Linux
Path path3 = Paths.get("C:\\temp\\dados.txt"); //Windows
```

Ex: Obtendo informações do Caminho:

```java
System.out.println("toString: " + path1.toString()); // /home/user2/statusReport
System.out.println("getFileName: " + path1.getFileName()); // statusReport
System.out.println("getName(0): " + path1.getName(0)); // home
System.out.println("getNameCount: " + path1.getNameCount()); // 3
System.out.println("subpath(0,2): " path1.subpath(0,2)); // /home/user2
System.out.println("getParent: " + path1.getParent()); // /home/user2
System.out.println("getRoot: " + path1.getRoot()); // Windows: C:\ Linux: /
```

3. A classe Files

A classe Files oferece métodos estáticos para a manipulação de arquivos, como:
* **Criar** um novo arquivo
* **Ler** dados do arquivo
* **Gravar** dados no arquivo
* **Remover** um arquivo
* **Alterar** permissões

**Importante:** qualquer operação que envolva arquivos pode falhar, por isso a única forma de tratar situações de erro com arquivos é através de exceções. As exceções de arquivos são todas derivadas de _IOException_ e como já vimos, são **verificadas**(Olhar documentação sobre exceções), portanto devemos capturar e tratar as exceções ou tratá-las através de _throws_

## Comando try com recursos

O comando try permite que seja especificado um ou mais recursos

**Recurso** é algo que deve ser liberado quando o programa termina(arquivo, conexão para banco de dados, etc...). O recurso só estará em uso dentro do bloco _try_, ou seja, quando terminar o recurso será automaticamente liberado. Isso é fundamental para arquivos,pois é preciso abri-los antes de usar, e fechá-los no final. Porém se ocorrer uma exceção, é preciso garantir que serão fechados mesmo assim.

Ex:

```java
try(PrintWriter arq = new PrintWriter("texto.txt"))
{
 // Código que usa o Recurso
}
catch(<exceção>)
{
 //Código que trata a exceção
}
//Neste ponto, o arquivo texto.txt não existe mais e o arquivo já foi liberado
```
