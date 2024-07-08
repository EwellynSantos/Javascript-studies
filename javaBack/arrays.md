# Arrays

O array é uma lista de elementos, e os indices do array sempre começam pelo 0. Além disso, um array em javascript pode conter diversos tipos de elementos e inclusive por ter um array dentro de um array.  E podemos declarar ela assim:

```javascript

const notas = [10, 6.5, 8, 7.5]; //aqui declaramos o array

const media = (notas[0] + notas[1] + notas[2] + notas[3] ) / notas.length;
//aqui estamos acessando os indices de cada nota e fazendo a soma
//logo após estamos dividindo o valor somado pelo tamanho do array, resultando na média


console.log(media);
```





### Método Push: adicionando elementos

O método push é um método de arrays e com ele podemos adicionar elementos ao final dos arrays:

<pre class="language-javascript"><code class="lang-javascript">// Some code

const notas = [10, 6, 8];

<strong>notas.push(7); //usando esse método push, adiconamos o elemento 7 ao array
</strong>
const media = (notas[0] + notas[1] + notas[2] + notas[3] ) / notas.length;

console.log(media);

</code></pre>





### Método Pop: excluindo o ultimo elemento

O método pop tem a função de excluir o ultimo elemento do array, sendo assim, nao precisamos colocar um parametro para ele.

```javascript
// Some code

const notas = [10, 6, 8, 5.5, 10];

notas.pop(); //usando o método pop estamos excluido o elemento 10 do array


const media = (notas[0] + notas[1] + notas[2] + notas[3] ) / notas.length;

console.log(media);

```
