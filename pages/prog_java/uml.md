[[Página Inicial](../prog_java/home.md)]

# Unified Modeling Language(UML):

* É uma linguagem para a modelagem de sistemas orientados a objetos
* UML não é uma linguagem de programação
* UML não é uma linguagem de marcação
* o Modelo mais usado para orientação a objetos do UML é o **Diagrama de Classes**

# Diagrama de Classes:
![alt text](https://upload.wikimedia.org/wikipedia/commons/f/f0/Diagrama_de_Classes_com_duas_classes.png)

* Diagrama de Classes são utilizados para modelagem estática
* A modelagem estática deve dar suporte as necessidades funcionais do sistema
* necessidades funcionais do sistema é o que o sistema deve prover aos seus usuários finais

## Classe
![alt text](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/uml/class-diagram/class-diagram-object-334x224.PNG)

* **Classe** refere-se a descrição de um conjunto de objetos que compartilham os mesmos atributos,operações,relacionamentos e semântica.

| Funcionario  <- **Nome da Classe** 
|-------------
| - nome: String <- **Atributos**
| -data          <- **Atributos**
| + getNome()    <- **Operações**
| + getData()    <- **Operações**

### **Nome**
* O **Nome** de uma classe distingue uma classe de outra classe, possui duas formas de dar um nome:
     * Nome Simples: somente o nome da Classe  
     * Nome com Caminho: o nome da classe é precedido pelo nome do pacote em que a classe existe

**Nome Simples:**

|Cliente|
|-------|

**Nome com Caminho:**

|Pacote_do_Projeto::Cliente|
|--------------------------|

### **Atributos**

* Cada objeto de uma classe possui um estado,representado pelos valores associados a cada um dos atributos definidos:
 
_[Visibilidade] nome[:tipo][=valor inicial]_

**OBS:** os Atributos de classe são sublinhados

* **Visibilidade:**
   * Público(+): o que pode ser visto por qualquer objeto de qualquer classe
   * Privado(-): o que pode ser visto apenas objetos da propria classe
   * Protegido(#): o que pode ser visto apenas pelos objetos da propria classe e por objetos de suas classes herdeiras(SubClasses)

**OBS:** Vale também para as **Operações**

* **Tipo**
   * o tipo é qual tipo é a variavel que pode ser:
   * Primitivo: int,double,char,boolean,float
   * Objetos de Classes: String,Object, outras classes
* **Valor inicial**
    * essa opção é OPCIONAL
    * será o valor que a variavel inicia,antes de alterar durante a classe

### **Operação**

* Operação é um serviço que pode ser requisitado a qualquer objeto da Classe,afetando o estado
* Operação são os métodos da classe
* Sintaxe básica para Operações:

[visibilidade]nome[(lista_de_parametros)][:tipo-retorno]

**OBS:** as Operações de classe são sublinhados

Exemplos:

|Cliente|
|-------|
| - numero: int 
| - nome: String
| - numValor: int = 5
| + getValor() : String
| + setValor() : void

## Relacionamentos

* Os relacionamentos determinam as ligações entre os objetos
* Fornecem um caminho para a comunicação entre os objetos

### Associação Bidirecional

* Uma associação é um relacionamento estrutural que descreve um conjunto de ligações
* Uma ligação é uma conexão entre objetos, sendo uma linha reta entre duas classes
* **Multiplicidade** é o valor de conexão de quantos existem entre um e outro
    * 1...* _Um ou Mais necessários_
    * 1 _Uma só necessárias_
    * 0...1 _Nenhum ou pelo menos um são necessários_
    * 0...* _Nenhum ou muitos necessários_
 
![alt text](https://d2slcw3kip6qmk.cloudfront.net/marketing/pages/chart/uml/class-diagram/class-diagram-bi-directional-association-689x182.PNG)

### Agregação

* é um caso especial de associação
* Representa relacionamentos onde objetos compostos por outros objetos são modelados como estando associados com suas partes
* Agregação é **Transitiva**: se A faz parte de B, e B faz parte de C, então A faz parte de C
* Agregação é **Não-Simétrica**: se A faz parte de B, então B não faz parte de A
* Agregação representa um vínculo fraco entre duas Classes
* A classe Filha faz sentido mesmo sem a Classe Pai, mesmo se ela deixar de existir
* no Exemplo abaixo o tijolo é a classe filha e a casa é a classe pai
* Usa-se o losango vazio posicionado na classe pai

![alt text](http://www.cleibsonalmeida.blog.br/site/wp-content/uploads/2012/08/uml_agregacao.gif)

### Composição

* A composição representa um vínculo forte entre duas classes onde uma classe Filha só faz sentido se uma classe Pai existir.
* No exemplo abaixo, o funcionário é a classe Filha e a empresa é a Classe Pai
* Usa-se o losango cheio posicionado na classe pai 

![alt text](http://www.cleibsonalmeida.blog.br/site/wp-content/uploads/2012/08/uml_composicao.gif)

### Dependências

* Uma dependência indica a ocorrência de um relacionamento semântico entre dois ou mais elementos do modelo, onde uma classe cliente é dependente de alguns serviços da classe

![alt text](http://slideplayer.com.br/3179722/11/images/12/Depend%C3%AAncia+entre+Classes.jpg)






