[[Página Principal](../prog_js/home.md)]

---

# Estruturas de Decisões e Repetições em Javascript

---

## Loops e Condicionais

### Condicional if 
* if serve para construir um bloco de código que só será executado se uma condição especifica for true
* Construção Básica e exemplos:

```javascript
if(condition){
 //codigo que sera executado se for true a condição
}

//exemplo
let num1 = 7;
let num2 = 10;
if(num1 != num2){
 alert("saida de teste");
}
```

### Condição if-else
* if-else serve para se acontecer da resposta do if der false, ele irá rodar a segunda parte que é o else

```javascript
let num1 = 3;
let num2 = 4;

if(num1 == num2){
  alert("parada"); //só irá aparecer se a condição der true
}
else{
 alert("continua"); //só irá aparecer se a condição der false
}
```

### Condição else if

* Funciona da mesma forma que o if-else só que podemos adicionar um novo teste de if dentro

```javascript
let valor = 1;

if(valor == 2){
 alert("saida 1");
} else if(valor == 1){ //ele é o else do primeiro if mas ele começa um teste de if novo
  alert("saida 2");
}else{  //este else só irá acontecer se o primeiro if e o else if forem false
 alert("saida 3");
}
```

### Switch

* Em caso de Necessitar de fazer multiplas condições, podemos utilizar o switch para isso
* no Switch, ele avalia a condição uma vez e o compara com o que chamamos de **case**
* se tiver um case que é igual ao resultado da condição, então ele roda o que tem dentro da contrução desse case
* Contrução Básica:

```javascript
 switch(expressao){
  case n1: 
   //códigos de dentro do case n1
  break; //encerra a operação depois de ler tudo de dentro do case

  case n2:
   //códigos de dentro do case n2
  break;
  
   .
   .
   .
  default: //o default é quando nenhum dos valores definidos como cases são iguais ao resultado da condição
    //códigos de dentro do default
}
```
* Exemplo completo de um Switch

```javascript
let valor = 2;
switch(valor){
 case 1: alert("o valor de valor é 1");
 break;
 case 2: alert("o valor de valor é 2");
 break;
 case 3: alert("o valor de valor é 3");
 break;
 case 4: alert("o valor de valor é 4");
 break;
 default:alert("o valor de valor é outro valor");
}
```
* Pode existir quantos cases forem necessário no switch

### O loop FOR

* Loops podem executar um código quantas vezes quisermos
* Normalmente são usados para atualizar um valor várias vezes
* o FOR é o mais comum das contruções de loop, mas existem também o while e do-while
* Construção básica de um FOR:

```javascript
for(declaração 1; declaração 2; declaração 3){
 //código de programa que será executado
}
```
* **declaração 1** será executada antes do loop iniciar
* **declaração 2** define a condição para rodar o loop e quanto tempo ele irá levar
   * ele irá **continuar no loop** enquanto a condição da declaração 2 for **true**
   * ele irá **encerrar o loop** se a condição da declaração 2 for **false**
* **declaração 3** é executado cada vez depois do loop ter sido executado

* Contrução clássica de um for:

```javascript
for(i = 0 ; i < 3 ; i++){
 alert(`O valor de i é ${i}!`);
}
// declaração 1: a variavel i foi iniciada com o valor 0
//declaração 2: a variavel i vai sendo alterada até i se tornar 2
//declaração 3 : a cada virada do loop o valor do i vai sendo incrementado
/*
A SAIDA DO FOR É:
 o valor de i é 0
 o valor de i é 1
 o valor de i é 2
*/
```

### O loop WHILE

* o loop while irá ficar se repetindo até que a sua condição se torne false
* o while pode rodar para sempre se quisermos
* construção básica do while:
```javascript
while(condicao){
 //código que será executado
}
```
* Exemplo de um while:

```javascript
let i = 0;
while(i <= 10){
 document.write(i);
 i++;
}
/*
saida:
0
1
2
3
4
5
6
7
8
9
10 ele irá parar em 10 porque depois a condição se torna false
*/
```

### o loop DO...WHILE
* este loop é uma variante do loop while
* neste loop, ele irá executar o bloco de código desejado **antes** de checar o loop while para ver se a condição é true
* se a condição do while for true, ele irá repetir o loop até que a condição se torne false
* sintaxe básica:

```javascript
do{
 //código do loop
}
while(condicao);
```
* Exemplo:

```javascript
let i = 20;
do{
 document.write(i);
 i++;
}
while(i <= 25);
```
* o código **irá rodar pelo menos uma vez** antes de saber se irá começar o loop

### Break

* A palavra reservada **break** serve para encerrar um loop e pular para a continuação do código depois
* apareceu pela primeira vez no switch nessa wiki
* atenção: o break não encerra o processo do código,só encerra o loop onde ele foi implementado
* voce pode usar o break como resultado de uma condição:

```javascript
for(i = 0 ; i <= 10;i++){
 if(i ==5){
  break;
 }
 document.write(i);
}

/*
 Saida do loop:
  0
  1
  2
  3
  4
 ele irá encerrar quando o i for 5 e não chega no Output que foi definido depois do break
 Quando ele chega no break, ele pula para fora do loop na hora
*/
```

### continue

* o continue, diferente do break, ele não sai do loop, ele só pula a interação onde ele foi implementado
* podemos pular uma interação do loop para outra 

```javascript
for(i = 0 ; i <= 10 ; i++){
 if(i == 5){
  continue;
 }
 document.write(i);
}
/*
saidas do loop:
0
1
2
3
4
6
7
8
9
10
ele pulou o loop quando o valor do i chegou em 5 e foi para o loop com o valor do i em 6
*/
```


