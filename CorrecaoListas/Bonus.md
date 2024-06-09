# Bônus - While, Do-While e For

1. Faça um programa usando o do-while + switch-case para criar um menu com as questões da lista:

    a) Escreva um programa que leia a idade de um grupo de pessoas e calcule a média de idade. O programa deve parar de ler as idades quando for digitada uma idade negativa. Use o laço while.

    b) Escreva um programa que leia um número inteiro do usuário e imprima a sequência de Fibonacci até esse número. Use o laço while.

    c) Escreva um programa que leia um número inteiro do usuário e imprima se o número é primo ou não. Use o laço while.

Para o menu você pode optar por usar char ou int.

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int op;
    //variaveis média de idade
    int cont, idade, soma;

    //variaveis fibonacci
    int n, i = 0;
    unsigned long long int primeiro = 0, segundo = 1, proximo;

    //variaveis num primo
    int j = 1, numero, primo=0;

    do{
        printf("\nLista bônus\n");
        printf("1- Media idade de um grupo\n");
        printf("2- Sequência de Fibonacci\n");
        printf("3- Número primo\n");
        printf("Digite zero para sair\n");
        printf("Escolha uma opção: ");
        scanf("%d", &op);

        switch(op){
        case 1:
            cont=0, soma=0;
            printf("Digite a idade %d: ", cont+1);
            scanf("%d", &idade);

            while(idade >= 0){
                cont++;
                soma = soma + idade;
                printf("Digite a idade %d: ", cont+1);
                scanf("%d", &idade);
            }
            printf("\n%d", cont);

            float media;
            media = (float) soma/cont;

            printf("Media de idade do grupo: %.2f", media);
            break;
        case 2:
            printf("Digite o número de termos da sequência de Fibonacci: ");
            scanf("%d", &n);

            printf("Sequência de Fibonacci até o %dº termo:\n", n);

            while (i < n){
                printf("%llu ", primeiro);
                proximo = primeiro + segundo;
                primeiro = segundo;
                segundo = proximo;
                i++;
            }
            break;
        case 3:
            printf("Digite um numero para verificar se ele e primo: ");
            scanf("%d", &numero);
            while (j <= numero){
                if(numero % j == 0){
                    primo++;
                }
                j++;
            }
            if(primo == 2){
                printf("Numero %d eh primo", numero);
            }else{
                printf("Nao eh primo");
            }

            break;
        default:
            if(op == 0){
                printf("Fim da lista\n");
            }else{
                printf("Opcao errada!");
            }
        }
    }while(op!=0);
}
```
