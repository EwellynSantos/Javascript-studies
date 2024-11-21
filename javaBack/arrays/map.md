# Map

O map, assim como o forEach, é uma função de callback da qual podemos acessar os elementos dentro de um array, mas há um grande diferença entre eles, pois o map é um método que retorna, ou seja, os dados capturados são "levados" pra fora, eles são atribuidos para um novo array. Além disso, com o map podemos alterar qualquer valores dos elementos do array inicial, ou seja, o no array conterá os novos elementos. Pra que voce entenda melhor, vou te mostrar a sintaxe:

```javascript
const novoArray = array.map(function (parametro){
    return array//aqui tera a execução;
}) 
```

Aqui está um exemplo pratico:

```javascript
// Some code


const notas = [10, 9, 7, 6];

//aqui criamos uma variavel notasAtualizadas que será um array
//no array notas usamos o método map e usamos como parametro uma função 
//contendo o parametro nota, e logo após retornamos ao notasAtualizadas todos os
//elementos com os seus valores alterados
const notasAtualizadas = notas.map(function (nota){
    return ++nota;
})

console.log(notasAtualizadas);

//resultado: [ 11, 10, 8, 7 ]

```



Um outro exemplo:

```javascript
const nomes = ['ana julia', 'caio vinicios', 'Bia silva'];

const nomesPadronizados = nomes.map((nome) => nome.toUpperCase());

console.log(nomesPadronizados)

//Resultado: [ 'ANA JULIA', 'CAIO VINICIOS', 'BIA SILVA' ]
```

Além disso, o map recebe tres informações, os elementos, os index e o array completo. Veja como é:

```javascript
const numero = [1, 2, 3];

const novoArray = numeros.map((elemento, index, arrayCompleto) => {
    console.log(elemento)
    console.log(index)
    console.log(arrayCompleto)
})

resultado:
//1
1
2
3

//2
0
1
2

//3
[1, 2, 3] //retorna 3 arrays porque ele passou 3 vezes(quantidade de elemetos)
[1, 2, 3] // e imprimiu o arratCompleto nas 3 vezes
[1, 2, 3]

```



<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>
