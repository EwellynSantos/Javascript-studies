# Operadores



### Operações

&#x20;**=**  operador de atribuição

**+=**  operador de incremento



| Operador | definição     |                                                                                                                                                   |
| -------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| =        | atribuição    |                                                                                                                                                   |
| +=       | incremento    |                                                                                                                                                   |
| +        | soma          |                                                                                                                                                   |
| -        | subtração     |                                                                                                                                                   |
| /        | divisão       |                                                                                                                                                   |
| \*       | multiplicação |                                                                                                                                                   |
| ===      | comparação    |                                                                                                                                                   |
| \|\|     | or (ou)       | O operador \|\| (OU lógico) retorna `true` se pelo menos um dos operandos for `true`. Retorna `false` apenas se ambos os operandos forem `false`. |
| &&       | and (e)       | O operador && (E lógico) retorna true apenas se ambos os operandos forem true. Caso contrário, retorna false.                                     |
| !        | not           | Se o operando for `true`, `!` retorna `false`. Se o operando for `false`, `!` retorna `true`.                                                     |



### Precedência de operações

```
// Some code

*  >  /  >  +  >  -
```





### Operador ternário

operador ternário é composto por uma variavel que possui uma condição.

como por exemplo:

```javascript
// Some code

const valor = 50;
const texto = valor < 50 ? ‘valor insuficiente’ : ‘valor suficiente’; //<- operador ternário
console.log(texto); // retorna ‘valor suficiente’

//a sintax é:

//condição ?      caso 'true'    :     caso 'false'
valor < 50 ? 'valor insuficiente' : 'valor suficiente';

```

ou seja, se o valor for menor que 50 entao( ? ) retorna "valor insuficiente", se nao( : ) retorna "valor suficiente"

O operador ternário é normalmente utilizado em substituição ao `if…else` em que as condições têm apenas uma linha de retorno.
