1. Escreva um programa em C que leia 5 números reais e os armazene em um vetor. Calcule e imprima a média desses números.
   
```C
#include <stdio.h>

#define QUANTIDADE_NUMEROS 5

int main() {
    float numeros[QUANTIDADE_NUMEROS];
    float soma = 0.0f;
    int i;

    // Leitura dos números
    printf("Digite %d números reais:\n", QUANTIDADE_NUMEROS);
    for (i = 0; i < QUANTIDADE_NUMEROS; i++) {
        printf("Número %d: ", i + 1);
        scanf("%f", &numeros[i]);
        soma += numeros[i];
    }

    // Cálculo da média
    float media = soma / QUANTIDADE_NUMEROS;

    // Impressão da média
    printf("A média dos números é: %.2f\n", media);

    return 0;
}
```

2. Escreva um programa em C que leia 8 números inteiros e os armazene em um vetor. Encontre e imprima o maior e o menor elemento do vetor.
```C
#include <stdio.h>

int main() {
    int numeros[8];
    int i, max, min;

    // Leitura dos números
    printf("Digite 8 números inteiros:\n");
    for (i = 0; i < 8; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    // Encontrando o maior e o menor elemento
    max = numeros[0];
    min = numeros[0];
    for (i = 1; i < 8; i++) {
        if (numeros[i] > max) {
            max = numeros[i];
        }
        if (numeros[i] < min) {
            min = numeros[i];
        }
    }

    // Impressão do maior e do menor elemento
    printf("O maior elemento é: %d\n", max);
    printf("O menor elemento é: %d\n", min);

    return 0;
}

```
3. Escreva um programa em C que leia 10 números inteiros e os armazene em um vetor. Procure um determinado número no vetor e, caso ele seja encontrado, imprima a sua posição. Caso contrário, imprima uma mensagem informando que o número não foi encontrado.
   
```C
#include <stdio.h>


int main() {
    int numero[10];
    int i, numeroEscolhido, numeroIgual = 0,posicao = -1;

    // Leitura dos números
    printf("Digite 10 números inteiros:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numero[i]);
    }

    // Solicitação do número a ser procurado
    printf("Digite o número que você deseja procurar: ");
    scanf("%d", &numeroEscolhido);

    // Procurando o número no vetor
    for (i = 0; i < 10; i++) {
        if (numero[i] == numeroEscolhido) {
           numeroIgual = 1;
           posicao = i;
           break;
        }
    }

    // Impressão do resultado
    if (numeroIgual) {
        printf("O número %d foi encontrado na posição %d.\n", numeroEscolhido, posicao);
    } else {
        printf("O número %d não foi encontrado no vetor.\n", numeroEscolhido);
    }

    return 0;
}
```
4. Escreva um programa em C que leia 12 números inteiros e os armazene em um vetor. Crie um novo vetor com o dobro de cada elemento do primeiro vetor e imprima-o.
   
```C
#include <stdio.h>

int main() {
    int numeros[12];
    int dobroNumeros[12];
    int i;

    // Leitura dos números
    printf("Digite 12 números inteiros:\n");
    for (i = 0; i < 12; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    // Criação do novo vetor com o dobro de cada elemento
    for (i = 0; i < 12; i++) {
        dobroNumeros[i] = numeros[i] * 2;
    }

    // Impressão do novo vetor
    printf("O novo vetor é:\n");
    for (i = 0; i < 12; i++) {
        printf("%d ", dobroNumeros[i]);
    }
    printf("\n");
}

```
5. Escreva um programa em C que leia 10 números inteiros e os armazene em um vetor. Em seguida, imprima os elementos do vetor na ordem inversa.
   
```C
#include <stdio.h>

int main() {
    int numeros[10];
    int i;

    // Leitura dos números
    printf("Digite 10 números inteiros:\n");
    for (i = 0; i < 10; i++) {
        printf("Número %d: ", i + 1);
        scanf("%d", &numeros[i]);
    }

    // Impressão dos números na ordem inversa
    printf("Os números na ordem inversa são:\n");
    for (i = 10 - 1; i >= 0; i--) {
        printf("%d ", numeros[i]);
    }
    printf("\n");
}
```
