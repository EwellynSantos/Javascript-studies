# Método reduce

O reduce é uma função que  reduz todos os elementos de um array  a um único valor.  O reduce também é um método callback, entao ele retorna uma function.&#x20;

<div align="left">

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

</div>

Veja um exemplo fácil:

```javascript
//a questão aqui é que o acumulador é onde estaremos armazenando os 
//valores temporáriamente, e o atual é o elemento do momento(o atual passa em cada 
//elemento como um for), e então adicionamos o elemento atual ao acumulador
//

const numeros = [1, 2, 3, 4, 5]

const soma = numeros.reduce((acumulador, atual) => {
    const total = acumulador + atual;
    
    return total
}, 10)//aqui definimos um valor inicial ao acumulador, entao ele começa assim: 10 + atual
        //se nao definir valor, ele inicia como zero

console.log(soma) //resultado: 15
```

Segue abaixo um exemplo:

```javascript
const salaJS = [6, 9, 8, 10];
const salaJava = [8, 7, 9, 3];
const slaPython = [8, 8, 1, 6];

//aqui criamos uma função com o parametro listaNotas
function calcMedia(listaNotas) {
    // aqui declaramos que o listaNotas recebera o reduce, onde teremos o acumulador
    //que é o que o próprio nome diz, e receberemos as notas
    const somaNotas = listaNotas.reduce((acumulador, nota) => {
        //aqui estamos somando a nota ao acumulador, ele vao acumular todos valores
        return acumulador + nota;
        //o 0 é pra indicar o valor inicial, como receberemos números, colocamos o 0
    }, 0);
    //ainda dentro da função nós calculamos a média e retonamos o valor
    const media = somaNotas / listaNotas.length;
    return media;
}

console.log(calcMedia(salaJS));
console.log(calcMedia(salaJava));
console.log(calcMedia(slaPython));

//Resultado: 
//8.25
//6.75
//5.75

```

A ideia é que pudéssemos calcular todas as médias, e dessa maneira, o array que passásemos como parametro seria calculado.&#x20;



uma maneira de fazer resumidamente:

```javascript

const salaJS = [6, 9, 8, 10];
const salaJava = [8, 7, 9, 3];
const slaPython = [8, 8, 1, 6];

function calcMedia(listaNotas) {
    // nos tiramos as chaves ({}) o returno e o ponto e virgula.
    const somaNotas = listaNotas.reduce((acumulador, nota) => acumulador + nota, 0);

    const media = somaNotas / listaNotas.length;
    return media;
}

console.log(calcMedia(salaJS));
console.log(calcMedia(salaJava));
console.log(calcMedia(slaPython));
```

Dessa maneira fica melhor de visualizar o reduce, pois definimos tudo em uma linha só.\
\
