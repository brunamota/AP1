1- Escreva um algoritmo em formato de pseudocódigo que receba o nome e a idade de uma pessoa e exiba uma mensagem de saudação com o nome e a idade informados.

``` C
   Variáveis:
      nome: string
      idade: inteiro

   Leia nome
   Leia idade

   Escreva "Olá, " + nome + "! Você tem " + idade + " anos."
```
2- Faça um fluxograma de um algoritmo que receba um número inteiro e verifique se ele é positivo. Exiba uma mensagem correspondente.
3- Crie um pseudocódigo que exiba os números pares de 1 a 20.
``` C
   Para i de 1 até 20 faça
      Se i % 2 = 0 então
         Escreva i
      FimSe
   FimPara
```
4- Elabore um fluxograma que receba a nota de um aluno em uma disciplina e exiba a situação do aluno de acordo com as seguintes regras:
   - Se a nota for maior ou igual a 7, exiba "Aprovado".
   - Se a nota for menor que 7 e maior ou igual a 5, exiba "Recuperação".
   - Se a nota for menor que 5, exiba "Reprovado".
5- Desenvolva um pseudocódigo que solicite ao usuário que digite números inteiros positivos. Em seguida, exiba a soma dos números.
``` C
   Variáveis:
      numero: inteiro
      soma: inteiro

   soma <- 0
   Leia numero

   Enquanto numero >= 0 faça
      soma <- soma + numero
      Leia numero
   FimEnquanto

   Escreva "A soma dos números é: " + soma
```
