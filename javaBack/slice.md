# Slice

O slice é um método utilizado para dividir um array e criar novos  arrays com base nele. Para utilizar ele precisamos devemos seguir a sintaxe:

```javascript
array.slice(inicio, fim)

```

segue abaixo um exemplo:

<pre class="language-javascript"><code class="lang-javascript">//o objetivo é dividir o array listaAlunos por 2 e criar 2 novos arrays


const listaAlunos = ['Joao', 'Bruno', 'Lucas', 'Millena', 'Ana', 'Amanda', 'Jhow', 'Leonardo'];

//neste slice o incio é o indice 0 e o fim é a metade da lista
//ps: quando dividimos, o slice nao peda o ultimo indice para incluir no primeiro array
const sala1 = listaAlunos.slice(0, listaAlunos.length/2);

//neste slice, como queremos a outra metade do array então o inicio é a metade do array
const sala2 = listaAlunos.slice(listaAlunos.length/2);

console.log(sala1);
console.log(sala2);

//Resultados:
<strong>//[ 'Joao', 'Bruno', 'Lucas', 'Millena' ]
</strong><strong>//[ 'Ana', 'Amanda', 'Jhow', 'Leonardo' ]
</strong>
</code></pre>
