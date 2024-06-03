# Lista 6 - Estrutura condicional simples e compostas

### 1- Escreva um programa que recebe um caractere que representa uma operação matemática (+, -, *, /) e dois números reais. O programa deve realizar a operação selecionada e exibir o resultado. Por exemplo, se o usuário digitar "+", 5 e 3, o programa deve exibir o resultado 8. Utilize estrutura condicional Switch-Case.

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

### 2- Escreva um programa que recebe um número inteiro e verifica se ele é positivo, negativo ou zero. Exiba a mensagem correspondente de acordo com o número inserido.

```c
#include <stdio.h>

int main() {
    int num;

    printf("Digite um número inteiro: ");
    scanf("%d", &num);

    if (num > 0) {
        printf("O número %d é positivo.\n", num);
    } else if (num < 0) {
        printf("O número %d é negativo.\n", num);
    } else {
        printf("O número é zero.\n");
    }

    return 0;
}
```

### 3- Escreva um programa que recebe um número inteiro de 1 a 12 e exibe o nome do mês correspondente. Por exemplo: se o usuário digitar 1, o programa deve exibir "Janeiro", se digitar 2, deve exibir "Fevereiro", e assim por diante. Utilize estrutura condicional Switch-Case.

```c
#include <stdio.h>

int main() {
    int mes;

    printf("Digite um número de 1 a 12 (representando o mês): ");
    scanf("%d", &mes);

    switch (mes) {
        case 1:
            printf("Janeiro\n");
            break;
        case 2:
            printf("Fevereiro\n");
            break;
        case 3:
            printf("Março\n");
            break;
        case 4:
            printf("Abril\n");
            break;
        case 5:
            printf("Maio\n");
            break;
        case 6:
            printf("Junho\n");
            break;
        case 7:
            printf("Julho\n");
            break;
        case 8:
            printf("Agosto\n");
            break;
        case 9:
            printf("Setembro\n");
            break;
        case 10:
            printf("Outubro\n");
            break;
        case 11:
            printf("Novembro\n");
            break;
        case 12:
            printf("Dezembro\n");
            break;
        default:
            printf("Erro: número inválido (deve ser entre 1 e 12).\n");
    }

    return 0;
}
```

### 4- Escreva um programa que recebe o horário atual em horas (0-23) e exibe uma saudação apropriada com base no horário.
- Por exemplo:

  - Se o horário for entre 0 e 11, exiba a mensagem "Bom dia!"

  - Se for entre 12 e 17, exiba a mensagem "Boa tarde!"

  - Caso contrário, exiba a mensagem "Boa noite!".
 
```c
#include <stdio.h>

int main() {
    int hora;

    printf("Digite a hora atual (0-23): ");
    scanf("%d", &hora);

    if (hora >= 0 && hora < 12) {
        printf("Bom dia!\n");
    } else if (hora >= 12 && hora < 18) {
        printf("Boa tarde!\n");
    } else {
        printf("Boa noite!\n");
    }

    return 0;
}
```
### Escreva um programa que recebe um número inteiro de 1 a 5 e exibe uma mensagem correspondente a uma avaliação. Utilize estrutura condicional Switch-Case.

- Por exemplo:

- Se o usuário digitar 1, o programa deve exibir "Péssimo"

- Se digitar 2, deve exibir "Ruim", e assim por diante.

- Se digitar 3, deve exibir "Médio", e assim por diante.

- Se digitar 4, deve exibir "Bom", e assim por diante.

- Se digitar 5, deve exibir "Excelente", e assim por diante.

```c
#include <stdio.h>

int main() {
    int avaliacao;

    printf("Digite um número de 1 a 5 (representando a avaliação): ");
    scanf("%d", &avaliacao);

    switch (avaliacao) {
        case 1:
            printf("Péssimo\n");
            break;
        case 2:
            printf("Ruim\n");
            break;
        case 3:
            printf("Médio\n");
            break;
        case 4:
            printf("Bom\n");
            break;
        case 5:
            printf("Excelente\n");
            break;
        default:
            printf("Erro: número inválido (deve ser entre 1 e 5).\n");
    }

    return 0;
}
```
