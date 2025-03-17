# Operadores

Na programação, os operadores são símbolos que realizam uma operação sobre um ou mais operandos. O Java oferece diversos operadores que são divididos em várias categorias baseado na sua funcionalidade. Nesse tópico iremos tratar sobre os operadores aritméticos, relacionais e lógicos. Já foi visto também, em outro tópico, os operadores de atribuição.

## Aritméticos

Os operadores aritméticos são usados para realizar operações fundamentais da matemática. São considerados “operadores binários” pois funcionam com dois operandos. 

No Java, os operadores aritméticos: adição, subtração, multiplicação e divisão e os sinais de positivo e negativo, funcionam da mesma forma que na matemática comum.

Veja a lista dos operadores aritméticos:

- **+ – adição**: retorna o resultado da adição de dois operandos.

- **- – subtração**: retorna a diferença entre dois operandos. 

- **\* – multiplicação**: retorna o resultado da multiplicação entre dois operandos.

- **/ – divisão**: retorna o quociente da divisão entre dois operandos. No caso desse operador, pode haver dois tipos de divisão: divisão de números inteiros e divisão de números reais (com casas decimais).

    - **Divisão de inteiros**: quando os dois operandos são inteiros, o quociente da divisão também será um inteiro. Exemplo: 

        ```java
        double x;
        x = 7 / 2; // x = 3, mesmo que x seja do tipo float/double.
        ```

    - **Divisão de reais**: quando um dos operandos é de um tipo de ponto flutuante (**float** ou **double**). Nesse caso a variável que irá receber o resultado deverá ser do tipo **float** ou **double**. Exemplos:

        ```java
        double x;
        x = 7 / 2.0; // x = 3.5 
        int a = 7, b = 2;
        x = a / (double) b; // x = 3.5 – casting explícito
        ```
    
        O exemplo usando o casting explícito é usado principalmente quando se precisa do resultado real, mas com os dois operandos sendo variáveis do tipo inteiro. Nesse caso, faz-se a conversão (casting) de uma das variáveis para ponto flutuante na expressão.

- **% – resto**: retorna o resto da divisão entre operandos do tipo inteiro.

### Exemplos

```java 
int a = 7;
int b = 2;
int i;
double d;

i = a + b; // i = 9;
i = a – b; // i = 5;
i = a * b; // i = 14;
i = a / b; // i = 3;
d = a / b; // d = 3.0;
d = a / (double) b; // d = 3.5;
i = a % b; // i = 1 – resto da divisão de 7 / 2.
```

## Incremento / Decremento

São operadores unários que devem ser usados juntos de uma variável.

- **++ – incremento**: incrementa o valor da variável em uma unidade.

- **-- – decremento**: decrementa o valor da variável em uma unidade.

Os operadores de incremento/decremento podem vir antes da variável ou depois da variável, sendo chamados de pré-fixado ou pós-fixado respectivamente. Se você usar o operador de incremento/decremento de forma isolada, a posição do operador não fará nenhuma diferença. Mas, se você usar o operador dentro de uma expressão, a sua posição faz toda diferença. Veja a diferença entre eles:

- **Pré-fixado** – O valor da variável será incrementado/decrementado primeiro para só depois o seu valor ser usado na expressão em que ela se encontra.

- **Pós-fixado** – O valor da variável será primeiro usado na expressão em que ela se encontra para só depois ser incrementado/decrementado.

### Exemplos

```java
int a = 1;
int b;
a++; // a = 2
a--; // a = 1
b = a++; // a = 2 e b = 1 (pós-incremento)
b = ++a; // a = 3 e b = 3 (pré-incremento)
```

## Relacionais

Os operadores relacionais, também conhecidos como operadores de comparação, avaliam a relação entre dois operandos, em outras palavras, eles fazem a comparação entre dois operandos. Os resultados dos operadores relacionais serão sempre um valor lógico (**booleano**): verdadeiro ou falso (**true** | **false**).

Veja a lista dos operadores relacionais:

- **== – igual a**: retorna verdadeiro (**true**) se o operando da esquerda for igual ao operando da direita, caso contrário retorna falso (**false**).

- **!= – diferente de**: retorna verdadeiro (**true**) se o operando da esquerda for diferente do operando da direita, caso contrário retorna falso (**false**).

