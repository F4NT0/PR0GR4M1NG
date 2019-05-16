[[Página Inicial](../prog_java/home.md)]

# Generalização

* Generalização é o compartilhamento de atributos,operações e relacionamentos entre classes
* Essas Classes devem possui um relacionamento hierárquico para que a generalização aconteça
* O que a Generalização Possibilita:
     * Possibilita a derivação de tipos mais específicos a partir de um tipo mais genérico
     * Uma Classe pode ser definida de forma abrangente e depois ser refinada nas chamadas **`SubClasses`**
     * A classe mais generalizada se chama **`SuperClasse`** e as classes conectadas a ela se chamam **`SubClasses`**
     * Subclasses herdam os atributos,operações e relacionamentos da superclasse,permitindo modificações diferentes em cada classe usando as informações da SuperClasse.
* Classe Mais Geral: **`SuperClasse`**
* Classes Mais detalhadas: **`SubClasses`**

# Herança

* É um mecanismo de reutilização de Código para atributos e métodos em comum em várias classes
* A ideia central de heranças é que novas classes são criadas a partir de classes já existentes
* Heranças seguem as ideias transmitidas na **`Generalização`**
* os Métodos e Variáveis definidos na SuperClasse **`Não são Declarados nas SubClasses`**
* Como Exemplo, queremos controlar os Funcionários de uma Empresa, mas nessa Empresa Existem diversos tipos de Funcionarios, portanto a Classe Funcionario é a SuperClasse e a informação de cada tipos de Funcionario são as SubClasses:
   
|Tipo de Funcionario|Informações relevantes|Informações Gerais
|-------------------|----------------------|------------------
| Motorista| Carteira De Motorista,Data de expiração da Carteira| nome,cpf,codigo de trabalhador
| Secretário|Secretario de quem,Andar que trabalha|nome,cpf,codigo de trabalhador
| Diretor| Sala onde Trabalha,tempo na direção|nome,cpf,codigo de trabalhador

* Só fiz esses trabalhadores como exemplo
* Podemos ver que todos os 3 Funcionarios possuem informações em Comum, portanto serão as informações que irão se colocados na **`SuperClasse Funcionario`**

```java
//criando a SuperClasse Funcionario

public class Funcionario{
 private String nome;
 private int cpf;
 private int codigoTrabalhador;

public Funcionario(String nome,int cpf,int codigoTrabalhador){
 this.nome = nome;
 this.cpf = cpf;
 this.codigoTrabalhador = codigoTrabalhador;
}

//Getters:

public String getNome(){return nome;}

public int getCpf(){return cpf;}

public int getCodigo(){return codigoTrabalhador;}

//Neste exemplo não precisamos de Setters
 
@Override
public String toString(){
 return getNome() + " " + getCpf() + " " + getCodigo();
}
}
```
* Nas SubClasses Motorista,Secretario e Diretor iremos utilizar as Variaveis e Métodos definidos em Funcionario
* Para chamar a Classe Funcionario nas Subclasses iremos usar a palavra reservada **`extends`**
* Para chamar o valor das Variáveis nas SubClasses iremos usar o método chamado **`super()`**
* no toString() existe uma forma de sobrescrever métodos da superclasse usando a **`Palavra super`** antes do nome do método

```java
//classe Motorista
public class Motorista extends Funcionario{
 private int cartMot;
 private String dataExp;

//no construtor podemos colocar parametros usando as variaveis da SuperClasse
public Motorista(String nome,int cpf,int codigo,int cartMot,String dataExp){
 super(nome,cpf,codigo); //método que irá chamar os valores das variaveis da SuperClasse
 this.cartMot = cartMot;
 this.dataExp = dataExp;
}

//getters são somente das variaveis desta classe

public int getCarteira(){return cartMot;}
public String getDataExp(){return dataExp;}

//
@Override
public String toString(){
return super.toString() + " " + getCarteira() + " " + getDataExp();
}
}
```
* Essa Classe do Motorista é um exemplo completo de como a Herança funciona, assim será com as outras Subclasses definidas anteriormente, fazendo a chamada da SuperClasse na SubClasse e trazendo as variaveis da SuperClasse e definindo qual é as Variaveis da propria SubClasse
 