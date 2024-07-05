# Type: number

O tipo number, como já diz o nome, é para números, sejam eles int, float além de outros tipos.

```javascript
// Some code

const nome = ‘Camila’; // variável global

function cumprimentar() {
  console.log(`Olá, ${nome}!`); // Acessa a var global
}

cumprimentar(); // ‘Olá, Camila!”

```



Para casos que voce queira transformar uma string em um number, voce pode utilizar o **parseInt:**

<pre class="language-javascript"><code class="lang-javascript">// Some code

const um = 8;
const dois = 6.3;
<strong>const tres = Number.parseInt('5');
</strong>
const total = um + dois + tres;

console.log(total)

</code></pre>



### Tipos



Int: números inteiros

```javascript
// Some code

let numeroInteiro = 10;
console.log(numeroInteiro); // Saída: 10

```



Float: números com ponto flutuante

```javascript
// Some code

let numeroFlutuante = 3.14;
console.log(numeroFlutuante); // Saída: 3.14

```



Hexadecimal: números representados na base 16

```javascript
// Some code

let numHex = 0xA; // Representa o número 10 em hexadecimal
console.log(numHex); // Saída: 10

```



Octais: podem ser representados usando o prefixo 0o seguido do valor&#x20;

```javascript
// Some code

let numOctal = 0o10; // Isso representa o número 8 em octal
console.log(numOctal); // Saída: 8

```

