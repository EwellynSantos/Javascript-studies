# Concatenando arrays

O método concat é utilizado para concatenar arrays. importante saber que o contat nao altera os arrays, ele apenas cria um novo array.

A sintaxe é:

```javascript
array1.concat(array2)
```

Exemplo:

<pre class="language-javascript"><code class="lang-javascript">const sala1 = ['Joao', 'Bruno', 'Lucas', 'Millena'];
const sala2 = ['Ana', 'Amanda', 'Jhow', 'Leonardo'];

//aqui estou criando um novo array slasUnificadas contendo a junção de sala1 e sala2
const salasUnificadas = sala1.concat(sala2);
console.log(salasUnificadas);

//Resultado:
<strong>//['Joao',  'Bruno', 'Lucas', 'Millena', 'Ana', 'Amanda', 'Jhow',  'Leonardo']
</strong>
</code></pre>
