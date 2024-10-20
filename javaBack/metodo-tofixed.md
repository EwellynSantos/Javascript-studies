# Método toFixed

O método toFixed é usado para fixar numeros decimais(após a virgula). A sintaxe é:



```javascript
resultado.toFixed(quantidade de casas decimais)
```



Por exemplo, quero fixar 2 casar decimais de um resultado, então:

```javascript
const readlineSync = require('readline-sync');

const raio = readlineSync.question('');

const pi = 3.14159;
//aqui faremos o calculo
const formula = (4/3) * pi * raio ** 3;

//aqui estamos fixando 2 casas decimais do resultado
console.log(`VOLUME = ${formula.toFixed(2)}`)

```
