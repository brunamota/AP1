# Lista 10 - 

1. Escreva um programa que leia uma matriz 4x4 e imprima o maior elemento da matriz.
```C
#include <stdio.h>

int main() {
    int matriz[4][4];
    int maior = 0;

    // Leitura da matriz
    printf("Digite os 16 elementos da matriz (4x4):\n");aa
    for (int i = 0; i < 4; i++) {
        for (int j = 0; j < 4; j++) {
            scanf("%d", &matriz[i][j]);
            if (matriz[i][j] > maior) {
                maior = matriz[i][j];
            }
        }
    }

    printf("O maior elemento da matriz é: %d\n", maior);
}
```
2. Escreva um programa que leia uma matriz 3x3 e um número, e verifique se esse número está presente na matriz.
```C
#include <stdio.h>

int main() {
    int matriz[3][3];
    int numero;
    int encontrado = 0;

    // Leitura da matriz
    printf("Digite os 9 elementos da matriz (3x3):\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            scanf("%d", &matriz[i][j]);
        }
    }

    // Leitura do número a ser procurado
    printf("Digite o número a ser procurado: ");
    scanf("%d", &numero);

    // Verificação da presença do número na matriz
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            if (matriz[i][j] == numero) {
                encontrado = 1;
                printf("O número %d está presente na matriz.\n", numero);
                break;
            }
        }
        if (encontrado) {
            break;
        }
    }

    if (!encontrado) {
        printf("O número %d não está presente na matriz.\n", numero);
    }
}
```
3. Escreva um programa que leia uma matriz 3x3 em que cada linha da matriz leia e armazena um nome.

```C
#include <stdio.h>
#include <string.h>

int main() {
    char nomes[3][50];
    int i, j;

    // Leitura dos nomes
    printf("Digite 3 nomes:\n");
    for (i = 0; i < 3; i++) {
        printf("Nome %d: ", i + 1);
        setbuf(stdin, NULL);
        gets(nomes[i]);
    }

    // Exibição da matriz de nomes
    printf("\nMatriz de nomes:\n");
    for (int i = 0; i < 3; i++) {
        printf("Nome %d: %s\n", i+1, nomes[i]);
        printf("\n");
    }
}
```

4. Escreva um programa que leia uma matriz 3x4 em que cada linha seja um aluno e cada coluna uma nota, no fim faça a média de cada aluno.
``` C
#include <stdio.h>

int main() {
    float matriz[3][4];
    float media[3];

    // Leitura da matriz de notas
    printf("Digite as 12 notas (4 notas para cada aluno):\n");
    for (int i = 0; i < 3; i++) {
        printf("Aluno %d:\n", i + 1);
        for (int j = 0; j < COLS; j++) {
            scanf("%f", &matriz[i][j]);
        }
    }

    // Cálculo da média de cada aluno
    for (int i = 0; i < 3; i++) {
        float soma = 0.0;
        for (int j = 0; j < 4; j++) {
            soma += matriz[i][j];
        }
        media[i] = soma / 4;
    }

    // Exibição das médias
    printf("\nMédias dos alunos:\n");
    for (int i = 0; i < 3; i++) {
        printf("Aluno %d: %.2f\n", i + 1, media[i]);
    }
}
```

5. Escreva um programa que leia uma matriz 3x3 e imprima os valores de forma organizada.

```C
#include <stdio.h>

int main() {
    int matriz[3][3];
    int maior = 0;

    // Leitura da matriz
    printf("Digite os 9 elementos da matriz (3x3):\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            scanf("%d", &matriz[i][j]);
        }
    }

    // Printar matriz
    printf("Matriz organizada:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("[%d] ", matriz[i][j]);
        }
        printf("\n");
    }
}
```

