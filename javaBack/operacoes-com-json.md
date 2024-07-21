# Operações com JSON



### Convertendo em String (stringify)

Para que possamos manipular os dados do json no front e no back, normalmente nós convertemos o conteudo em string e depois mandamos para o front ou back. E para mandarmos utilizamos requisiçoes HTTP. Vejamos como podemos converter esse dados utilizando o método stringify.

```javascript
//aqui importamos o arquivo estudante.json e atribuimos a variavel estudante
const estudante = require('./estudante.json'); //agr ele é um obj js

//aqui utilizamos o método JSON.stringify na variavel estudante, que possui o obj js
const stringEstudante = JSON.stringify(estudante);

console.log(stringEstudante);
console.log(typeof stringEstudante);

Resultados:
{"nome":"Ana","idade":32,"cpf":"23423423423","email":"ana@email.com","telefones":["551198745632","551198745633"],"endereco":{"rua":"Rua Joseph Climber","numero":"45","complemento":"apto 43"}}
string
```

<mark style="color:blue;">**O que houve?**</mark>

Veja que o primeiro resultado contém diversas string que estão em uma única linha. No segundo resultado confirmamos que o tipo desse conteudo é string.

OBS: enquanto ele é uma string, os métodos não funcionarão nele. Exemplo, quero agora ver o valor da pripriedade nome, não será possivel. Para que possamos acessar, precisamos converter as strings json em um obj.



### Convertendo em Objeto (parse)

Quando recebemos então um json em string, para que possamos manipular os dados que estão nele, precisamos converter ele em objeto, e para isso usaremos a função parse do JSON.&#x20;

```javascript
//aqui importamos e transformamos em obj js
const estudante = require('./estudante.json');

//aqui estamos convertendo em string
const stringEstudante = JSON.stringify(estudante);

Parte2

//aqui utilizamos o JSON.parse para transformar a string em um objeto novamente.
const objEstudante = JSON.parse(stringEstudante);//aqui atribuimos ao objEstudante

console.log(objEstudante);
console.log(typeof objEstudante);

Resultados:
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

na parte 2 do código estamos usando o método JSON.parse para transfomar a string stringEstudante em um objeto js. Atribuimos então o objeto a variavel objEstudante e quando analisamos o tipo, é objeto, como esperavamos. Sendo assim, agora conseguimos utilizar os métodos normais do objeto, podendo acessar propriedades e afins.&#x20;
