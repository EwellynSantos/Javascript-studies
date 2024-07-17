# clonando arrays: Spred Operator

O Spred Operator tem como função abrir o array e "espalhar" os elementos, desse modo voce cria uma cópia de um array, e por essa cópia estar aberta, cove pode adicionar valores a ela. Mas quando clonamos um array, precisamos ter atenção, pois dependendo do modo que fazemos, podemos acabar criando um referencia para aquele array ao invés de clonar. E é importante se atentar pois quando mudamos valores na refencia do array, ele também altera no array original.

Como **não** devemos fazer:

```javascript
const listaOriginal = [6, 9, 8, 10];
const novaLista = listaOriginal; //aqui estamos criando apenas uma referencia

novaLista.push(10); //quando alteramos o novaLista, ele também altera a listaOriginal

console.log(listaOriginal);
console.log(novaLista);

//Resultado: 
//[ 6, 9, 8, 10, 10 ]
//[ 6, 9, 8, 10, 10 ]
```

Desse modo estamos criando um referencia, entao apesar de alterar o valor na novaLista, por ele ser um refencia, na verdade estaremos alterando a própria listaOriginal.

Para que de fato possamos criar uma cópia, devemos utilizar o Spred Operator.

### Como devemos fazer:

<pre class="language-javascript"><code class="lang-javascript">const listaOriginal = [6, 9, 8, 10];
const novaLista = [...listaOriginal]; //aqui utilizamos o Spred Operator
//ou seja, estamos criando uma copia com base na listaOriginal

novaLista.push(10); //se alterar valores na cópia, ela nao reflete no array original

console.log(listaOriginal);
console.log(novaLista);

//Resultado:
<strong>//[ 6, 9, 8, 10 ]
</strong>//[ 6, 9, 8, 10, 10 ]
</code></pre>

uma outra maneira de já adicionar um valor ao novo array:

```javascript
const listaOriginal = [6, 9, 8, 10];
const novaLista = [...listaOriginal, 10]; //aqui ja adicionamos o elemento 10

console.log(listaOriginal);
console.log(novaLista);

//Resultado:
//[ 6, 9, 8, 10 ]
//[ 6, 9, 8, 10, 10 ]
```
