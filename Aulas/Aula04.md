# Aula 4 - Estrutura Sequencial

### Estrutura Sequencial:

A estrutura sequencial é a base de qualquer programa. As instruções são executadas em ordem, de cima para baixo, uma após a outra. É como seguir um conjunto de passos em uma receita, onde cada passo deve ser executado na ordem correta.

### Exemplos de Instruções:

As instruções podem ser comandos simples ou expressões que realizam alguma operação.
Alguns exemplos comuns de instruções são:
- Atribuição de valores a variáveis.
- Cálculos matemáticos.
- Chamadas de funções.
- Entrada e saída de dados.

### Exemplo Prático:

Vamos criar um programa simples que solicita ao usuário dois números e exibe a soma deles.
- Passo a passo:
  - Solicitar ao usuário que digite o primeiro número.
  - Ler o número digitado e armazená-lo em uma variável.
  - Solicitar ao usuário que digite o segundo número.
  - Ler o número digitado e armazená-lo em outra variável.
  - Calcular a soma dos dois números.
  - Exibir o resultado da soma na tela.

### Exemplo de Código em C:
``` C
#include <stdio.h>
#include <stdlib.h>

int main() {
    int num1, num2, soma;

    printf("Digite o primeiro número: ");
    scanf("%d", &num1);

    printf("Digite o segundo número: ");
    scanf("%d", &num2);

    soma = num1 + num2;

    printf("A soma é: %d\n", soma);

    return 0;
}
```

### Conclusão:
Nesta aula, exploramos a estrutura sequencial, que consiste em executar instruções em ordem, uma após a outra. Vimos um exemplo prático de um programa simples que solicita dois números e exibe a soma deles. A estrutura sequencial é a base para o desenvolvimento de algoritmos mais complexos. Na próxima aula, vamos explorar a estrutura de decisão. Até lá!
