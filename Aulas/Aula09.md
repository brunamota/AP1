# Aula 9: Variáveis Compostas Unidimensionais

### Arrays:

Os arrays são variáveis compostas unidimensionais que podem armazenar um conjunto de elementos do mesmo tipo.
Na linguagem C, a declaração de um array é feita especificando o tipo dos elementos seguido pelo nome do array e o número de elementos entre colchetes. Exemplo de declaração de um array do tipo int com 5 elementos:
```C
int numeros[5];
```

### Índices de Arrays:

Os elementos de um array são acessados por meio de índices.
O primeiro elemento de um array tem índice 0, o segundo tem índice 1 e assim por diante. Exemplo de acesso aos elementos de um array:
```C
numeros[0] = 10;    // atribui o valor 10 ao primeiro elemento
int valor = numeros[2];    // atribui o valor do terceiro elemento à variável 'valor'
```

### Inicialização de Arrays:
Os arrays podem ser inicializados simultaneamente à sua declaração. Exemplo de inicialização de um array:
```C
int numeros[5] = {1, 2, 3, 4, 5};
```

### Percorrendo um Array:
É comum percorrer os elementos de um array usando loops, como o for. Exemplo de percorrer um array e exibir seus elementos:
```C
for (int i = 0; i < 5; i++) {
    printf("%d ", numeros[i]);
}
```

### Funções para Manipulação de Strings:
A biblioteca string.h fornece diversas funções úteis para manipulação de strings, como strcpy, strcat, strlen, entre outras.
Exemplo de uso da função strcpy para copiar uma string:

```C
char destino[20];
char origem[20] = "Hello";
strcpy(destino, origem);
```

### Código feito em sala

```C
int main()
{
    //criação de vetores
    //vetor sem valores pré-definidos
    float nota[3], soma = 0;

    //insere 3 valores no veto nota
    for(int i = 0; i < 3; i++){
        printf("digite 3 notas do aluno x: ");
        scanf("%f", &nota[i]);
    }
    
    //mostra as notas em cada um das posições
    printf("Notas do aluno x:\n");
    for(int i = 0; i < 3; i++){
        printf("Nota %d: %.2f\n", i+1, nota[i]);
    }

    //soma os valores das notas inseridas no vetor
    for(int i = 0; i < 3; i++){
        soma = soma + nota[i];
    }

    float media = soma/3;
    
    printf("Media do aluno x: %.2f", media);
}
```
