[[**Página Inicial**](../README.md)]

# Modelagem Básica de uma classe Orientada a Objetos

Existem  Partes de um código Básico de uma Classe:
* Método Construtor
* Métodos Getters
* Métodos Setters
* Método toString

### Método Construtor:

* Um método construtor é um método que é utilizado para **iniciar um objeto dessa classe**
* quando você inicia um método construtor em outra classe se chama **Instanciar um objeto**
* esse Metodo pode ter quantos parametros forem necessarios
* esses parametros sao as variareis necessárias para iniciar o método construtor
* quando se inicia uma variável de objeto, será um objeto criado anteriormente que pode ser chamado nessa classe
* o **this** serve para podermos utilizar o nome da variável mais de uma vez, sendo usado no construtor para que 
o valor de entrada no construtor seja armazenado na variável de mesmo nome

```java
public nomeDaClasse(parametros){
   this.parametro = parametro;
}

//iniciando em outras classes:

nomeDaClasse novo1 = new nomeDaClasse(valor do parametro); 
```

### Métodos Getters:

* Nas classes de objetos são iniciados variáveis privadas
* Para chamar os valores dessas variáveis fora da classe onde foram criadas, usamos métodos Getters
* Métodos Getters servem para retornar o valor de uma variável em outras classes 

```java
//exemplo 1:
private int valor = 5; //foi iniciada a variável privada

public int getValor(){return valor;} //metodo getter de valor

//exemplo 2:

private String valor = "Ola";

public String getValor(){return valor;}
```

### Método Setters:

* Depois de Criado uma classe Getter, não se pode alterar o valor da variável 
* Para trocar um valor de uma variável privada, criamos um método Setter
* No metodo Setter, deve ter um parâmetro de entrada no método para alterar o valor
* aqui podemos usar o **this** também, para referenciar uma variável criada nessa classe

```java
private int valor = 5;

public void setValor(int v){valor = v;}

//exemplo com this:

private int valor = 10

public void setValor(int valor){this.valor = valor;}
```

### Método toString:

* Este Método serve para construir uma saída personalizada para a sua classe orientada a objetos
* Ela ja existe como um método básico do Java, por isso é recomendável utilizar o Override 
* Override serve para que seja sobreescrevido o método nessa classe onde foi recriado o método 

```java

@Override //para sobrescrever

public String toString(){
  return // depois do return você coloca como deseja a saída da sua Classe
}

```  

### Exemplo de Classe Completa:

```java

public class ClasseTeste{
  private int numero;  //iniciado a variável de tipo int 
  private String palavra; //inciado a variável de tipo String, de texto
  private OutraClasse objeto; //iniciado uma variável Objeto, que e de outra classe

//Metodo Construtor:

public ClasseTeste(int numero,String palavra,OutraClasse objeto){
  this.numero = numero;
  this.palavra = palavra;
  this.objeto = objeto;
}

//Getters:

public int getNumero(){return numero;}

public String getPalavra(){return palavra;}

public OutraClasse getObjeto(){return objeto;}

//Setters:

public void setNumero(int numero){this.numero = numero;}

public void setPalavra(String palavra){this.palavra = palavra;}

public void setObjeto(OutraClasse objeto){this.objeto = objeto;}

//toString:

@Override

public String toString(){

return getNumero() + " " + getPalavra() + " " + getObjeto();

// pode também chamar direto as variáveis: return numero + " " + palavra + " " + objeto;

}
  
}

```
