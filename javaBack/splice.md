# Splice

O método spice é utilizado para deletar elementos específicos e adicionar elementos em um ponto específico do array.



### Deletando

para utilizar o método splice para deletar, seguiremos a sintexe:

```javascript
array.splice(inicio, qtdeElementos)

//no inicio devemos colocar o indice do elemento que vamos iniciar a exclusão
//na qtdeElementos, colocaremos a quantidade de elementos que queremos excluir 
//a partir do indice
```

Exemplo:

<pre class="language-javascript"><code class="lang-javascript">// Some code
const listaAlunos = ['Joao', 'Bruno', 'Lucas', 'Millena', 'Ana', 'Amanda', 'Jhow', 'Leonardo'];

listaAlunos.splice(4, 2)
//inicio: indice  4(ana)
//qtdeElementos 2(ana e amanda)

console.log(listaAlunos);

//Resultado:
<strong>//[ 'Joao', 'Bruno', 'Lucas', 'Millena', 'Jhow', 'Leonardo' ]
</strong></code></pre>



### Adicionando

para utilizar o método, devemos seguir os parametros de dele e por fim adicionar o elemento que voce deseja inserir no lugar dos que voce deletou. Segue a sintaxe:

```javascript
array.splice(inicio, qtdeElementos, 'novoElemento')

//o inicio e qtdeElementos segue as mesmar regras dedeletendo, mas adicionaremos 
//um último parametro, que será o elemento que substituirá aqueles que foram deletados
```

exemplo:

```javascript
const listaAlunos = ['Joao', 'Bruno', 'Lucas', 'Millena', 'Ana', 'Amanda', 'Jhow', 'Leonardo'];

listaAlunos.splice(4, 2, 'Juliana')
//inicio: indice  4(ana)
//qtdeElementos: 2(ana e amanda)
//novoElemento: 'Juliana'

console.log(listaAlunos);

//Resultado:
//['Joao', 'Bruno', 'Lucas', 'Millena', 'Juliana', 'Jhow', 'Leonardo']
```
