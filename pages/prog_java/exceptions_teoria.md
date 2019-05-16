[[Página Inicial](../prog_java/home.md)]

# Tratamento de Exceções (TEORIA)

Á medida que os programas se tornam mais complexos,podem apresentar situações anormais ou inválidas durante sua execução, costumamos chamar isso de erros e exceções.

**Erros** são situações excepcionais que ocorrem fora do escopo do programa, e normalmente implicam em finalização do mesmo

Ex: Falta de Memória

**Exceções** são eventos inesperados ou indesejados, que afetam o fluxo de execução normal de um programa, e que podem ser tratados

Ex: 
* Falhas na aquisição de um recurso(Tentar abrir um arquivo que não existe)
* Tentativa de fazer algo impossivel(divisão por zero)

## Conceito básico de Tratamento de Exceções

O tratamento de exceções de Java envolve dois conceitos importantes:

1. **Lançamento(throw)**: Quando um método encontra uma situação anormal, ele informa tal anormalidade pelo lançamento(geração) de uma exceção.Por exemplo, o método Integer.parseInt(String s) que converte Strings para inteiros,irá lançar a exceção _NumberFormatException_ se a String não possui somente dígitos de um número inteiro

2. **Captura(catch)**: Quando um método tenta detectar uma condição,ele captura essa exceção,possivelmente indicando que irá realzar o tratamento do problema encontrado. Por exemplo, um método que faz uso de Integer.parseInt(String s) pode querer capturar essa exceção para evitar problemas no programa.

Em resumo, a idéia com o tratamento de exceções é anecipar os possiveis problemas, e tentar resolvê-los, de forma que situações de erro possam ser revertidas.

## Hierarquia de Exceções

Exceções são objetos que indicam a ocorrência de um evento anormal. Java deriva objetos que indicam exceções a partir da Classe Throwable, esta por sua vez possui duas Subclasses imediatas.

* Exception: Para indicar ocorrências de eventos que causam um disturbio no fluxo normal de execução de uma operação e podem ser tratados

* Error - para indicar uma condição anormal fora do escopo da aplicação e que não pode ser tratado(erros internos da máquina virtual,falta de memória,etc...)

![](https://3.bp.blogspot.com/-j8y3jyEkRKg/WDCVASlGsoI/AAAAAAAADQ8/oTdt8ty-emUBcNuzVzXpZKpTU2nGWeVrACLcB/s1600/ExceptionClassHierarchy.png)

Existem dois tipos de exceções derivadas de Exception:
   1. **Exceções Verificadas(Checked)**: São situações que estão fora do controle do programa, mas que podem antecipar e nos recuperarmos a partir delas.
   
Exemplo: Ao tentar abrir um arquivo que não existe(_FileNotFoundException_). Esse tipo de exceção obrigatóriamente deve ser tratado e é inclusive verificado em tempo de compilação. Java considera que qualquer classe derivada de Exception(menos RuntimeException) é uma exceção verificada.

  2. **Exceções não verificadas (unchecked)**: São normalmente causadas por programação incorreta da própria aplicação.

Exemplo: tentar acessar um elemento fora dos limits de uma _array_, ou acessando métodos a partir de uma referência null. _São todas as classes derivadas de **RuntimeException**_. A API de Java utiliza extensivamente esses tipos de exceções. Não precisam necessariamente ser tratadas mas se não forem, o programa irá terminar com um erro.