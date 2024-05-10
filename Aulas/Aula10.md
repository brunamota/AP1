**Aula 10: Strings vs. Vetores de Caracteres**

1. Vetores de Caracteres:
   - Um vetor de caracteres é uma variável composta unidimensional que armazena uma sequência de caracteres.
   - Na linguagem C, os vetores de caracteres são declarados especificando o tipo "char" seguido pelo nome do vetor e seu tamanho.
   - Exemplo de declaração de um vetor de caracteres:
     ```C
     char nome[20];
     ```

2. Strings:
   - Strings são sequências de caracteres terminadas por um caractere nulo ('\0').
   - Na linguagem C, as strings são representadas como vetores de caracteres.
   - Exemplo de declaração e inicialização de uma string:
     ```C
     char nome[20] = "John Doe";
     ```

3. Diferenças entre Vetores de Caracteres e Strings:
   - Caractere Nulo: Uma string é sempre terminada por um caractere nulo ('\0'), enquanto um vetor de caracteres pode ou não ter um caractere nulo no final.
   - Manipulação de Strings: A biblioteca string.h oferece várias funções para manipulação de strings, como cópia, concatenação, comparação, entre outras. Os vetores de caracteres não possuem essas funções embutidas e a manipulação deve ser feita manualmente.
   - Inicialização: As strings podem ser inicializadas diretamente durante a declaração, enquanto os vetores de caracteres requerem atribuição manual de caracteres.
   - Comportamento em Funções: Strings podem ser passadas como argumentos para funções diretamente, enquanto os vetores de caracteres são passados como ponteiros para o primeiro elemento.
   - Comparação: Strings podem ser comparadas usando operadores de comparação (==, !=, <, >), enquanto os vetores de caracteres não podem ser comparados diretamente.

4. Exemplos de Uso:
   - Exemplo de uso de um vetor de caracteres:
     ```C
     char nome[20];
     nome[0] = 'J';
     nome[1] = 'o';
     nome[2] = 'h';
     nome[3] = 'n';
     nome[4] = '\0';
     ```

   - Exemplo de uso de uma string:
     ```C
     char nome[20] = "John Doe";
     ```

5. Funções para Manipulação de Strings:
   - A biblioteca string.h fornece diversas funções úteis para manipulação de strings.
   - Exemplo de uso da função strcpy para copiar uma string:
     ```C
     char destino[20];
     char origem[20] = "Hello";
     strcpy(destino, origem);
     ```

