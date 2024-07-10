# Operadores de incremento

i++ e ++i são ambos operadores de incremento usados para aumentar o valor de uma variável i em 1. No entanto, a diferença entre eles está na forma como o aumento é aplicado e quando o valor é retornado.



### i++

O operador `i++` é conhecido como pós-incremento. Ele primeiro retorna o valor atual de `i` e depois incrementa `i` em 1 unidade. Ou seja, o valor atual de `i` é usado na expressão em que `i++` está presente, e após isso, `i` é aumentado em 1.

Exemplo:

```javascript
let i = 5;
console.log(i++); // Saída: 5 (retorna o valor atual de i)
console.log(i);   // Saída: 6 (i foi incrementado após a execução)
```

### ++i

O operador `++`i é conhecido como pré-incremento. Ele primeiro incrementa `i` em 1 unidade e depois retorna o novo valor de `i`. Ou seja, o valor de i é incrementado imediatamente, e então o valor atualizado é usado na expressão em que `++i` está presente.

Exemplo:

```javascript
// Some code

let j = 8;
console.log(++j); // Saída: 9 (j foi incrementado antes de ser usado)
console.log(j);   // Saída: 9 (j já foi incrementado)
```
