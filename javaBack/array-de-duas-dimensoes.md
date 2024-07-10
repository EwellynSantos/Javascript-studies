# Array de duas dimensões

Um array de duas dimenções é um array que contém mais de um array.  E para que possamos acessar os arrays dentro do array, devemos seguir essa sintaxe:

```
arrayNovo[indiceArray que quer acessar][indiceDado que voce quer acessar]
```

Ou seja, se voce tem mais de um array dentro do array prinicpal, para acessar as informações dos arrays secindários voce precisa indicar o indice do array secundario e o indice do dado que devesa visualizar do array secundário.

Para que entenda melhor, veja o exemplo abaixo:

```javascript
// Some code


const alunos = ['Joao', 'Lucas', 'Bruno', 'Millena'];
const media = [10, 8, 7.5, 9];

//aqui estamos criando um array que contém dois arrays, alunos e media
const lista = [alunos, media];
//ele ficará assim: [ [ 'Joao', 'Lucas', 'Bruno', 'Millena' ], [ 10, 8, 7.5, 9 ] ]

//aqui declaramos o indice 0 que é a posição do primeiro array e o depois declaramos
//o indice 1 do dado que queremos ver dentro do array que escolhemos
console.log(`o aluno da posição 1 da lista é: ${lista[0][1]}, a nota desse aluno é ${lista[1][1]}`)

//Resultado: o aluno da posição 1 da lista é: Lucas, a nota desse aluno é 8
```
