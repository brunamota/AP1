# Lista 4 - Estrutura Sequencial/Boas práticas de programação

### 1- Escreva um programa em C que solicite ao usuário o valor principal, a taxa de juros anual e o período de tempo em anos. Em seguida, calcule e exiba o valor final com base na fórmula de juros compostos: $VF = P$ * $(1 + r)^n$. Em que VF é o valor final, P é o valor principal, r é a taxa de juros e n é o número de períodos.

```C
#include <stdio.h>
#include <math.h>

int main() {
    float valorPrincipal, taxaJuros, valorFinal;
    int periodo;

    printf("Digite o valor principal: ");
    scanf("%f", &valorPrincipal);

    printf("Digite a taxa de juros anual (em decimal): ");
    scanf("%f", &taxaJuros);

    printf("Digite o período de tempo em anos: ");
    scanf("%d", &periodo);

    // Cálculo do valor final com juros compostos
    valorFinal = valorPrincipal * pow(1 + taxaJuros, periodo);

    printf("Valor final: %.2f\n", valorFinal);
}
```

### Crie um programa em C que solicite ao usuário o valor de um produto e a porcentagem de desconto a ser aplicada. Calcule e exiba o valor final do produto com o desconto aplicado.
```C
#include <stdio.h>

int main() {
    float valorProduto, percentualDesconto, valorFinal;

    printf("Digite o valor do produto: ");
    scanf("%f", &valorProduto);

    printf("Digite a porcentagem de desconto: ");
    scanf("%f", &percentualDesconto);

    // Cálculo do valor final com desconto
    valorFinal = valorProduto - (valorProduto * percentualDesconto / 100.0);

    printf("Valor final do produto com desconto: %.2f\n", valorFinal);
}
```

### Desenvolva um programa em C que converta uma determinada quantia em reais para dólares. Solicite ao usuário o valor em reais e o valor do dólar atual. Faça o cálculo da conversão e exiba o resultado na tela.
```C
#include <stdio.h>

int main() {
    float valorReais, valorDolar, valorConvertido;

    printf("Digite o valor em reais: ");
    scanf("%f", &valorReais);

    printf("Digite o valor do dólar atual: ");
    scanf("%f", &valorDolar);

    // Conversão de reais para dólares
    valorConvertido = valorReais / valorDolar;

    printf("Valor convertido em dólares: %.2f\n", valorConvertido);
}
```

### Escreva um programa em C que solicite ao usuário as idades de três pessoas e calcule a média das idades. Em seguida, exiba o resultado na tela. Dica: Utilize variáveis do tipo inteiro para armazenar as idades e uma variável do tipo float para calcular a média. Certifique-se de utilizar mensagens claras para solicitar as idades ao usuário e exiba a média das idades com uma mensagem adequada na tela.
```C
#include <stdio.h>

int main() {
    int idade1, idade2, idade3;
    float media;

    printf("Digite a idade da primeira pessoa: ");
    scanf("%d", &idade1);

    printf("Digite a idade da segunda pessoa: ");
    scanf("%d", &idade2);

    printf("Digite a idade da terceira pessoa: ");
    scanf("%d", &idade3);

    // Cálculo da média das idades
    media = (idade1 + idade2 + idade3) / 3.0;

    printf("A média das idades é: %.2f\n", media);

    return 0;
}
```