- **> – maior que**: retorna verdadeiro (**true**) se o operando da esquerda for maior que o operando da direita, caso contrário retorna falso (**false**).

- **< – menor que**: retorna verdadeiro (**true**) se o operando da esquerda for menor que o operando da direita, caso contrário retorna falso (**false**).

- **>= – maior ou igual a**: retorna verdadeiro (**true**) se o operando da esquerda for maior ou igual ao operando da direita, caso contrário retorna falso (**false**).

- **<= – menor ou igual a**: retorna verdadeiro (**true**) se o operando da esquerda for menor ou igual ao operando da direita, caso contrário retorna falso (**false**).

### Exemplos

```java
int a = 5;
int b = 10;
boolean res;

res = b == a; // res = false
res = b == a*2; // res = true
res = a != b; // res = true
res = b > a; // res = true
res = a < b; // res = true
res = b <= a*2; // res = true
res = b >= a*2; // res = true
```

## Lógicos

Os operadores lógicos avaliam uma expressão, ou combinam várias expressões, retornando um único valor verdadeiro (**true**) ou falso (**false**). Em outras palavras, os operadores lógicos permitem que você crie expressões lógicas maiores a partir da união de expressões lógicas simples. 

Veja a lista dos operadores lógicos:

- **&& – lógico E (and)**: retorna verdadeiro (**true**) se os dois operandos forem verdadeiros.

- **|| – lógico OU (or)**: retorna verdadeiro (**true**) se pelo menos um dos operandos for verdadeiro.

- **!  – lógico NÃO (not)**: inverte o valor do operando.

### Exemplos

```java
int a = 10;
int b = 15;
boolean res;

res = a > b && (a + b == 25); // res = false
res = a > b || (a + b == 25); // res = true
res = !( a > b && (a + b == 25)); // res = true
res = !(a > b || (a + b == 25)); // res = false
```

## Ternário

O operador ternário, também conhecido como operador condicional, possui três operandos. O operador ternário avalia uma expressão booleana (primeiro operando) e retorna um de dois valores (segundo e terceiro operandos). Caso a expressão seja avaliada como verdadeira, será retornado o segundo operando, já se a expressão for avaliada como falso, será retornado o terceiro operando.

### Sintaxe

```java
expressaoBooleana ? vlrExpVerdadeira : vlrExpFalsa
```

### Exemplos

```java
int nota = 67;
String sit1 = (nota > 60) ? "aprovado" : "reprovado";
String sit2 = (nota < 40) ? "reprovado" : (nota < 60) ? "recuperação" : "aprovado";
```

Repare que a variável “**sit2**” poderá receber um de três valores, pois foram usados dois operadores ternários aninhados. Se a primeira expressão booleana (**nota < 40**) for avaliada como verdadeira o valor “**reprovado**” será retornado para a variável “**sit2**” mas, se for avaliada como falsa, o segundo operador ternário será executado avaliando a expressão (**nota < 60**) e, se essa segunda expressão booleana for verdadeira a variável “**sit2**” recebe o valor “**recuperação**” e se for falsa recebe o valor “**aprovado**”.

## Precedência de operadores

Há situações em que você precisará juntar operadores diferentes em uma mesma expressão. Nesses casos, cada operação possui uma ordem, predeterminada, para ser executada. Essa ordem é denominada como precedência. 

Segue a lista de precedência dos operadores em Java, da mais alta (executado primeiro) até a mais baixa precedência.

- **( )** – as expressões entre parênteses serão executadas primeiro.

- **+ - ++ --** – operadores unários positivo e negativo e operadores de incremento e decremento.

- **\* / %** – multiplicação, divisão e módulo (resto da divisão).

- **+ -** – adição e subtração.

- **< <= > >=** – menor que, menor ou igual, maior que, maior ou igual.

- **== !=** – igual, diferente.

- **&&** – operador lógico **E**.

- **||** – operador lógico **OU**.

- **? :** – operador ternário.

- **= \<opArit>=** – atribuição e atribuição composta.

Quando ocorrer, na mesma expressão, mais de um operador com a mesma precedência, eles serão avaliados da esquerda para a direita.
