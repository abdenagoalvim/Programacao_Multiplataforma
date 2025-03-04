# Variáveis, Constantes e Tipos Primitivos

Variável e/ou constante, é um nome dado a um espaço da memória do computador usado para armazenar algum dado para processamento futuro. A diferença entre variável e constante é que a variável poderá ter o seu valor alterado durante o processamento do programa enquanto a constante não. A partir do momento que um valor for definido para uma constante ela terá esse valor enquanto o bloco (escopo) onde ela foi definida estiver sendo executado.

## Nomeando identificadores

Existem algumas regras/convenções que precisam ser seguidas ao nomear qualquer identificador (classes, métodos, variáveis, constantes...) no Java. Veja algumas delas listadas a seguir.

- O Java diferencia letras maiúsculas de letras minúsculas, portanto, um nome de variável escrito com alguma letra maiúscula é diferente de outro nome escrito somente com letras minúsculas.

- Os nomes podem ser compostos por letras e dígitos desde que o primeiro caractere seja uma letra. O Java não aceita caracteres acentuados e nenhum caractere especial, exceto os caracteres “**_**” sublinhado e “**$**” cifrão.

- Um nome de identificador não pode conter espaço em branco.

- O nome escolhido não deve ser uma palavra-chave ou palavra reservada do Java.

- Se o nome consistir em apenas uma palavra, use somente letras minúsculas. As classes devem ter a primeira letra maiúscula.

- Se o nome consistir em mais de uma palavra, coloque em maiúscula a primeira letra de cada palavra subsequente.

- Se o nome for de uma constante, use somente letras maiúsculas separando as palavras com o caractere de sublinhado.

- Prefira palavras completas em vez de abreviações enigmáticas.

## Variáveis

Toda variável no Java, deve ser declarada antes de ser usada. Para declarar uma variável, deve-se informar o tipo e o nome da variável. Antes de ser usada, uma variável também tem que ser iniciada, isso implica em atribuir, armazenar, um valor à variável, o que pode ser feito durante a declaração da variável.

### Sintaxe

```java
<tipo> <nome>;
<tipo> <nome> = <valor inicial>;
```

A atribuição de um valor inicial, `= <valor inicial>`, é opcional e não precisa, necessariamente, ser feita junto com a declaração.

### Exemplo

```java
double altura;
int idade = 25;
altura = 1.85;
```

Repare que a variável `altura` foi, num primeiro momento, declarada e depois inicializada por outro comando. Veja também que os números com casas decimais são separados por um ponto “**.**” e não por vírgula “**,**” como estamos acostumados. Isso ocorre, pois, as linguagens de programação, como o Java, são escritas baseadas na língua inglesa, onde o separador decimal é o ponto “**.**”.

## Constantes

As constantes, conforme dito no início desse tópico, são nomes dados a um espaço da memória para armazenar dados que não sofrerão alteração, como a constante matemática pi.

No Java uma constante é definida através da palavra reservada “**final**” que deve ser colocada antes do tipo na sua declaração. Para identificar melhor as constantes ao longo do programa o seu nome deve ser todo escrito com letras maiúsculas como visto no item “**Nomeando identificadores**”.

### Sintaxe

```java
final <tipo> <NOME> = <valor inicial>;
```

### Exemplo

```java
final double PI = 3.14159;
```

Se você tentar alterar uma constante após ela ter sido inicializada, será gerado um erro.

## Tipos Primitivos

Como dito no início desse tópico, para declarar variáveis/constantes você precisa especificar o seu tipo. O Java possui, basicamente, dois tipos de dados: os primitivos e os compostos, também chamados “de referência” ou “não primitivos”. Nesse tópico trataremos dos tipos primitivos, os tipos compostos (String, Object, arrays, classes...) serão estudados, em outros momentos, ao longo do curso.

Os tipos primitivos em Java são tipos de dados mais básicos, que representam valores numéricos, caracteres e lógicos. Os tipos primitivos possuem melhor desempenho por ocuparem menos espaço e por serem mais rápidos de processar.

O Java possui 8 tipos primitivos:

- **char**: armazena um caractere unicode, ocupando 2 bytes (16 bits) na memória. Pode armazenar valores entre \u0000 a \uFFFF.

- **boolean**: armazena um valor lógico (booleano) true ou false.

- **byte**: armazena um número inteiro com sinal, ocupando 1 byte (8 bits) na memória. Pode armazenar valores entre **-128** a **+127**.

- **short**: armazena um número inteiro com sinal, ocupando 2 bytes (16 bits) na memória. Pode armazenar valores entre **-32.768** a **+32.767**.

- **int**: armazena um número inteiro com sinal, ocupando 4 bytes (32 bits) na memória. Pode armazenar valores entre **-2.147.483.648** a **+2.147.483.647**.

- **long**: armazena um número inteiro com sinal, ocupando 8 bytes (64 bits) na memória. Pode armazenar valores entre **-9.223.372.036.854.775.808** a **+9.223.372.036.854.775.807**. Por padrão, no Java, os números inteiros literais são interpretados como do tipo “**int**”. Para mostrar ao compilador que está usando um valor do tipo “**long**” inclua a letra “**L**” no final do número literal: `long x = 725L;`

- **float**: armazena um número real (ponto flutuante) com sinal, ocupando 4 bytes (32 bits) na memória. Pode armazenar valores entre **1,4E-37** a **3,4E+38**. Por padrão, no Java, os números reais (ponto flutuante) são interpretados como do tipo “**double**”, para mostrar ao compilador que está usando um valor do tipo “**float**” inclua a letra “**F**” no final do número literal: `float altura = 1.75F`;

- **double**: armazena um número real (ponto flutuante) com sinal, ocupando 8 bytes (64 bits) na memória. Pode armazenar valores entre **4,9e-324** a **1,7e+308**.

A faixa de valores dos tipos inteiros são calculadas elevando o número 2 (base binária) pela quantidade de bits do tipo menos 1 (um bit é usado para definir o sinal do número: positivo ou negativo). O lado positivo será esse valor menos um, pois o número zero é interpretado como positivo no computador. Assim:

- **byte**: 2<sup>7</sup> = 128
- **short**: 2<sup>15</sup> = 32.768
- **int**: 2<sup>31</sup> = 2.147.483.648
- **long**: 2<sup>63</sup> = 9.223.372.036.854.775.808
