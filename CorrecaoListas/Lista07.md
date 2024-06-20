# Lista 6 - Estrutura condicional simples e compostas

1. Faça um programa usando o do-while + switch-case para criar um menu com as questões da lista:
    a) Escreva um programa que leia 5 números inteiros e imprima apenas os números pares. Use o laço for.

  b) Escreva um programa que leia 5 números inteiros e imprima o maior e o menor número digitado. Use o laço for.

  c) Escreva um programa que leia um número do usuário e imprima a tabuada desse número. Use o laço for.

Para o menu você pode optar por usar char ou int.

```c
#include <stdio.h>

int main() {
    char op;
    float num1, num2, result;

    printf("Digite a operação matemática (+, -, *, /): ");
    scanf("%c", &op);

    printf("Digite o primeiro número: ");
    scanf("%f", &num1);

    printf("Digite o segundo número: ");
    scanf("%f", &num2);

    switch (op) {
        case '+':
            result = num1 + num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '-':
            result = num1 - num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '*':
            result = num1 * num2;
            printf("Resultado: %.2f\n", result);
            break;
        case '/':
            if (num2 == 0) {
                printf("Erro: divisão por zero!\n");
            } else {
                result = num1 / num2;
                printf("Resultado: %.2f\n", result);
            }
            break;
        default:
            printf("Erro: operação inválida!\n");
    }

    return 0;
}
```
