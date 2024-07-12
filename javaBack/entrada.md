# Entrada

Para que voce possa atribuir valores digitados no terminal a uma variavel, voce pode usar o módulo readline-sync. a sintaxe é:

```javascript
//aqui voce está atribuindo o módulo readline-sync a variavel readlineSync
const readlineSync = require('readline-sync');

//aqui voce cria a variavel que receberá o valor digitado, que seria o input
//logo depois utilizamos a const contendo o módulo e com ele usamos o método question
//o método question será utilizado para imprimir a pergunta no terminal
const input = readlineSync.question('Digite algo: ');

//e aqui imprimimos o que voce digitou 
console.log(`Você digitou: ${i}`);


```

