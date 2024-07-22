---
description: Java Script Object Notation
---

# Introdução ao JSON

Uma notação de objeto javascript usa como base o objeto do javascript, mas possui algumas diferenças de estrutura.&#x20;

<figure><img src="../.gitbook/assets/image (8).png" alt="" width="563"><figcaption></figcaption></figure>

### Diferenças

* O json não é atribuido a uma variavel, ele nao é um tipo de dado js, ele usa a notação do js;
* As propriedades(o nome delas) obrigatóriamente devem possui aspas duplas;
* O json não utilizam aspas simples, entao strings também devem utilizar aspas duplas;
* O json nao aceita vírgulas sobrando. Ex: colocamos uma vírgula na última propriedade do objeto, mas depois dessa propriedade nao adicionaremos outra propriedade, entao nao pode ter aquela vírgula.



### Sintaxe do JSON

* Funções não são permitidas.&#x20;
* Comentários não são permitidos. Então não é possivel comentar alguma parte do json.
* Suporta apenas tipos primitivos (string, number, boolean, null), arrays e objetos.



### Como importar um arquivo JSON

Utilizaremos o método 'require' que possui a mesma função que o import que nós conhecemos, a diferença é que o require é o método indicado para importar aquivos JSON. Veja:\
\


```javascript
//aqui importamos o arquivo estudante.json e atribuimos a variavel estudante
const estudante = require('./estudante.json'); 

//aqui imprimimos o conteudo da variavel estudante, que agora é um objeto js
console.log(estudante);
console.log(typeof estudante); //o tipo dele será objeto

//Resultados:
{
  nome: 'Ana',
  idade: 32,
  cpf: '23423423423',
  email: 'ana@email.com',
  telefones: [ '551198745632', '551198745633' ],
  endereco: { rua: 'Rua Joseph Climber', numero: '45', complemento: 'apto 43' }
}
object
```

<mark style="color:blue;">**O que houve?**</mark>

Pra que entenda melhor o que houve, aqui está a explicação: Primeiro nós importamos o arquivo estudante,json usando o método require e atribuimos o conteúdo a variável estudante. Quando fizemos isso, transformamos o objeto json que estava no arquivo em um objeto javascript, dessa maneira, agora ele possui as propriedades de um objeto javascript. Ou seja, o objeto json virou um objeto javascript, e nesse momento ele possui todas as funçoes de um objeto normal.&#x20;
