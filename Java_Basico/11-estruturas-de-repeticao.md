# Estruturas de Repetição

Ao desenvolver um sistema, muitas vezes é necessário repetir um mesmo bloco de código algumas vezes. Para evitar que o programador tenha que, escrever esse mesmo bloco de código diversas vezes, ou copiar e colar, existem as estruturas de repetição, também conhecidas como laços (loops), que permitem que um bloco de código seja executado repetidamente, enquanto uma determinada condição for verdadeira. 

Na maioria das linguagens, as principais estruturas de repetição são: “**while**” e “**for**”. No Java, existe variações dessas estruturas de repetição, possuindo quatro estruturas de repetição: “**while**”, “**do-while**”, “**for**” e “**for-each**”, que serão descritas a seguir.

## Laço WHILE

Repete um bloco de código enquanto uma determinada condição for verdadeira. Normalmente é usado quando não se sabe, previamente, quantas vezes o bloco de código será repetido. 

Outra característica desse laço é a posição da condição que define se o bloco de código continuará sendo executado. Essa condição é posicionada no início do laço, assim, pode acontecer, caso a condição já inicie avaliada como falsa, do bloco de código nunca ser executado.

### Sintaxe

```java
while(condicao){
	//blocoCod
}
```

### Exemplo

```java
Scanner sc = new Scanner(System.in);
int num = 0;
while(num != 7){
	System.out.print("Digite um número: ");
	num = sc.nextInt();
	if (num < 7) {
		System.out.print("Muito pequeno...");
	} else if (num > 7) {
		System.out.print("Muito grande...");
	} else {
		System.out.print("ACERTOU!!!");
	}
}
sc.close();
```

## Laço DO-WHILE

Assim como o laço “**while**”, esse laço repete um bloco de código enquanto uma condição for verdadeira. A diferença é que essa condição é posicionada no final do laço. Dessa forma o bloco de código do laço será executado pelo menos uma vez, mesmo que a condição seja avaliada como falsa no início.

### Sintaxe

```java
do {
	//blocoCod
} while (condicao);
```

### Exemplo

```java
Scanner sc = new Scanner(System.in);
int num = 0;
do {
	System.out.print("Digite um número entre 1 e 5: ");
	num = sc.nextInt();
	if (num < 1 || num > 5){
		System.out.println("Número inválido...");
	}
} while (num < 1 || num > 5);
System.out.println("Número correto!!!");
sc.close();
```

## Laço FOR
O laço “**for**” normalmente é usado quando se sabe, previamente, quantas vezes o bloco de código será repetido. A sintaxe do laço “**for**” facilita a inicialização de uma variável, o seu incremento/decremento e a definição de uma condição de repetição do bloco de código.

### Sintaxe

```java
for(inicializacao; condicao; atualizacao){
	//blocoCod
}
```

### Exemplo

```java
for(int i=1; i<=5; i++){
	System.out.println(i); 
}
```

## Laço FOR-EACH

O laço “**for-each**” é uma variação do laço “**for**” e é usado para facilitar a iteração de um “**array**” ou coleção. Esse laço itera sobre os elementos de um “**array**” de forma automática.

### Sintaxe

```java
for(tipo variavel: array){
	//blocoCod
}
```

### Exemplo
```java
int[] números = {1,2,3,4,5};
for(int numero: numeros) {
	System.out.println(numero);
}
```
