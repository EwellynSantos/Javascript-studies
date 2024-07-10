# For

Laço de reperição for, é utilizado para percorrer listas. Importante lembrar que todos os parametros do for são essenciais para que não tenhamos um loop infinito.

veja sua sintaxe:\


```javascript
// Some code

for (let indice = 0; indice < 10; indice++)

// em let indice = 0, é onde declaramos uma variavel e indicamos por onde 
//vai começar a contagem.

 //em indice < 10, é onde temos a condição, entao nesse caso o loop termina quando 
 //chegar a 9, pois a partir de 10 a condição se torna false
 
 //em indice++, é onde vamos fazer o incremento da variavel que declaramos
 
 ou seja, indice inicia com 0, o loop percorrerá até chegar em 9, e enquanto isso
 estamos incrementando 1 a cada loop.
```

Exemplo:\


```javascript

const notas = [10, 8, 7.5, 9, 6, 8];

//primeira expressão: executada apenas uma vez
//segunda expressão: condição de execução
//terceira expressão: sempre executada ao final do bloco
for (let indice = 0; indice < notas.length; indice++) {
    console.log(indice, notas[indice])
};

//Resultado:
0 10
1 8
2 7.5
3 9
4 6
5 8
```



Outro exemplo:

somando notas e tendo a média com for:\


```javascript

const notas = [10, 8, 7.5, 9, 6, 8];

let somaNotas = 0;

//o for incia com i(indice) 0, a execução sera feita enquanto o i for menos que o 
//tamanho do array notas, e por fim acrescentamos 1 ao indice a cada execução. 
for (let i = 0; i < notas.length; i++){
//aqui somamos a variavel soma notas o conteudo dos indices
    somaNotas += notas[i];
}

const media = somaNotas / notas.length
console.log(media)

//Resultado: 8.083333333333334


```

Ou seja, enquanto o indice for menor que o tamanho do array, o for vai executar, e a cada execução será adiconado 1 ao indice. E enquanto isso, a cada execução nós conferimos o valor do indice atual e somamos a variavel somaNotas
