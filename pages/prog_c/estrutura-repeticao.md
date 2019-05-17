[[Página Inicial](../prog_c/home.md)]

# Estruturas de Repetição em C

Estruturas de Repetições servem para utilizar um pedaço de Código quantas vezes forem necessários

---

## Operadores Aritméticos

são operadores principais de Cálculos Matemáticos, muito importantes para atualizarem valores de Atributos ou cálculos diretos

---

Simbolos dos Operadores

Nome do Operador|Símbolo
|---|---|
Adição|<code style="color : lightgreen">+</code>
Subtração|<code style="color : lightgreen">-</code>
Multiplicação|<code style="color : lightgreen">*</code>
Divisão|<code style="color : lightgreen">/</code>
Potenciação|<code style="color : lightgreen">pow(x,y)</code>
Radiciação|<code style="color : lightgreen">sqrt(x)</code>
Módulo ou Resto da Divisão|<code style="color : lightgreen">%</code>
Incremento em uma unidade|<code style="color : lightgreen">++</code>
Decremento em uma unidade|<code style="color : lightgreen">--</code>


Atribuição de valores

Simbolo|Exemplo|Significado
|---|---|---|
<code style="color : purple">+=</code>|x <code style="color : purple">+=</code> 1| x  = x + 1
<code style="color : purple">-=</code>|x <code style="color : purple">-=</code> 1| x = x - 1
<code style="color : purple">*=</code>|x <code style="color : purple">*=</code> 1| x = x * 1
<code style="color : purple">/=</code>|x <code style="color : purple">/=</code> 1| x = x / 1



---

## Estruturas de Repetições

Agora sabendo como funcionam os operadores, iremos ver cada uma das estruturas de Repetições usadas

---

* <code style=" color : gold">Laço de Repetição do While</code>

While recebe uma condição verdadeira e faz toda uma parte de código enquanto essa condição for verdadeira(resultado 1)

```c
//Atributo que irá ser 1
int condicao = 1;

//Atributo que irá ser incrementado
int valor = 0;

while(condicao)
{
    valor += 1;
    
    if(valor == 10)
    {
        condicao = 0; //quando chegar aqui o While para
    }
}

```

* <code style=" color : gold">Laço de Repetição do <code style="color : red">Do While</code></code>

Assim como o While, no caso do `Do While` ele verifica pelo menos uma vez antes de entrar no Laço do while, para poder verificar as entradas antes de usar o While

```c

// Atributo que é Verdadeira
int atributo = 1;
// Atributo que irá ser incrementado
int valor = 0;


do{
    valor += 1
    if(valor == 10){
        atributo = 0;
    }
}while(atributo);

```

* <code style=" color : gold">Laço de Repetição do For</code>

Diferente do While, o For tu define já desde o inicio qual a inicialização,condição Final do Laço e o incremento que você deseja que seja feito

```c

//estrutura
for(condicao_inicial ; condicao_final ; incremento )
{
    //Código
}

//Exemplo

for(int i = 0 ; i < 10 ; i++)
{
    printf("%d"  , i); // será feito 9x
}

```

---

### Podemos utilizar os Laços dentro um do outro quanto quisermos, dependendo da necessidade

---