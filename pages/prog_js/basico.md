[[Página Principais](../prog_js/home.md)]

---

# Estruturas Básicas em Javascript

---

## Comentários no Javascript:

```javascript
//Isto é um comentário de uma linha

/*Isto também é um comentário de uma linha*/

/*
 Isto é um comentário de várias linhas
onde espande o quanto quiser
*/
```

## Variáveis no Javascript

* Variáveis são "Case-Sensitives", ou seja, tem uma forma especifica de defini-las:
    * O primeiro símbolo da variável só pode ser uma letra,underscore(_) ou o cifrão($)
    * As consequentes podem ser números,letras,underscore(_) ou o cifrão($)
    * Variáveis **não** aceitam símbolos matemáticos em seu nome (*,+,-,/)
    * Variáveis não podem conter espaços em seu nome
    * o "=" quando iremos definir um valor para uma variável se chama assignment symbol

* Para criarmos uma variável necessitamos usar a palavra reservada **let**
* Não é necessário dizer que tipo de variável estamos definindo,porque ele irá reconhecer automaticamente
* há duas formas de definir um valor para uma variável

```javascript
/*criando uma variável de string*/
let mensagem;
mensagem = "texto da mensagem";
let mensagem2 = "texto da mensagem 2";

/*criando uma variável de numeros*/
let numero;
numero = 42;
let numero2 = 24;

/*criando uma variável de booleanos*/
let valor;
valor = true;
let valor2 = false;
```
## Forma de fazer output de uma informação:

```javascript
/*A primeira forma e a mais básica de sair uma informação*/
 alert(...);

/*Exemplo:*/
let valor = 43;
alert(valor); /*Teste 1*/
alert(32); /*Teste 2*/
alert("Teste"); /*Teste 3*/

/*A segunda forma é para arquivos html onde se chama o javascript*/
/*as tags de javascript(script) deve ser colocado no head do arquivo HTML*/
/*O método document.write() é só para programas testes iniciais*/
<script>
let valor = 42;
document.write(valor);
/*Podemos usar tags de HTML para mudar a forma de saida do texto do Javascript*/
document.write(<h1>"Saida de texto"</h1>);
</script>
```

## Concatenação de variáveis no Output
* Para ter uma variável chamada no Output iremos utilizar a seguinte construção:

```javascript
alert(` ${nomeVariavel}! `);

/*Exemplo:*/
let nome = "F4NT0";
alert(`Me chamo ${nome}!`);
```

## Formas de Contruir um documento de Javascript:
* Existem duas formas de construir um documento Javascript:
    * chamando dentro de uma tag script em um documento .html
    * criando um arquivo separado com a extensão .js

* **Forma 1:**

```html
<html>
 <!-- Isto é um comentário na área do HTML-->
 <head>
  <script>
    /*Aqui vai as informações sobre Javascript*/
   /*Podem ter várias tags script dentro de um arquivo html*/
    let valor = 1;
    alert(valor);
  </script>

 </head>
 <body>

 </body>
</html>
```
* **Forma 2:**
* Nome do Arquivo: teste.js

```javascript
/*isto está sendo escrito dentro do arquivo teste com extensão .js*/
let testeMensagem = "Valor do Sistema";
let valor1 = 23;
alert(`A String: ${testeMensagem}! O Valor: ${valor1}!`);
```
* Como rodar o arquivo .js:
    * 1) crie um arquivo .html separado(normalmente chamamos de index)
    * 2) dentro do arquivo html construa a estrutura básica 
    * 3) abra uma tag script e e use o atributo **src** e coloque o nome do arquivo javascript

```html
<html>
  <head>
    <!-- O script abaixo irá chamar as informações do arquivo javascript -->
    <script type="text/javascript" src="teste.js"></script>

  </head>
  <body>
  </body>
</html>
```
* É muito melhor construir um arquivo separado para poder melhor controlar as alterações feitas no código

## Usando escape Character em Strings
* Existem duas formas de se construir uma String

```javascript
let nome1 = "nome";
let nome2 = 'nome2';
```
* existe um símbolo que auxilia nas saidas de texto, que chamamos de escape character (**\**)
* Usos do escape character:

|no código|saída
|---------|-----
| \\\'      | para fazer uma saída do símbolo **'**
|\\\"       | para fazer uma saída do símbolo **"**
|\\\\       | para fazer uma saída do símbolo **\**
|\n       | para fazer o texto todo ir para a próxima linha
|\b       | para dar um espaço entre duas palavras 
|\t       | tem a mesma função do botão tab do teclado

 ## Usando o typeof

* typeof serve para retornar o tipo de um argumento
* serve para saber que tipo é a variavel criada

```javascript
let str = "teste";
typeof str; /*vai retornar que é uma String*/
let val = 1;
typeof val; /*vai retornar que é um int*/
alert(...);
typeof alert; /*vai retornar que é uma função*/
```

## Tipos de variáveis:
* Existem 7 tipos de variáveis no Javascript:
    * Number: são os números
    * String: são as saídas de texto
    * Boolean: são os valores de T(true) ou F(false)
    * null: serve para valores nulos
    * Undefined: para os valores não definidos
    * Object: para objetos mais complexos
    * Symbol: para identificadores únicos
