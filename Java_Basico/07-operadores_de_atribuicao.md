# Operadores de Atribuição

O Java possui vários operadores que permitem realizar diversas operações e manipular dados. Nesse tópico serão mostrados os operadores de atribuição. O Java possui dois tipos de operadores de atribuição o simples e os compostos.

Os operadores de atribuição são usados para atribuir (armazenar, definir...) valores a variáveis/constantes. No caso das variáveis, o operador de atribuição pode também alterar o seu valor.

## Operador de Atribuição Simples

O operador de atribuição simples é o sinal de igual “**=**” que atribui o valor da expressão a direita do sinal ao operando do lado esquerdo do sinal. Portanto, em Java, o sinal de igual não serve para comparar a igualdade entre dois operandos e sim atribuir/definir um valor a um operando.

### Sintaxe

```java
<operando> = <valor>;
```

### Exemplo

```java
idade = 33;
area = altura * largura;
```

No primeiro exemplo, o valor 33 será atribuído a variável `idade`. Já no segundo exemplo o resultado da multiplicação da `altura` pela `largura` será atribuído a variável `area`.

## Operadores de Atribuição Compostos

Os operadores de atribuição compostos combinam uma operação aritmética com o operador de atribuição simples. Esses operadores realizam uma operação aritmética (soma, subtrai, multiplica, divide...) com o valor atual da variável e depois atribui o resultado na própria variável.

### Sintaxe

```java
<operando> += <valor>;
<operando> -= <valor>;
<operando> *= <valor>;
<operando> /= <valor>;
<operando> %= <valor>;
```

### Exemplo

```java
int x = 5;
x += 10     // x receberá 15 (5 + 10)
x -= 3 	    // x receberá 12 (15 – 3)
x *= 2	    // x receberá 24 (12 * 2)
x /= 3 	    // x receberá 8 (24 / 3)
x %= 5 	    // x receberá 3 (8 % 5 -> resto da divisão de 8 por 5)
```
