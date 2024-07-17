# ForEach

O forEach é uma função de callback, que é quando uma função chama outra função dentro de si. O forEach tem um sintaxe simples, nao precisando criar parametros de inici, execução e incremento. Segue a sintaxe:

```javascript
// Some code

array.forEach(function(parametro){
        
})
```

Pra que possa entender melhor, segue o exemplo:

```javascript
// Some code

const notas = [10, 9, 7, 6];

let somaNotas = 0;

//no array notas usamos a função forEach
//O forEach usa como parametro uma função e essa função possui um parametro nota
notas.forEach(function (nota) {
    //a cada execução o forEach atribui os valores do array no parametro nota
    somaNotas += nota;
})

//por fim obtemos a média
const media = somaNotas / notas.length;

console.log (`a media é: ${media}`)

//Resultado: a media é: 8

```

Nós também podemos fazer o forEach separado da function. Veja como:\


```javascript
// Some code
const notas = [10, 9, 7, 6];

let somaNotas = 0;

//aqui inicamos o forEach atribuindo como paramentro a função arrayNotas
notas.forEach(arrayNotas)

//aqui delaramos a função arrayNotas
function arrayNotas(nota) {
    somaNotas += nota;
}

const media = somaNotas / notas.length;

console.log (`a media é: ${media}`)


//Resultado: a media é: 8

```
