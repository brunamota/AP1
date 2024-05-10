# Aula 11: Variáveis Compostas Unidimensionais (Matrizes)

### Matrizes:
Matrizes são variáveis compostas unidimensionais que podem armazenar um conjunto de elementos do mesmo tipo em duas dimensões.
Na linguagem C, a declaração de uma matriz é feita especificando o tipo dos elementos seguido pelo nome da matriz e o número de linhas e colunas entre colchetes.
 - Exemplo de declaração de uma matriz do tipo int com 3 linhas e 4 colunas:
     ```
     int matriz[3][4];
     ```

### Acesso aos Elementos de uma Matriz:
Os elementos de uma matriz são acessados por meio de índices de linha e coluna.
O primeiro elemento de uma matriz tem índice [0][0].
- Exemplo de acesso aos elementos de uma matriz:
     ```
     matriz[0][0] = 10;    // atribui o valor 10 ao primeiro elemento
     int valor = matriz[2][3];    // atribui o valor do elemento na terceira linha e quarta coluna à variável 'valor'
     ```

### Inicialização de Matrizes:
As matrizes podem ser inicializadas simultaneamente à sua declaração, especificando os valores dos elementos entre chaves.
- Exemplo de inicialização de uma matriz:
     ```
     int matriz[3][4] = {{1, 2, 3, 4},
                         {5, 6, 7, 8},
                         {9, 10, 11, 12}};
     ```

### Percorrendo uma Matriz:
É comum percorrer os elementos de uma matriz usando loops aninhados, como o for, para percorrer cada linha e coluna.
- Exemplo de percorrer uma matriz e exibir seus elementos:
     ```
     for (int i = 0; i < 3; i++) {
         for (int j = 0; j < 4; j++) {
             printf("%d ", matriz[i][j]);
         }
         printf("\n");    // imprime uma nova linha após cada linha da matriz
     }
     ```

### Matrizes Irregulares:
Em C, é possível criar matrizes irregulares, onde cada linha pode ter um número diferente de colunas.
Para usar matrizes irregulares, é necessário alocar memória dinamicamente para cada linha.
- Exemplo de declaração e uso de uma matriz irregular:
     ```
     int** matrizIrregular;
     int numLinhas = 3;
     matrizIrregular = (int**)malloc(numLinhas * sizeof(int*));
     matrizIrregular[0] = (int*)malloc(2 * sizeof(int));
     matrizIrregular[1] = (int*)malloc(3 * sizeof(int));
     matrizIrregular[2] = (int*)malloc(4 * sizeof(int));
     ```

