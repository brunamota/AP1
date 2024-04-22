# Aula 3 - Dados primitivos, atribuição, variáveis simples, constantes, entrada/saída de dados

#### Dados Primitivos:
Os dados primitivos são os tipos básicos de dados disponíveis em uma linguagem de programação. Na linguagem C, os quatro tipos principais são: int, float, char e double.
- O tipo "int" é usado para representar números inteiros, como -3, 0 e 42.
- O tipo "float" é usado para representar números de ponto flutuante, que possuem casas decimais, como 3.14 e -0.5.
- O tipo "char" é usado para representar caracteres individuais, como 'a', '1' e '!'.
- O tipo "double" é usado para representar números de ponto flutuante com maior precisão do que o tipo "float".

#### Atribuição de Valores:

A atribuição é o processo de armazenar um valor em uma variável. Uma variável é um local na memória que pode armazenar dados. Em C, a atribuição é feita usando o operador de atribuição "=", que atribui o valor à direita para a variável à esquerda.
Exemplo:
``` C
int idade = 25; atribui o valor 25 à variável idade.
```
#### Variáveis Simples:

Uma variável é um nome dado a um local na memória onde podemos armazenar dados. Antes de usar uma variável, é necessário declará-la informando seu tipo e nome.
Exemplo:
``` C
int quantidade; declara uma variável chamada quantidade do tipo int.

#### Constantes:

Uma constante é um valor fixo que não pode ser alterado durante a execução do programa. Em C, as constantes são declaradas usando a palavra-chave "const" antes do tipo da constante.
Exemplo:
``` C
const float PI = 3.14; declara uma constante chamada PI do tipo float com valor 3.14.
```

#### Entrada de Dados:

Para receber dados do usuário, podemos utilizar a função "scanf" em C. A função "scanf" permite ler valores digitados pelo usuário e atribuí-los a variáveis.
Exemplo:
``` C
scanf("%d", &idade); lê um valor inteiro digitado pelo usuário e o atribui à variável idade.
```
#### Saída de Dados:

Para exibir informações na tela, podemos utilizar a função "printf" em C. A função "printf" permite exibir mensagens formatadas e valores de variáveis na tela.
Exemplo:
``` C
printf("A idade é %d", idade); exibe a mensagem "A idade é" seguida do valor da variável idade.
```

``` C
//bibliotecas
#include <stdio.h>
#include <stdlib.h>

int main()
{
    //Declaração de Variáveis
    //armazena valores numéricos inteiros
    int numeroInteiro;
    //armazena números com ponto flutuante (reais) com precisão simples.
    float numeroFlutuante;
    //armazena números com ponto flutuante, possui o dobro da capacidade de uma variável do tipo float.
    double numeroFlutuanteMaior;
    //armazena caracteres.
    char caractere;

    //Atribuição de valores

    //Entrada de dados

    printf("\nEscreva um numero inteiro: ");
    scanf("%i", &numeroInteiro);
    printf("\nEscreva um numero decimal: ");
    scanf("%f", &numeroFlutuante);
    printf("\nEscreva um numero decimal grande: ");
    scanf("%f", &numeroFlutuanteMaior);
    printf("\nEscreva um numero caractere: ");
    setbuf(stdin, NULL); //limpar memória
    scanf("%c", &caractere);


    //Saída de Dados
    printf("\nNumero inteiro: %d", numeroInteiro);
    printf("\nNumero decimal: %f", numeroFlutuante);
    printf("\nNumero decimal grande: %f", numeroFlutuanteMaior);
    printf("\nCaractere: %c", caractere);

    //Atribuição de valores
    numeroInteiro = 4;
    numeroFlutuante = 2.0;
    numeroFlutuanteMaior = 200000.36;
    caractere = 'b';

    //Saída de Dados
    printf("\n\nNumero inteiro: %d", numeroInteiro);
    printf("\nNumero decimal: %f", numeroFlutuante);
    printf("\nNumero decimal grande: %f", numeroFlutuanteMaior);
    printf("\nCaractere: %c", caractere);

}
```
#### Conclusão:
Nesta aula, aprendemos sobre dados primitivos, atribuição, variáveis simples, constantes, entrada de dados com "scanf" e saída de dados com "printf". Esses conceitos são fundamentais para manipular informações em um programa. Pratiquem esses conceitos em exercícios e projetos para fortalecer sua compreensão. Na próxima aula, exploraremos estruturas de controle de fluxo. Até lá!
