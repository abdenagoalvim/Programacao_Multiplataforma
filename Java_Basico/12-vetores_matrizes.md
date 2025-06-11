# Vetores / Matrizes

Vetor/matriz é uma estrutura de dados que armazena uma coleção de valores de um mesmo tipo, são armazenados de forma contíguas na memória e podem ser acessados por um índice numérico, normalmente iniciado por zero “**0**”. Os colchetes **[]** são usados para especificar o índice desejado.

Cada posição de um **array** é acessada através do nome do **array** acompanhado do índice da posição entre colchetes: `nomeArray[ind]`.


A diferença entre vetor e matriz é a sua dimensão, enquanto o vetor é unidimensional a matriz é multidimensional. Em programação os vetores/matrizes também são conhecidos com “**arrays**”. Uma matriz também pode ser chamada de um vetor de vetores.

A declaração de um **array** deverá ser feita indicando o tipo de dados a ser armazenado no **array** seguido de colchetes e do seu nome: 

```java
tipo[] nomeArray;
```

Outra forma de declarar um **array** é colocando os colchetes após o seu nome:

```java
tipo nomeArray[];
```
As duas formas são válidas, mas **a primeira é a mais recomendada**. 

Depois de declarar o **array**, precisamos criar ele na memória usando a palavra-chave `new` seguida do tipo de dados do **array** e do seu tamanho (quantos elementos ele terá) entre colchetes:

```java
String[] alunos;
int[] notas;

alunos = new String[5];
notas = new notas[5];
```

Você também pode declarar e criar o **array** na mesma linha:

```java
String[] alunos = new String[5];
int[] notas = new int[5];
```

Nos exemplos, o **array** alunos pode conter 5 nomes (textos) e o **array** notas 5 números inteiros. Os índices dos elementos desses **arrays** variam de 0 a 4.

Você pode atribuir valores a cada posição do **array** através do seu índice:

```java
notas[0] = 7;
notas[1] = 9;
notas[2] = 8;
notas[3] = 5;
notas[4] = 6;
```

Você também pode declarar e preencher um **array** com valores ao mesmo tempo:

```java
int[] notas = {7, 9, 8, 5, 6};
```
Os valores de um **array** também podem ser acessados usando um laço `for`:

```java
for(int i = 0; i < notas.length; i++) {
	System.out.println("Notas[" + i + "]: " + notas[i]);
}
```

O atributo `.length` de um **array** retorna o seu tamanho (quantidade de posições do **array**).

Para declarar uma matriz, basta colocar um par de colchetes para cada dimensão (linhas/colunas) do **array**: 

```java
double[][] notas = new double[5][3];
```

Nesse exemplo será criado um **array** de 5 linhas e 3 colunas para armazenar números reais (com casas decimais). 

Assim como no vetor, você também pode declarar e preencher uma matriz com valores ao mesmo tempo:

```java
double[][] notas = {{7.5, 5.8, 6.5},
		    {9.5, 9.0, 9.8},
		    {7.2, 8.9, 7.5},
		    {5.1, 4.3, 6.5},
		    {6.5, 7.5, 9.0}};
```

Um **array** em Java pode ter múltiplas dimensões (uma (vetor), duas (matriz), três, quatro, cinco...). Teoricamente, não existe um limite para o número de dimensões de um **array** no Java. Entretanto, criar **arrays** com muitas dimensões (acima de três) torna o código difícil de entender, dificultando a compreensão e leitura do código.
