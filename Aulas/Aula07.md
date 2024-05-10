# Aula 7: Estruturas Condicionais Simples e Compostas

### Estrutura Condicional Simples:

A estrutura condicional simples é utilizada quando desejamos executar um bloco de código apenas se uma condição for verdadeira.
Na linguagem C, a estrutura condicional simples é representada pelo "if".
- Sintaxe:
``` C
if (condicao) {
    // bloco de codigo a ser executado se a condicao for verdadeira
}
```

### Estrutura Condicional Composta:

A estrutura condicional composta é utilizada quando desejamos executar diferentes blocos de código com base em diferentes condições.
Na linguagem C, a estrutura condicional composta é representada pelo "if-else".
- Sintaxe:

``` C
if (condicao) {
    // bloco de codigo a ser executado se a condicao for verdadeira
} else {
    // bloco de codigo a ser executado se a condicao for falsa
}
```
### Estrutura Condicional Encadeada:

A estrutura condicional encadeada é utilizada quando desejamos testar múltiplas condições e executar diferentes blocos de código com base em cada uma delas.
Na linguagem C, a estrutura condicional encadeada é representada pelo "if-else if-else".
- Sintaxe:
```C
if (condicao1) {
    // bloco de codigo a ser executado se a condicao1 for verdadeira
} else if (condicao2) {
    // bloco de codigo a ser executado se a condicao1 for falsa e a condicao2 for verdadeira
} else {
    // bloco de codigo a ser executado se todas as condicoes anteriores forem falsas
}
```
### Operador Switch:

O operador switch é utilizado quando desejamos testar uma variável em múltiplas condições e executar diferentes blocos de código com base no valor da variável.
Na linguagem C, o operador switch é representado pelo "switch" e "case".
- Sintaxe:
```C
switch (variavel) {
    case valor1:
        // bloco de codigo a ser executado se a variavel for igual a valor1
        break;
    case valor2:
        // bloco de codigo a ser executado se a variavel for igual a valor2
        break;
    default:
        // bloco de codigo a ser executado se a variavel nao corresponder a nenhum dos valores anteriores
}
```
