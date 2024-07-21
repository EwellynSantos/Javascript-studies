# Métodos de objeto

### Object.key

o método object keys <mark style="color:yellow;">**retorna um array de string**</mark> contendo todas as chaves do objeto, ou seja, as propriedades. E dessa maneira podemos utilizar métodos de arrays no array de chaves que é retornado. Segue abaixo um exemplo:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    media: 7.5,
    estaAprovado: function(mediaBase){
        return this.media >= mediaBase ? true : false
    }  
};

//aqui estamos chamando o método object.keys que retorna um array de chaves do obj
const chaveObjeto = Object.keys(estudante);
console.log(chaveObjeto);

//aqui utilizamos o includes que é um método de array para verificar se o obj inclui
//a string/chave enderecos
if (!chaveObjeto.includes('enderecos')) {
    //aqui usamos o console.error para imprimir o erro.
    console.error('é necessário ter um endereço cadastrado')
}

//Resultados:
//[ 'nome', 'idade', 'cpf', 'media', 'estaAprovado' ]
//é necessário ter um endereço

```



### Um pouco mais sobre métodos

<mark style="color:yellow;">`Object.keys()`</mark> e <mark style="color:yellow;">`Object.values()`</mark>: são usados para extrair informações específicas de um objeto. Esses métodos fornecem, respectivamente, as chaves e os valores presentes em um objeto. São úteis para iterar ou fazer operações específicas em conjuntos de dados de um objeto.

O <mark style="color:yellow;">**Object.keys**</mark>, nós vimos que extrai as chaves/propriedades do objeto. Enquanto isso, O <mark style="color:yellow;">**Object.values**</mark> retorna os valores do objetos.

```js
const meuObjeto = { a: 1, b: 2, c: 3 };
const chaves = Object.keys(meuObjeto);
const valores = Object.values(meuObjeto);

console.log(chaves); // Saída: ['a', 'b', 'c']
console.log(valores); // Saída: [1, 2, 3]
```



<mark style="color:yellow;">`Object.entries()`</mark>: este método retorna um array de arrays que representam pares chave-valor. É útil em situações que demandam iterações mais complexas ou manipulação mais minuciosa dos dados.

```js
const meuObjeto = { a: 1, b: 2, c: 3 };
const entradas = Object.entries(meuObjeto);

console.log(entradas);
// Saída: [['a', 1], ['b', 2], ['c', 3]]

```

<mark style="color:yellow;">`Object.assign()`</mark>: usado para fusão e cópia de objetos. Este método permite combinar propriedades de diferentes objetos em um único objeto.

```js
const objetoOriginal = { a: 1, b: 2 };
const objetoParaCopiar = { b: 3, c: 4 };

const objetoFusionado = Object.assign({}, objetoOriginal, objetoParaCopiar);

console.log(objetoFusionado);
// Saída: { a: 1, b: 3, c: 4 }
```

Acesse o MDN e saiba mais:

[https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Working\_with\_Objects](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Working\_with\_Objects)
