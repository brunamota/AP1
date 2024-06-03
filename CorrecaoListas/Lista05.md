# Lista 5 - Operadores lógicos e Expressões lógicas

### 1- Escreva um programa que verifica se um número inteiro é par. O programa deve exibir a mensagem "O número é par" se o número for par, e "O número é ímpar" caso contrário.
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
### 2- Escreva um programa que verifica se um aluno foi aprovado em uma disciplina. O aluno é considerado aprovado se sua média final for maior ou igual a 7 e se ele não tiver faltado mais de 25% das aulas. O programa deve exibir a mensagem "Aluno aprovado" se o aluno satisfazer as duas condições, e "Aluno reprovado" caso contrário.
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
### 3- Escreva um programa que verifica se um aluno foi aprovado em uma disciplina. O aluno é considerado aprovado se sua média final for maior ou igual a 7 e se ele não tiver faltado mais de 25% das aulas. O programa deve exibir a mensagem "Aluno aprovado" se o aluno satisfazer as duas condições, e "Aluno reprovado" caso contrário.
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
### 4- Escreva um programa que verifica se uma pessoa pode dirigir um carro. Para poder dirigir, a pessoa deve ter idade igual ou superior a 18 anos e possuir uma carteira de motorista válida. O programa deve exibir a mensagem "Pode dirigir" se a pessoa satisfizer as duas condições, e "Não pode dirigir" caso contrário.
```C
#include <stdio.h>

int main() {
    int idade;
    int tem_carteira;

    printf("Digite a idade da pessoa: ");
    scanf("%d", &idade);

    printf("A pessoa possui carteira de motorista válida? (1 - Sim, 0 - Não) ");
    scanf("%d", &tem_carteira);

    if (idade >= 18 && tem_carteira == 1) {
        printf("Pode dirigir.\n");
    } else {
        printf("Não pode dirigir.\n");
    }

    return 0;
}
```

### 5- Utilize o calculo do IMC feito na lista 03, mas agora verifique se a pessoa está no peso ideal.

- Parâmetros:

    - IMC < 18,5 Classificação: MAGREZA
    
    - 18,5 <= IMC <=  24,9  Classificação:   NORMAL
    
    - 25,0 <= IMC <=  29,9  Classificação:   SOBREPESO 
    
    - 30,0  <= IMC <=  39,9   Classificação:  OBESIDADE
    
    - IMC >= 40,0  Classificação:  OBESIDADE GRAVE
```c
#include <stdio.h>
#include <math.h>

int main() {
    float peso, altura, imc;

    printf("Digite o peso da pessoa (em kg): ");
    scanf("%f", &peso);

    printf("Digite a altura da pessoa (em metros): ");
    scanf("%f", &altura);

    imc = peso / (altura * altura);

    printf("O IMC da pessoa é: %.2f\n", imc);

    if (imc < 18.5) {
        printf("Classificação: MAGREZA\n");
    } else if (imc >= 18.5 && imc <= 24.9) {
        printf("Classificação: NORMAL\n");
    } else if (imc >= 25.0 && imc <= 29.9) {
        printf("Classificação: SOBREPESO\n");
    } else if (imc >= 30.0 && imc <= 39.9) {
        printf("Classificação: OBESIDADE\n");
    } else {
        printf("Classificação: OBESIDADE GRAVE\n");
    }

    return 0;
}
```
