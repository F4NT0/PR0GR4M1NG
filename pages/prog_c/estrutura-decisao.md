[[Página Inicial](../prog_c/home.md)]


# Estruturas de Decisão em C


Antes de trabalharmos com estruturas de decisão,devemos trabalhar com lógica de programação

---

## Tabelas verdades

---

Quando trabalhamos com Tabelas Verdades, trabalhamos com dois valores Booleanos:

* <code style="color : green">True</code> = é uma resposta positiva que causa que as ações sejam feitas nas estruturas de controles

* <code style="color : red">False</code> = é uma resposta negativa que para interações do sistema

As tabelas-verdades trabalham com os resultados usando essas respostas booleanas para tratarmos de decisões

---

<code style="color : gold">Conjunção</code>

A|B| A && B
|---|---|---|
<code style="color : green">True</code>|<code style="color : green">True</code>|<code style="color : green">True</code>
<code style="color : green">True</code>|<code style="color : red">False</code>|<code style="color : red">False</code>


<code style="color : gold">Disjunção</code>

A|B| A `||` B
|---|---|---|
<code style="color : green">True</code>|<code style="color : green">True</code>|<code style="color : green">True</code>
<code style="color : green">True</code>|<code style="color : red">False</code>|<code style="color : green">True</code>
<code style="color : red">False</code>|<code style="color : green">True</code>|<code style="color : green">True</code>
<code style="color : red">False</code>|<code style="color : red">False</code>|<code style="color : red">False</code>

<code style="color : gold">Negação</code>

A| !A
|---|---|
<code style="color : green">True</code>|<code style="color : red">False</code>
<code style="color : red">False</code>|<code style="color : green">True</code>

ou

B| !B
|---|---|
<code style="color : green">True</code>|<code style="color : red">False</code>
<code style="color : red">False</code>|<code style="color : green">True</code>

---

## Operadores Relacionais

São utilizados para comparação de valores e entregam um valor Booleano como resposta

---

Nome do Operador|Simbolo|Exemplo
|---|---|---|
Igualdade|<code style="color : lightblue">==</code>| 2 <code style="color : lightblue">==</code> 2
Menor|<code style="color : lightblue"><</code>| 3 <code style="color : lightblue"><</code> 4
Maior|<code style="color : lightblue">></code>| 4 <code style="color : lightblue">></code> 3
Maior ou Igual|<code style="color : lightblue">>=</code>| 3 <code style="color : lightblue">>=</code> 2 ou 3 <code style="color : lightblue">>=</code> 3
Menor ou Igual|<code style="color : lightblue"><=</code>| 3 <code style="color : lightblue"><=</code> 4 ou 4 <code style="color : lightblue"><=</code> 4
Diferente|<code style="color : lightblue">!=</code>| A <code style="color : lightblue">!=</code> B

---

## Estruturas de decisão

são estruturas que fazem uma parte de código se um teste lógico de <code style="color : green">True</code>, se der <code style="color : red">False</code> irá fazer outra parte de código

---

* <code style="color : gold">Decisão Simples</code>

Simplesmente um teste IF

```c
if(teste_logico)
{
    //código
}
```


* <code style="color : gold">Decisão Composta</code>

Quando uma decisão possa dar um valor False, ele causa outra linha de código

```c
if(teste_logico)
{
    // Código se der True
}
else
{
    // Código se der False
}
```

* <code style="color : gold">Decisão Multipla</code>

Utilizamos uma estrutura chamada Swift que serve para mudar o resultado dependendo de uma resposta especifica de entrada

```c

// Pegamos uma variavel de entrada que recebe um inteiro de 1 á 5
parametro;
scanf("%d", &parametro);

switch(parametro)
{
    case 1 : printf('Entrada foi 1');
    break;
    case 2 : printf('entrada foi 2');
    break;
    case 3 : printf('entrada foi 3');
    break;
    case 4 : printf('entrada foi 4');
    break;
    case 5 : printf('entrada foi 5');
    break;
    default : printf('Entrada não permitida');    
}
```

