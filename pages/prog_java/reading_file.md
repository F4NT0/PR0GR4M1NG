[[Página Inicial](../prog_java/home.md)]

# Lendo de um arquivo texto

* Para se Escrever um texto, Clique [Aqui](https://github.com/F4NT0/Java_Basics/wiki/Writing_Files)

A leitura de um arquivo texto é feito de forma similar a Escrever um arquivo texto, mas usando a Classe _BufferedReader_

* Escrevendo um Arquivo texto .txt comum:

```java
import java.nio.charset.Charset;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.nio.file.Files;
import java.io.IOException;
import java.io.PrintWriter;

public class EscrevendoTexto{
    public static void main(String args[]){
        Path caminhoArquivo = Paths.get("Arquivo.txt"); //Se não existir ele irá criar um
        try(PrintWriter escrever = new PrintWriter(Files.newBufferedWriter(caminhoArquivo, Charset.forName("utf8"))))
        {
            escrever.println("Escrevendo em uma linha");
            escrever.println("Escrevendo em outra linha");
        }
        catch (IOException e){
            System.err.format("Erro de E/S: %s%n", e);
        }
    }
}
```

* Lendo esse arquivo texto:

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;

public class LendoTexto {
    public static void main(String args[]){
        Path caminhoArquivo = Paths.get("Arquivo.txt"); //Procura pelo arquivo específico
        try(BufferedReader leitor = Files.newBufferedReader(caminhoArquivo, Charset.forName("utf8")))
        {
          String line = null; //a variável é iniciada nula, se não tiver informação no arquivo
            int count = 1;
          while((line = leitor.readLine()) != null)
          {
              System.out.println(count + " " + line);
              count++;
          }

        }
        catch (IOException e){
           System.err.format("Erro de E/S: %s%n", e);
        }
    }

}

```

* Essa forma acima de leitura de arquivo texto vai pegando toda a linha e vai imprimindo na tela

### Leitura de um arquivo texto, lendo palavra por palavra

*Iremos utilizar a Classe **Scanner** para poder ler palavra por palavra do texto criado
* Para ler dados formatados, pode-se usar a classe _Scanner_
* A classe _Scanner_ por padrão separa a entrada por espaços em branco
* Pode-se especificar um separador especifico, utilizando a classe _Pattern_

```java
import java.io.IOException;
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.util.Scanner;

public class LendoPalavras {
    public static void main(String[] args) {
    	Path caminho = Paths.get("Arquivo.txt");
    	try (Scanner sc = new Scanner(Files.newBufferedReader(caminho,Charset.forName("utf8")))){
    		String palavra = null;
    		while(sc.hasNext()) {
    			palavra = sc.next();
    			System.out.println("Palavra: " + palavra);
    		}
    	}
    	catch (IOException x) {
    		System.err.format("Erro!" + x);
    	}
    }
}
```

### Lendo o arquivo texto e armazenando as palavras em variáveis

* Iremos ler o seguinte texto:
```
Leticia;24;33558787
```
* Esse arquivo texto esta formatado na forma `Nome;Idade;Telefone`
* Escrevendo Esse Arquivo:

```java
import java.nio.charset.Charset;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.nio.file.Files;
import java.io.IOException;
import java.io.PrintWriter;

public class EscrevendoTexto2{
    public static void main(String args[]){
        Path caminhoArquivo = Paths.get("Dados.txt"); //Se não existir ele irá criar um
        try(PrintWriter escrever = new PrintWriter(Files.newBufferedWriter(caminhoArquivo, Charset.forName("utf8"))))
        {
           String nome = "leticia";
           String idade = "24";
           String telefone = "33558787";
           escrever.format("%s;%s;%s%n", nome,idade,telefone);
        }
        catch (IOException e){
            System.err.format("Erro de E/S: %s%n", e);
        }
    }
}
```

* Lendo esse Arquivo E salvando em variáveis:

```java
import java.io.IOException;
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.util.Scanner;

public class LendoESalvando {
   public static void main(String[] args) {
	   Path path2 = Paths.get("Dados.txt");
	   try(Scanner sc = new Scanner(Files.newBufferedReader(path2,Charset.forName("utf8")))){
		   sc.useDelimiter("[;\n]"); //os Delimitadores do arquivo, que não serão lidos
		   //String header = sc.nextLine(); //pula o cabeçalho
		   String nome,idade,telefone;
		   while(sc.hasNext()) {
			   nome = sc.next();
			   idade = sc.next();
			   telefone = sc.next();
			   System.out.format("%s %s %s %n", nome,idade,telefone); //formato da saida 
		      //ou System.out.format("%s,%s = (%s) %n"), nome,idade,telefone);
		   }
	   }
	   catch (IOException x) {
		   System.err.format("Erro de E/S: %s%n", x);
	   }
   }
}

```

### Lendo um arquivo linha a linha e salvando em variáveis

* Uma alternativa que podemos fazer é ler linha a linha usando apenas o _BufferedReader_ e depois quebrar cada linha com um _Scanner_

* Irei mostrar um exemplo de um código feito com o arquivo Dados.txt mostrado antes

```java
import java.io.BufferedReader;
import java.io.IOException;
import java.nio.charset.Charset;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.util.Scanner;

public class LendoESalvando2 {
   public static void main(String[] args) {
	   Path path2 = Paths.get("Dados.txt");
	   try (BufferedReader lendo = Files.newBufferedReader(path2, Charset.defaultCharset())){
		   String linha = null;
		   while((linha = lendo.readLine()) != null) {
			   Scanner sc = new Scanner(linha).useDelimiter(";"); //usando o limitador ;
		       String nome,idade,telefone;
		       nome = sc.next();
		       idade = sc.next();
		       telefone = sc.next();
		       System.out.format("%s %s %s%n", nome,idade,telefone);
		   }
	   }
	   catch (IOException x) {
		   System.err.format("Erro %s%n", x);
	   }
   }
} 


```


