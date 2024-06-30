# Lista 9 - Strings e Vetores de Caracteres

1. Implementar um programa que leia uma frase do usuário e execute as seguintes tarefas:
    a) Contar o número de palavras na frase.
    b) Contar o número de caracteres na frase.
    c) Exibir a frase com todas as palavras em maiúsculas.
    d) Exibir a frase com todas as palavras em minúsculas.
```C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char frase[100];
    int i, palavras, caracteres;

    // Leitura da frase
    printf("Digite uma frase: ");
    fgets(frase, 100, stdin);

    // Remoção do caractere de nova linha
    frase[strcspn(frase, "\n")] = '\0';

    // Contagem de palavras
    palavras = 1;
    for (i = 0; frase[i]; i++) {
        if (frase[i] == ' ') {
            palavras++;
        }
    }

    // Contagem de caracteres
    caracteres = strlen(frase);

    // Exibição da frase em maiúsculas
    printf("\nFrase em maiúsculas: ");
    for (i = 0; frase[i]; i++) {
        putchar(toupper(frase[i]));
    }
    printf("\n");

    // Exibição da frase em minúsculas
    printf("Frase em minúsculas: ");
    for (i = 0; frase[i]; i++) {
        putchar(tolower(frase[i]));
    }
    printf("\n");

    // Exibição do número de palavras e caracteres
    printf("\nNúmero de palavras: %d\n", palavras);
    printf("Número de caracteres: %d\n", caracteres);

}
```
2. Implementar um programa que leia uma string do usuário e execute as seguintes tarefas:
    a) Inverter a ordem dos caracteres da string.
    b) Verificar se a string é um palíndromo (uma palavra, número ou outra sequência de caracteres que lê da mesma forma tanto da esquerda para a direita quanto da direita para a esquerda).

```C
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
    char str[100];
    char letra_substituir, nova_letra = '*';
    int i, j;

    // Leitura da string
    printf("Digite uma string: ");
    fgets(str, 100, stdin);

    // Remoção do caractere de nova linha
    str[strcspn(str, "\n")] = '\0';

    // Remoção dos espaços
    j = 0;
    for (i = 0; str[i]; i++) {
        if (str[i] != ' ') {
            str[j++] = str[i];
        }
    }
    str[j] = '\0';

    // Substituição da letra
    printf("Digite a letra a ser substituída: ");
    scanf("%c", &letra_substituir);

    for (i = 0; str[i]; i++) {
        if (tolower(str[i]) == tolower(letra_substituir)) {
            str[i] = nova_letra;
        }
    }

    // Exibição da string modificada
    printf("\nString modificada: %s\n", str);

}
```

4. Implementar um programa que leia uma string do usuário e execute as seguintes tarefas:
    a) Remover todas as vogais da string.
    b) Contar o número de vogais na string.
``` C
#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[100];
    int i, j, vogais;

    // Leitura da string
    printf("Digite uma string: ");
    fgets(str, 100, stdin);

    // Remoção do caractere de nova linha
    str[strcspn(str, "\n")] = '\0';

    // Remoção das vogais
    j = 0;
    vogais = 0;
    for (i = 0; str[i]; i++) {
        if (tolower(str[i]) != 'a' && tolower(str[i]) != 'e' &&
            tolower(str[i]) != 'i' && tolower(str[i]) != 'o' &&
            tolower(str[i]) != 'u') {
            str[j++] = str[i];
        } else {
            vogais++;
        }
    }
    str[j] = '\0';

    // Exibição da string modificada
    printf("\nString modificada: %s\n", str);

    // Exibição do número de vogais
    printf("Número de vogais: %d\n", vogais);

}

```

