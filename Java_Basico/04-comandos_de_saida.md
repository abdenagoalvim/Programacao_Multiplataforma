# Comandos de Saída

A maioria dos programas de computador, de forma simplificada, possuem três etapas na sua execução: entrada de dados; processamento; saída dos resultados após o processamento dos dados de entrada. Nesse tópico trataremos da 3ª etapa, saída dos resultados, da forma mais padrão, isto é, na tela do computador, também chamado de terminal ou console.

O Java possui a classe “**System**” que possui vários recursos, atributos e métodos, que incluem fluxos de entrada padrão, saída padrão e saída de erro.

A classe “**System**” possui o atributo “**out**” abreviação de **_output_**, que é um objeto pronto para aceitar dados de saída que serão disponibilizados na saída padrão do sistema (terminal, console, tela...). 

O objeto “**out**” é definido a partir da classe “**PrintStream**” que possui a capacidade de imprimir representação de vários valores de dados através dos métodos “**print()**”, “**println()**” e “**printf()**”.

## print()

No Java existem vários métodos “**print()**”, um para cada tipo do Java (**boolean**, **char**, **double**, **float**, **int**, **long**, **String**, **Object**...), através da sobrecarga de métodos (**_overload_**) que é um conceito de **polimorfismo**, um dos pilares da **POO - Programação Orientada a Objetos**, que consiste basicamente, em criar vários métodos com o mesmo nome só que com assinaturas diferentes. Discutiremos mais sobre o **polimorfismo** no conteúdo sobre **POO - Programação Orientada a Objetos**.

O mais importante nesse momento, é entender que o método “**print()**” imprimirá uma string (cadeia de caracteres) na saída padrão do sistema. Essa string será convertida em bytes, usando a codificação de caracteres passa ao construtor, ou usando o **_charset_** padrão. Caso o argumento passado para o método seja nulo (**null**) a string “null” será impressa.  Caso seja passado um outro tipo de dados para o método, o mesmo será convertido em string através do método “**valueOf()**” da classe “**String**”.

### Sintaxe

```java
System.out.print(<arg>);
```

Onde \<**arg**> deverá ser substituído pelo dado que se deseja imprimir na saída padrão do sistema.

### Exemplos

```java
System.out.print(“Olá Mundo!!!”);
System.out.print(725);
Systen,out.print(13.21);
```

## println()

Funciona da mesma forma que o método “**print()**” incluindo um separador de linha após a impressão do argumento passado. Assim, a próxima entrada/saída padrão não ficará na mesma linha impressa por esse método. O separador de linha costuma ser definido pelo caractere “**\n**”. O separador de linha normalmente é definido pela propriedade do sistema “**line.separator**”.

### Sintaxe

```java
System.out.println(<arg>);
```

### Exemplos

```java
System.out.print(“Olá Mundo!!!”);
System.out.print(725);
Systen,out.print(13.21);
```

Compare as saídas desses exemplos com as saídas dos exemplos do método “**print()**” para clarear a diferença entre os dois métodos.

## printf()

O método “**printf()**” é usado para escrever uma string formatada no fluxo de saída padrão do sistema. Ela deve receber uma string de formato e os argumentos para substituir os elementos da string de formato. 

### Sintaxe

```java
System.out.format(formato, args);
```

### Parâmetros

**formato**: Uma string de formato conforme descrito abaixo.

**args**: Argumentos referenciados pelos especificadores de formato na string de formato. Se houver mais argumentos do que os especificadores de formato, os argumentos excedentes serão ignorados.

### String de formato

A string de formato é uma cadeia de caracteres que pode conter texto fixo e um ou mais especificadores de formato.

#### Sintaxe dos especificadores de formato

```java
%[arg_indice$][flags][tam][.precisão]conversão
```

onde:

**arg_indice**: (opcional) é um inteiro que indica a posição do argumento na posição do argumento na lista de argumentos. O primeiro argumento é referenciado por “**1$**”, o segundo por “**2$**” etc. 

**flags**: (opcional) são um conjunto de caracteres que modificam o formato da saída. O conjunto de flags válidos depende da conversão. 

**tam**: (opcional) um número inteiro que indica o mínimo de caracteres gerados na saída. 

**precisão**: (opcional) um número inteiro usado para restringir a quantidade de casas decimais usadas em números de ponto flutuante.

**conversão**: (necessário) um caractere que indica o conteúdo a ser inserido na saída.

Veja algumas das conversões que podem ser usadas:

|Conversão|Descrição|
|---|---|
|c|Caractere simples (char)|
|s|Cadeia de caracteres (String)|
|d|Inteiro decimal (int)|
|f|Real em ponto flutuante (float ou double)|
|%|Caractere “%”|
|n|Separador de linha|

Para mais especificadores de formato, consulte a classe “[**Formatter**](https://docs.oracle.com/en/java/javase/23/docs/api/java.base/java/util/Formatter.html#syntax)” na documentação do Java.

### Exemplos

```java
System.out.printf(“O resultado é %d%n”, 21);
System.out.printf(“O resultado é %.2f\n”, 5.42513);
System.out.printf(“Olá, %s, seja bem-vindo!!!”, “José”);
System.out.printf(“%-20s|%10.2f\n”,”Caneta”, 2.1);
```

Os exemplos acima estão trabalhando com valores literais como argumentos a serem usados na string de formato do método “**printf()**”. Nos próximos tópicos você aprenderá a usar variáveis e poderá usá-las como argumentos também.

No último exemplo estão sendo usados dois especificadores com mais detalhes:

**%-20s**: resultara em uma string de 20 caracteres, no mínimo, com o texto passado como argumento alinhado à esquerda. Quando é definido um tamanho para a saída, normalmente o alinhamento, do argumento passado, ocorre do lado direito. Nesse caso está sendo usado a flag “-“ indicando o alinhamento à esquerda.

**%10.2f**: resultara em uma string de 10 caracteres no mínimo, com um número de real (ponto flutuante) com duas casas decimais alinhado à direita.

Veja os resultados gerados pelos exemplos acima:

```
O resultado é 21
O resultado é 5,43
Caneta              |      2,10
Olá, José, seja bem-vindo!!!
```

