[[Página Inicial](../prog_java/home.md)]

# Escrevendo arquivos texto em Java

Define-se arquivo texto como um arquivo onde a informação é organizada linha a linha, ou seja, a informação é gravada de forma textual(legível em qualquer editor). Normalmente se considera duas possibilidades nesse tipo de arquivo.

* **Forma Livre:** 
   * É um texto escrito de forma livre no arquivo, sem uma regra de contrução

```
Isto é um texto de forma livre
Onde tudo que escrevo tem um conteudo e formato diferente
1,2,3,4,5
```

* **Formatado:** 
  * Cada linha é um registo bem definido e construido
  * Um exemplo é um arquivo .csv

```
Nome;DataNasc;CPF
Ana Freitas;08/10/2017;123456656.12
Paulo Fagundes;09/10/1998;987654321.02 
```

## Classes para escrever um arquivo texto

1. Classe **BufferedWriter**:
   * Oferece acesso de alto desempenho para gravação de arquivo texto
2. Classe **PrintWriter**:
   * É a classe do objeto out de System, ou seja, permite _println_ e outros.

## Escrevendo um arquivo .txt

Usaremos um bloco _try_ com recursos para simplificar o tratamento de exceções, como abaixo:

```java
Paths path1 = Paths.get("teste.txt");
try(PrintWriter escrevendo = new PrintWriter(Files.newBufferedWriter(path1,Charset.forName("utf8")))){
 escrevendo.println("Escrevendo uma linha de texto");
 escrevendo.println("Escrevendo outra linha de texto");
}
catch(IOException e){
 System.err.format("Erro de Entrada e Saida: %s%n", e);
}
```
No código acima, o símbolo **%s** serve para gravar uma String e **%n** grava um caractere de nova linha

Normalmente essa construção é um padrão para escrever arquivos de texto, mas pode ser moldado.

Criamos no Exemplo acima um _BufferedWriter_ através do método Files.newBufferedWriter e usando o mesmo objeto, criamos um _PrintWriter_. Isso é necessário porque a classe BufferedWriter só oferece métodos para escrever caracteres e Strings, enquanto a PrintWriter tem toda a funcionalidade do println, entre outros. 

## Escrevendo um arquivo .csv

Irei utilizar o arquivo .csv para mostrar como se escreve em um arquivo de texto formatado, que são Strings separadas por um caractere específico(Vírgula ou ponto e Vírgula).

Imagine que tenha uma classe, onde armazena o nome e idade de uma pessoa

```java
public class ClasseInfo {
 private String nome;
 private int idade;

 //construtor
 public ClasseInfo(String nome, int idade){
   this.nome = nome;
   this.idade = idade;
 }

 //Getters
 public String getNome(){return nome;}
 public int getIdade() {return idade;}
}
```

Agora, queremos pegar as Informações que o Usuário colocar no programa e colocar em um arquivo

```java
import java.io.IOException;
import java.io.PrintWriter;
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.util.ArrayList;
import java.util.Scanner;

public class App {
    public static void main(String args[]){
        //criando um ArrayList para armazenar as informações
        ArrayList<ClasseInfo> lista = new ArrayList<ClasseInfo>();

        //Adicionando informações para armazenar:
         Scanner entrada = new Scanner(System.in);
         System.out.println("Quantas entradas o arquivo terá: ");
          int numero = entrada.nextInt();
        for(int i = 0 ; i < numero; i++) {
            System.out.println("Informe o nome da Pessoa: ");
            String nome = entrada.next();
            System.out.println("Informe a idade da Pessoa: ");
            int idade = entrada.nextInt();
            ClasseInfo valor = new ClasseInfo(nome,idade);
            lista.add(valor);
        }

        //Adicionando agora as informações criadas em um arquivo
        Path path = Paths.get("Arquivo.txt");
        try(PrintWriter writer = new PrintWriter(Files.newBufferedWriter(path, Charset.forName("utf8")))){
            for(ClasseInfo info: lista){
                writer.format("%s;%s%n", info.getNome(),info.getIdade());
            }
        }catch (IOException e){
            System.err.format("Erro em criar a formatação: %s%n", e);
        }
    }
}
```
**Este arquivo estará para teste neste Repositório**
