# Aula 3 - Dados primitivos, atribuição, variáveis simples, constantes, entrada/saída de dados

A linguagem C possui quatro tipos básicos de dados, conhecidos como tipos primitivos: int, float, char e double. Esses tipos são amplamente suportados pelo hardware da maioria dos computadores.

Ao declarar uma variável em C, são especificados dois elementos:
- A quantidade de armazenamento necessária para os objetos criados com esse tipo. Por exemplo, uma variável do tipo int precisa de espaço suficiente para armazenar o maior valor inteiro possível.
- A forma como os dados representados por sequências de bits devem ser interpretados. Os mesmos bits em uma determinada posição de armazenamento podem ser interpretados como um número inteiro ou de ponto flutuante, resultando em dois valores numéricos distintos.
A declaração de variável tem o propósito de reservar espaço na memória para um objeto do tipo especificado e permite que esse objeto seja acessado por meio de um identificador (nome) atribuído à variável declarada.

#### Declaração de Variáreis em C:
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
