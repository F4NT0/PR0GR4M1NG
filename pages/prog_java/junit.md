[[Página Inicial](../prog_java/home.md)]

# A ferramenta Junit

* Junit é uma forma de fazer Teste Unitário
   * Teste Unitário é todo baseado na construção de Classes Driver
   * Para cada classe que se deseja testar deve-se construir uma Classe driver de teste que exercita a classe original procurando identificar defeitos
* Vantagens do uso de classes Drivers:
   * Exige que se reflita sobre as funcionalidades da classe e sua implementação antes de seu desenvolvimento
   * Permite a identificação rápida dos defeitos mais simples
   * Permite garantir que a classe cumpra um conjunto de requisitos mínimos
   * Facilita a detecção de defeitos no caso de manutenção ou refactoring
   
* **Anotações:**
    * São rótulos incluídos no código fonte e que servem para indicar o papael do método na classe Driver
    * **@Before**: indica que o método deve ser executado **antes** de cada teste
    * **@After**: indica que o método deve ser executado **Depois** de cada teste
    * **@Test**: indica que é um método de teste
* **Asserções:**
    * Asserções são declarações do que acreditamos ser correto
    * Quando construímos classes Drivers,usamos asserções para verificar as condições que desejamos testar
    * O Junit captura as exceções lançadas pelas asserções
    * Quando uma asserção falha ela lança uma exceção que detecta a falha
    * **assertEquals**: para tipos flutuantes
    * **assertFalse** ou **assertTrue**: sobre uma condição
    * **fail(msg)**: falha o teste e exibe uma mensagem que voce quiser

* **Exemplos**

```java
//classe que desejamos testar:

public class Funcionario{
 private String nome; 
 private int codigo;
 private double salarioBase;

public Funcionario(String n,int c,double s){
 nome = n;
 codigo = c;
 double s = s; 
}

//getters:

public String getNome(){return nome;}
public int getCodigo(){return codigo;}
public double getSalarioBase(){return salarioBase;}

//setters:

public void setSalarioBase(double salB){salarioBase = salB;}

//Método para Calcular o Salario liquido

public double getSalarioLiquido(){
 double inss = salarioBase*0.1;
 double ir = 0.0;
if(salarioBase > 2000.0){
 ir = (salarioBase-2000.0)*0.12;
}
return salarioBase - inss - ir;
}
}
```

```java
//Classe de teste da Classe Funcionario

public class FuncionarioTest{
 private Funcionario func;

@Before //faz antes de começar os testes
public void iniciandoClasse(){ //iniciando a classe que será testada
 Funcionario func = new Funcionario("Pedro",1223,1900.0);
}

@Test
public void testGetSalarioLiquidoMenosQue2000(){
 double expected = 1710;
 double actual = func.getSalarioLiquido();
 assertEquals(expected,actual,0.1);
}

@Test
public void testGetSalarioLiquidoIgual2000(){
 func.setSalarioBase(2000.0);
 double expected = 1900;
 double actual = func.getSalarioLiquido();
 assertEquals(expected,actual,0.1);
}
@Test
public void testGetSalarioLiquidoMaior2000(){
 func.setSalarioBase(3000.0);
 double expected = 2580;
 double actual = func.getSalarioLiquido();
 assertEquals(expected,actual,0.1);
}
}
```

### Processo de Teste Unitário
* Definir a interface(esqueleto) da classe alvo
* Definir o conjunto de casos de teste
* Implementar a classe Driver
* Completar a codificação da classe alvo
* Executar os testes
* Corrigir os bugs, se houver
* Complementar os testes


   

