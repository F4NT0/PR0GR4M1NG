[[Página Principal](../prog_js/home.md)]

---

# Matemática em Javascript

---

* São os Símbolos matemáticos de Javascript:
     * **+** Soma
     * **-** Subtração
     * _*_  Multilicação
     * **/** Divisão
     * **%** Modulo (é o resto que sobra de uma divisão)
     * **++** incremento
     * **--** decremento   
     * **( e )** para controlar o que deve ser feito primeiro na conta matemática

* Exemplos de Uso:

```javascript
//Soma
//exemplo 1
let soma = 3+2; //saida: 5

//exemplo 2
let val1 = 3;
let val2 = 2;
let soma2 = val1 + val2; //saida: 5

//subtração
//exemplo 1
let sub = 3 - 2; //saida: 1

//exemplo 2
//usando as variaveis val1 e val2 definidas acima:
let sub2 = val1 - val2; //saida: 1

//multiplicação
//exemplo 1
let mult = 3 * 2; //saida: 6

//exemplo 2
let mult2 = val1 * val2; //saida: 6

//divisão
//exemplo 1
let div = 3 / 2; //saida: 1.5
//exemplo 2
let div2 = val1 / val2; //saida: 1.5

//modulo
//exemplo 1 
let mod = 3 % 2; //saida: 1 porque sobra 1 no resto da divisão

//exemplo 2
let val3 = 5;
let val4 = 5;
let mod2 = val3 % val4; //saida: 0 porque não sobra resto na divisão

//incremento
//exemplo 1
let valor = 5;
valor++; //mesma coisa que dizer: valor = valor+1;
alert(valor); // o valor de valor será 6
//exemplo 2
++valor; //funciona da mesma forma que no exemplo 1
alert(valor); // o valor de valor é 7

//decremento
//exemplo 1
let valor2 = 5;
valor2--; //mesma coisa que dizer: valor = valor-1;
alert(valor2)// o valor de valor será 4
//exemplo 2
--valor2;
alert(valor2); //o valor de valor é 3 

//controle de conta
let valor = 3+5*3; //na matemática normal, a soma é sempre feita antes da multiplicação
let valor3 = 3+(5*3); //usando parenteses faz com que o calculo dentro deles será feito primeiro 
```

# Trabalhando com o simbolo assignment(=) na matemática

* podemos facilitar a vida utilizando o assignment de vez de fazer uma conta nova
* serve principalmente para atualizar o valor de uma variavel
* tabela de como funcionam:

|operador|exemplo|equivalencia na matemática
|--------|-------|------------------------
| =      | x = y | x = y
| +=     | x += y| x = x + y
| -=     | x -= y| x = x - y
| *=     | x *= y| x = x * y
| /=     | x /= y| x = x/y
| %=     | x %= y| x = x % y

# Comparações de valores

* O símbolo **==** verifica se os valores a esquerda e da direita são iguais e retornam um boolean
* Tabela de comparações:

|operador| descrição | exemplo | resposta booleana
|--------|-----------|---------|-----------------
| ==     | é igual a | 5 == 10 | false
| ===    | identico a| 5 ===10 | false
| !=     | não é igual| 5 != 10 | true
| !==    | não é identica| 5 !== 5| false
| >      | maior que | 10 >5 | true
| >=     | maior ou igual que| 10 >= 5 | true
| <      | menor que | 10 < 5 | false
| <=     | menor ou igual que | 10 <= 5 | false

# Operadores lógicos

* tem 3 operadores lógicos usados em Javascript:
     
 * **&&** retornará true se os dois operandos forem true
      
 * **||** retornará true se pelos menos um dos operandos for true
      
 * **!** retornara verdadeiro se o operando for falso e falso se o operador for verdadeiro

* Exemplos:

```javascript
let booleano = 3 > 4 && 2 < 5 //retornará false
let booleano2 = 3 > 4 || 2 < 5 // retornará true
let booleano = !(3 < 4) //retornará false
```