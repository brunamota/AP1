# Lista 3 - Dados primitivos, atribuição, variáveis, constantes, entrada/saída de dados

### 1- Escreva um programa que solicite ao usuário sua idade, e em seguida exiba essa informação na tela.
```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int idade;

    printf("Digite sua idade: ");
    scanf("%i", &idade);

    printf("\nIdade: %i\n", idade);

}
```

### 2- Crie um programa que converta uma temperatura em graus Celsius para Fahrenheit. O usuário deve inserir a temperatura em Celsius e o programa deve exibir o resultado em Fahrenheit.

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    float celsius, fahrenheit;

    printf("Insira a temperatura em Celsius: ");
    scanf("%f", &celsius);

    fahrenheit = (celsius*9/5) + 32;

    printf("Fahrenheit: %.2f", fahrenheit);

}
```

### 3- Escreva um programa que calcule e exiba a área de um retângulo. O usuário deve inserir os valores da base e altura.

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int base, altura, area;

    printf("Digite a altura: ");
    scanf("%d", &altura);

    printf("Digite a base: ");
    scanf("%d", &base);

    area = base*altura;

    printf("Area do quadrado: %d", area);
}
```

### 4- Crie um programa que calcule o IMC (Índice de Massa Corporal) de uma pessoa. O programa deve solicitar ao usuário o peso e a altura, e em seguida exibir o valor do IMC.

```C
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main()
{
    float raio, area;

    const float PI = 3.14;

    printf("Digite o raio: ");
    scanf("%f", &raio);

    area = PI * pow(raio, 2);

    printf("Area da circunferencia: %.2f", area);
}
```

### 5- Escreva um programa que solicite ao usuário dois números inteiros e realize as operações de adição, subtração, multiplicação e divisão entre esses números, exibindo os resultados na tela.
### 6- Crie um programa que calcule a média aritmética de três notas inseridas pelo usuário. O programa deve exibir a média final.
### 7- Escreva um programa que solicite ao usuário o raio de um círculo e calcule a sua área. O programa deve exibir o resultado na tela. Utilize a biblioteca Math.h
### 8- Desenvolva um programa que converta um valor em metros para centímetros e milímetros. O usuário deve inserir o valor em metros, e o programa deve exibir os equivalentes em centímetros e milímetros.
