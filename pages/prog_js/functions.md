[[Página Principal](../prog_js/home.md)]

---

# Funções de Javascript

---

* As funções de Javascript são um bloco de código designados para uma função específica
* A vantagem de usar funções é reutilização(reuse), defina a função uma vez e pode reutilizar quantas vezes quiser
* pode usar quantas vezes a função e pode alterar os seus argumentos para o que desejar, para produzir diferentes resultados
* Definindo uma função:
  * para definir uma função em javascript, utilizamos a palavra reservada **function** primeiro
  * depois vem o **nome da função** e depois os parametros dentro de um parenteses
  * dentro do parenteses dos parametros pode ou não ter parametros
  * o nome do método deve funcionar que nem definir variaveis

```javascript
function nomeMetodo(){
 //código para ser executado
}
```

## Chamando uma função

* Para se usar uma função, você deve chamá-la
* Para chamar uma função, você deve iniciar o nome da função, abrir e fechar parenteses e chamar os valores para os parametros definidos
* Exemplo:

```javascript
//função que queremos
function minhaFuncao(){
 alert("função foi chamada");
}

minhaFuncao();

//podemos chamar uma função quantas vezes quisermos:
minhaFuncao();
minhaFuncao();
minhaFuncao();
//todos irão rodar no programa
```

# Parâmetros de uma Função

* Funções podem receber parâmetros
* Os parâmetros de uma função são os nomes listados na definição da função

```javascript
funcion nomeFuncao(parametro1,parametro2,parametro3,...){
  //código para ser executado
}
```
* Quando chamar uma função existem duas formas de entrar um Parâmetro
  * Entrando um valor direto no lugar do parâmetro
  * Definir uma variável e dar um valor para ela e depois chamar ela dentro da função 

```javascript
//Opção 1
let i = 10; //variavel iniciada
//iniciado uma função
function numero(parametro){
 alert(parametro);
}
//chamando a função
numero(i);
//o valor guardado na variavel i vai ser lançado dentro da função

//Opção 2
iniciando uma função
function numero(parametro){
 alert(parametro);
}
//chamando uma função
numero(23); //chamando o valor desejado direto na chamada de uma função
```

* Assim como podemos chamar quantas vezes quisermos a função, podemos definir um valor diferente para os parâmetros
* Podemos fazer vários testes com a função desse jeito
* Podemos ter multiplos parâmetros, mas quando formos chama-los deve ter uma ordem de entrada
```javascript
//iniciando uma função
function funcao(nome,idade){
 alert(`meu nome é ${nome}! e minha idade é ${idade}!`);
}

//quando for chamar a função:
funcao("Pedro",23); //CERTO
funcao(23,"Pedro"); //ERRADO 
//podemos fazer como a segunda forma, mas o resultado não faria sentido
```

# A declaração Return

* Uma função pode ter uma declaração opcional chamada **return**
* ela é usada para retornar o valor de uma função
* Ela é bem util quando quisermos um resultado de um cálculo
* Quando o programa chega no return e o executa, depois ele para de executar a função
* Exemplo do uso de return:

```javascript
//Função 1
function saida(a,b){
 return a*b;
}
//Chamada da função
let valor = saida(4,5);
document.write(valor); //saida: 20
//se não tiver um valor, retornará undefined

//Função 2
funcion saida2(a,b){
 let c = a * b;
return c;
}
//Chamada da função
document.write(saida2(2,3)); //saida: 6
//se não tiver um valor, retornará undefined
```

# A função Alert

* a função Alert, dita desde o inicio é uma função que faz o Output do programa sair em uma caixa de alerta no sistema
* aparece junto com o output do sistema um botão de OK, onde somente irá fechar aquela tela depois de voce clicar nele

```javascript
alert(...);
```

# A função Prompt

* essa função prompt serve se você deseja que o usuário escreva um valor de entrada no sistema
* Ele pergunta pela entrada do usuário antes de entrar na página do site(por exemplo)
* O usuário tem a opção de cancelar ou dar um ok depois de entrar com o valor na tela
* se Clicar em Cancelar, o programa irá utilizar o null no lugar de um valor
* A função prompt possui *Dois Parâmetros*
  * O primeiro Parâmetro é o que você deseja passar de mensagem para o usuário
  * O segundo Parâmetro é opcional, se você deseja colocar um exemplo do que gostaria que o usuário entrasse como dado no sistema

```javascript
let usuario = prompt("Por Favor, entre um Número","Ex: 1");
alert(usuario);
``` 

# A função Confirm

* essa função normalmente é usado para perguntar para o usuário se deseja continuar ou cancelar
* dependendo da escolha, o programa irá retornar um booleano:
  * Se o usuário clicar em OK, irá retornar um true
  * Se o usuário clicar em Cancelar, irá retornar um false
* Exemplo:

```javascript
let resultado = confirm("Deseja sair dessa página");
if(resultado == true){
 alert("Obrigado pela visita!");
}
else{
 alert("Obrigado por continuar aqui!");
}
```


