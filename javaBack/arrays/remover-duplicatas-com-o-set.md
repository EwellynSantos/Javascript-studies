# Remover duplicatas com o Set

Set é um conjunto, e o conjunto é um tipo de dado que armazena valores unicos. O set é um dado chamado de array like, isso porque ele parece um array, mas ele não é um array. Então todos os métodos que usamos para arrays nao funcionarão para o Set.&#x20;

segue abaixo um exemplo:

```javascript
const nomesDuplicados = ['ana', 'maria', 'jose', 'millena', 'lucas', 'lucas', 'lucas'];

//aqui passamos o valores do array pro Set, como o set é uma lista que armazena
//valores unicos, então nao haverá valores duplicados. 
const nomesAtualizados = new Set(nomesDuplicados);

console.log(nomesAtualizados);

//Resultado: Set(5) { 'ana', 'maria', 'jose', 'millena', 'lucas' }
```

No caso de queremos usar essa lista de valores unicos, precisamos então transformar esse conjunto em um array.

E para transformar podemos utilizar o **Spred Operator**, que criará uma cópia desse conjunto:

```javascript
const nomesDuplicados = ['ana', 'maria', 'jose', 'millena', 'lucas', 'lucas', 'lucas'];

const nomesAtualizados = new Set(nomesDuplicados);
//aqui criamos uma variavel e passamos uma cópia do conjunto utilizanso o spred
const listaNomesAtualizados = [...nomesAtualizados]

console.log(listaNomesAtualizados);
```

Dessa maneira podemos utilizar todos os métodos que sabemos no array listaNomesAtualizados.



Uma maneira reduzida desse código:

```javascript
// Some code

const nomesDuplicados = ['ana', 'maria', 'jose', 'millena', 'lucas', 'lucas', 'lucas'];

//aqui utilizamos o set para criar um conjunto com valores unicos e já usamos o spred
const listaNomesAtualizados = [...new Set (nomesAtualizados)];

console.log(listaNomesAtualizados);

```
