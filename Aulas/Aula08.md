# Aula 8: While, Do-While e For

### Estrutura de Repetição While:
A estrutura de repetição while é utilizada para executar um bloco de código enquanto uma condição for verdadeira.

- Sintaxe:
```C
while (condicao) {
    // bloco de codigo a ser repetido enquanto a condicao for verdadeira
}
```

### Estrutura de Repetição Do-While:

A estrutura de repetição do-while é utilizada para executar um bloco de código pelo menos uma vez e repeti-lo enquanto uma condição for verdadeira.

- Sintaxe:
```C
do {
    // bloco de codigo a ser repetido
} while (condicao);
```

### Estrutura de Repetição For:

A estrutura de repetição for é utilizada para executar um bloco de código um número específico de vezes.

- Sintaxe:

``` C
for (inicializacao; condicao; incremento) {
    // bloco de codigo a ser repetido
}
```
A inicialização é utilizada para configurar uma variável de controle.
A condição é verificada a cada iteração e determina se o bloco de código deve ser repetido.
O incremento é utilizado para atualizar a variável de controle a cada iteração.

### Palavras-chave break e continue:
- A palavra-chave "break" é utilizada para interromper a execução do loop imediatamente, passando para a próxima instrução após o loop.
- A palavra-chave "continue" é utilizada para interromper a execução da iteração atual do loop e passar para a próxima iteração.

### Exemplos de Uso:
- Exemplo de uso do while:
```C
int contador = 0;
while (contador < 5) {
    printf("%d\n", contador);
    contador++;
}
```
- Exemplo de uso do do-while:
```C
int contador = 0;
do {
    printf("%d\n", contador);
    contador++;
} while (contador < 5);
```
- Exemplo de uso do for:
```C
for (int i = 0; i < 5; i++) {
    printf("%d\n", i);
}
```
