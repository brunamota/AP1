# Lista 9 - Strings e Vetores de Caracteres

1. Implementar um programa que leia uma frase do usuário e execute as seguintes tarefas:

   a) Contar o número de palavras na frase.

   b) Contar o número de caracteres na frase.

   c) Exibir a frase com todas as palavras em maiúsculas.

   d) Exibir a frase com todas as palavras em minúsculas.

``` C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char frase[500];
    int count = 0;

    printf("Digite uma frase: ");
    gets(frase);

    // Contagem de palavras
    for (int i = 0; frase[i]; i++) {
        if (isspace(frase[i])) {
            count++;
        }
    }
    count++; // Última palavra não é contada no loop

    printf("Número de palavras: %d\n", count);
    printf("Número de caracteres: %d\n", strlen(frase));

    // Frase em maiúsculas
    printf("Frase em maiúsculas: %s\n", strupr(frase));

    // Frase em minúsculas
    printf("Frase em minúsculas: %s\n", strlwr(frase));

    printf("\n");

}

```

2. Implementar um programa que leia uma string do usuário e execute as seguintes tarefas:

   a) Inverter a ordem dos caracteres da string.

   b) Verificar se a string é um palíndromo (uma palavra, número ou outra sequência de caracteres que lê da mesma forma tanto da esquerda para a direita quanto da direita para a esquerda).
   
``` C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {

    char palavra[100], palindromo[100];
    int i, igual = 0;

    printf("Digite uma palavra: ");
    scanf("%s", palavra);

    int tamanho = strlen(palavra);

    for(i = 0; i < tamanho; i++){
        palindromo[i] = palavra[tamanho - 1 - i];
    }
    palindromo[i] = '\0';

    printf("Original: %s\nInverso: %s\n", palavra, palindromo);

    for (i = 0; i < tamanho; i++){
        if(tolower(palavra[i]) == tolower(palindromo[i])){
            igual++;
        }
    }
    if(tamanho == igual){
        printf("%s eh palindroma\n", palavra);
    }else{
        printf("%s nao eh palindroma\n", palavra);
    }
}
```

3. Implementar um programa que leia uma string do usuário e execute as seguintes tarefas:

   a) Remover os espaços da string. 

   b) Substituir todas as ocorrências de uma determinada letra por outra '*'.

```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>


int main() {
    char palavra[100];
    char caractere, separador;
    int i,j;

    // Ler a string do usuário
    printf("Digite uma string: ");
    gets(palavra);

    // Remover os espaços da string
    j = 0;
    for (i = 0; palavra[i]; i++) {
        if (!isspace(palavra[i])) {
            palavra[j++] = palavra[i];

        }
    }
    palavra[j] = '\0';

    printf("String sem espaço: %s\n", palavra);

    printf("Digite uma string: ");
    gets(palavra);

    // Substituir todas as ocorrências de uma determinada letra por '*'
    printf("Qual letra deseja substituir por '*'? ");
    scanf(" %c", &caractere);
    for (i = 0; palavra[i]; i++) {
        if (tolower(palavra[i]) == tolower(caractere)) {
            palavra[i] = '*';
        }
    }

    printf("String modificada: %s\n", palavra);

}

```

4. Implementar um programa que leia uma string do usuário e execute as seguintes tarefas:

   a) Remover todas as vogais da string.

   b) Contar o número de vogais na string.

   c) Substituir todas as vogais por um caractere especificado pelo usuário.

```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>


int main() {
    char palavra[100];
    int i, j, numeroVogais = 0;

    // Ler a string do usuário
    printf("Digite uma string: ");
    gets(palavra);

    // Remover todas as vogais da string
    j = 0;
    for (i = 0; palavra[i]; i++) {
        if (tolower(palavra[i]) != 'a' && tolower(palavra[i]) != 'e' &&
            tolower(palavra[i]) != 'i' && tolower(palavra[i]) != 'o' &&
            tolower(palavra[i]) != 'u') {
            palavra[j++] = palavra[i];
        } else {
            numeroVogais++;
        }
    }
    palavra[j] = '\0';

    printf("String modificada: %s\n", palavra);
    printf("Numero de vogais: %d\n", numeroVogais);

    return 0;
}
```
