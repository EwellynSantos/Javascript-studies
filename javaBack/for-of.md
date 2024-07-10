# For of

O for of é mais simples, mas também nao podemos definir exatamente como será a execução do nosso loop. Veja um exemplo:

```javascript
const notas = [10, 8, 7, 9, 6, 8];

let somaNotas = 0;

//aqui definimos a variavel que passará pelos indices do array nota
for (let nota of notas){
    //aqui definimos que a cada execução nós somaremos o valor do indice a variavel
    //somaNotas
    somaNotas += nota;
}

const media = somaNotas / notas.length
console.log(media)
```

Ou seja, a cada execução nota acessa um indice, de um a um, do array nota, e a cada execução somamos o valor do indice atual em somaNotas.

Pra ficar mais facil de entender, segue um novo exemplo:

```javascript

const listaCompras = ['banana', 'maça', 'brocolis', 'cenoura'];

let itensCompra = '';

for (let itens of listaCompras){
    itensCompra += itens;
}

console.log(`Minha lista de compras é: ${itensCompra}`)

//Resultado: Minha lista de compras é: bananamaçabrocoliscenoura 

```

Ou seja, temos a listaCompras, criamos a variavel itensCompra que receberá os itens da lista compras, e a cada execução adicionamos os itens a itensCompra.
