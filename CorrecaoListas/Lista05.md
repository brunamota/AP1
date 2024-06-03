# 1- Escreva um programa que verifica se um número inteiro é par. O programa deve exibir a mensagem "O número é par" se o número for par, e "O número é ímpar" caso contrário.
```c
#include <stdio.h>

int main() {
    int numero;

    printf("Digite um número inteiro: ");
    scanf("%d", &numero);

    if (numero % 2 == 0) {
        printf("O número %d é par.\n", numero);
    } else {
        printf("O número %d é ímpar.\n", numero);
    }

    return 0;
}
```
# 2- Escreva um programa que verifica se um aluno foi aprovado em uma disciplina. O aluno é considerado aprovado se sua média final for maior ou igual a 7 e se ele não tiver faltado mais de 25% das aulas. O programa deve exibir a mensagem "Aluno aprovado" se o aluno satisfazer as duas condições, e "Aluno reprovado" caso contrário.
```c
#include <stdio.h>

int main() {
    float media_final;
    int aulas_totais, aulas_faltadas;

    printf("Digite a média final do aluno: ");
    scanf("%f", &media_final);

    printf("Digite o total de aulas da disciplina: ");
    scanf("%d", &aulas_totais);

    printf("Digite o número de aulas faltadas pelo aluno: ");
    scanf("%d", &aulas_faltadas);

    if (media_final >= 7.0 && aulas_faltadas <= aulas_totais * 0.25) {
        printf("Aluno aprovado.\n");
    } else {
        printf("Aluno reprovado.\n");
    }

    return 0;
}
```
# 3- Escreva um programa que verifica se um aluno foi aprovado em uma disciplina. O aluno é considerado aprovado se sua média final for maior ou igual a 7 e se ele não tiver faltado mais de 25% das aulas. O programa deve exibir a mensagem "Aluno aprovado" se o aluno satisfazer as duas condições, e "Aluno reprovado" caso contrário.
```C
#include <stdio.h>

int main() {
    int ano;

    printf("Digite o ano: ");
    scanf("%d", &ano);

    if ((ano % 4 == 0 && ano % 100 != 0) || ano % 400 == 0) {
        printf("Ano bissexto.\n");
    } else {
        printf("Ano não bissexto.\n");
    }

    return 0;
}
```
