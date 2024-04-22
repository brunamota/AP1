# Aula 6: Operadores Lógicos e Expressões Lógicas

### Operadores Lógicos:

Os operadores lógicos são utilizados para combinar ou negar expressões lógicas.Na linguagem C, os principais operadores lógicos são:
- E lógico (&&): Retorna verdadeiro se ambas as expressões forem verdadeiras.

| A | && | B |
|   :---:  |   :---:  |   :---:  |
| V | V | V |
| V | F | F |
| F | F | V |
| F | F | F |

- OU lógico (||): Retorna verdadeiro se pelo menos uma das expressões for verdadeira.

| A | \|\| | B |
|   :---:  |   :---:  |   :---:  |
| V | V | V |
| V | v | F |
| F | v | V |
| F | F | F |

- NÃO lógico (!): Inverte o valor da expressão, se for verdadeira, torna-se falsa e vice-versa.

### Expressões Lógicas:

As expressões lógicas são combinações de valores e operadores lógicos que resultam em um valor verdadeiro ou falso (booleano). Podemos utilizar operadores de comparação para criar expressões lógicas, tais como:
- Igual a (==): Verifica se dois valores são iguais.
- Diferente de (!=): Verifica se dois valores são diferentes.
- Maior que (>), Maior ou igual a (>=), Menor que (<), Menor ou igual a (<=): Comparação numérica.
- Exemplo de expressão lógica: idade > 18 && salario < 1000.

### Estrutura de Decisão:

- A estrutura de decisão permite que o programa tome diferentes caminhos com base nas condições estabelecidas. Na linguagem C, a estrutura de decisão mais comum é o "if-else", que avalia uma expressão lógica e executa um bloco de código caso a condição seja verdadeira e outro bloco de código caso a condição seja falsa.

#### Exemplo:
``` C
if (idade >= 18) {
    printf("Você é maior de idade.\n");
} else {
    printf("Você é menor de idade.\n");
}
```

### Estrutura de Decisão Encadeada:

É possível encadear múltiplas estruturas "if-else" para lidar com diferentes condições.

#### Exemplo:

``` C
if (idade < 13) {
    printf("Você é uma criança.\n");
} else if (idade < 18) {
    printf("Você é um adolescente.\n");
} else {
    printf("Você é um adulto.\n");
}
```

### Operador Ternário:

O operador ternário é uma forma abreviada de escrever uma estrutura de decisão simples.
- Sintaxe: expressão ? valor_verdadeiro : valor_falso

#### Exemplo:
``` C
printf((idade >= 18) ? "Você é maior de idade.\n" : "Você é menor de idade.\n");
```
