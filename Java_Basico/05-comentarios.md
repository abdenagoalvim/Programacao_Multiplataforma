# Comentários

Como na maioria das linguagens de programação o Java também permite que você inclua comentários no seu código. Comentários são textos no seu código fonte, que serão ignorados durante a compilação/execução do programa.

Os comentários são extremamente importantes no Desenvolvimento de Sistemas, mas temos que tomar cuidado para não extrapolar, pois a partir de um determinado ponto os comentários passam a prejudicar a legibilidade do código.

Para que os comentários possam ajudar, no lugar de atrapalhar, eles precisam fornecer informações adicionais, isto é, que não estejam no próprio código, além de serem relevantes para um bom entendimento do código.

O Java possui três maneiras de incluir comentário no código fonte: **Comentário de Linha**, **Comentário de Bloco** e **Comentário de Documentação**.

## Comentário de Linha

Os comentários de linha são definidos por um conjunto de duas barras “**//**” sem espaço entre elas. Todo o texto que estiver a direita das barras, até o final da linha, será ignorado pelo compilador.

No Eclipse você pode selecionar várias linhas e pressionar as teclas “**Ctrl+/**” para colocar/retirar comentário de linha para as linhas selecionadas.

### Sintaxe

```java
// <comentário>
```

### Exemplo

```java
// todo o texto dessa linha será ignorado pelo compilador.
Idade = 15; // o texto a partir das barras será ignorado pelo compilador. 
```

## Comentário de Bloco

Quando é necessário fazer um comentário de múltiplas linhas, apesar de você poder iniciar cada linha com um comentário de linha, o mais prático é usar o comentário de bloco. Um comentário de bloco deve ter uma linha em branco antes do comentário e iniciar com uma barra asterisco “**/\***” e finalizar com um asterisco barra “**\*/**”. Tudo que estiver entre esses caracteres será ignorado pelo compilador.

É comum as linhas dentro do comentário de bloco, no Java, iniciar com um asterisco, mas isso não é uma regra. No Eclipse, quando você inicia um comentário de bloco, ele já coloca uma linha em branco com o asterisco e uma linha de finalização do comentário.

Comentários de blocos são muito usados para descrever arquivos, métodos, estrutura de dados etc. Um comentário de bloco deve acompanhar a indentação do código onde ele estiver.

### Sintaxe

```java
/*
 * <comentário>
 */
```

### Exemplo

```java
/*
 * primeira linha de comentário
 * segunda linha de comentário
 * terceira linha de comentário		
 */
```

## Comentário de Documentação

O comentário de documentação é basicamente o mesmo comentário de bloco, porém inicia com uma barra e dois asteriscos “**/\*\***”. Mas também finaliza com um asterisco barra “**\*/**”.

Os comentários de documentão são usados para descrever a especificação do código, descrevendo classes, interfaces, construtores, métodos e campos, mostrando as funcionalidades e regras de negócio do sistema.

Os comentários de documentação são divididos basicamente em duas partes: descrição geral sobre o código e informações especiais usadas pela ferramenta **JavaDoc** na criação da documentação. As informações especiais possuem etiquetas no formato **@nomeEtiqueta**, e tem a finalidade de estruturar melhor a documentação.

Algumas etiquetas pré-definidas são: **@author**, **@version**, **@param**, **@return** entre outras. Consulte a Especificação de Comentário de documentação **JavaDoc** para mais detalhes.

### Sintaxe

```java
/**
 * <comentário>
 */
```

### Exemplo

```java
/**
 * Método principal da aplicação
 * @author Abdenago Alvim
 * @param args
 */
```
