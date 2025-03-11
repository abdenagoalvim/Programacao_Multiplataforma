# Comandos de Entrada

Como foi visto no tópico **“Comandos de Saída**” no início desse material, a maioria dos programas de computadores deve receber entrada de dados, do usuário, para que sejam processados. Uma das formas de obter entradas é a partir do teclado. No Java, a forma mais básica de receber dados a partir do teclado, em uma aplicação do tipo console/terminal, é a partir do comando:

```java
System.in.read();
```

Entretanto, esse comando, apesar de básico, não é tão simples para fazer a leitura de dados. Pois, esse comando lê caractere a caractere, sendo retornado um inteiro que representa o código ASCII do caractere lido. O que tornaria bem complexo, leituras simples como um texto, um número inteiro ou um número real.

Para facilitar a leitura de dados a partir do teclado, em programas do tipo consolo/terminal, o Java disponibiliza a classe “**Scanner**” do pacote “**java.util**”.

Como definido pela documentação do Java, um objeto da classe “**Scanner**” é um scanner (digitalizador) de texto simples que pode analisar tipos primitivos e strings. Ele quebra a sua entrada em tokens usando um delimitador padrão, normalmente espaços em branco, e converte esses tokens em valores de diferentes tipos conforme o método usado.

## Passos para usar a classe Scanner

Para usar a classe “**Scanner**” e ler dados de entrada a partir do teclado, você precisa seguir alguns passos:

1. Importar a classe “**Scanner**”

    ```java
    Import java.util.Scanner;
    ```

    A importação deve ser feita no início do arquivo “**.java**” que usará a classe.

2. Criar um objeto da classe “**Scanner**”

    ```java
    Scanner sc = new Scanner(System.in)
    ```

    Onde:

    - “**sc**” é o nome da variável que armazenará o objeto do tipo “**Scanner**”. Poderia ser qualquer outro nome como: teclado, entrada, banana, abacaxi...

    - “**System.in**” é o dispositivo padrão do sistema, normalmente o teclado.

3.	Ler os valores do teclado usando o método apropriado ao tipo de valor a ser lido.

    - ```sc.nextBoolean()``` – lê o próximo token da entrada como um **boolean**;
    - ```sc.nextByte()``` – lê o próximo token da entrada como um **byte**;
    - ```sc.nextShort()``` – lê o próximo token da entrada como um **short**;
    - ```sc.nextInt()``` – lê o próximo token da entrada como um **int**;
    - ```sc.nextLong()``` – lê o próximo token da entrada como um **long**;
    - ```sc.nextFloat()``` – lê o próximo token da entrada como um **float**;
    - ```sc.nextDouble()``` – lê o próximo token da entrada como um **double**;
    - ```sc.nextLine()``` – lê o próximo token da entrada como uma **string** (até a tecla [**ENTER**] ser pressionada);
    - ```sc.next()``` – lê o próximo token da entrada como uma **string** (até a tecla [**ENTER**] ser pressionada), mas diferente do método “**nextLine()**” lê somente a primeira palavra (até o primeiro espaço ser encontrado).

4.	Fechar o objeto Scanner

    ```java
    sc.close(); 
    ```

## Exemplo

```java
package exemplos;

import java.util.Scanner;

public class ExemplosEntrada {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		String nome = sc.nextLine();
		char c = sc.next().charAt(0);
		int i = sc.nextInt();
		double d = sc.nextDouble();
		
		System.out.println(nome);
		System.out.println(c);
		System.out.println(i);
		System.out.println(d);
		
		sc.close();
	}

}
```

Repare, no exemplo, que a classe “**Scanner**” não possui um método para leitura de um único caractere. Quando é necessário ler um único caractere deve usar o método “**next()**” e usar o método “**charAt()**” da classe “**String**” para pegar o primeiro caractere (índice zero “**0**”) da string retornada.

