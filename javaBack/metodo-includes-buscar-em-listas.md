# Metodo includes(buscar em listas)

O método includes é utilizado para buscar valores em arrays, e ele retorna true or false.&#x20;

Exemplo:\


```javascript
// Some code
//aqui temos 2 arrays
const alunos = ['Joao', 'Lucas', 'Bruno', 'Millena'];
const media = [10, 8, 7.5, 9];

//aqui estamos criando um array de duas dimensões
const lista = [alunos, media];


//essa função recebe como pararametro o aluno
function exibeNomeENota(aluno) {
//aqui acessamos a lista de indice 0 e buscamos pelo aluno
    if(lista[0].includes(aluno)) {
    //aqui usamos o indexOf para retornar o indice do do aluno na lista do indice 0
        const indice = lista[0].indexOf(aluno);
        //aqui acessamos a lista de indice 1 e buscamos o valor com base no indice
        const mediaAluno = lista[1][indice];
        console.log(`${aluno} tem a média ${mediaAluno}`);
    } else {
        console.log('Estudante não existe na lista')
    }
}

//aqui chamamos a função passando os valores
exibeNomeENota('Lucas');
exibeNomeENota('mi');


//Resultados:
//Lucas tem a média 8
//Estudante não existe na lista
```

Ou seja, nos criamos uma função onde temos uma condição de que se aquele aluno estiver incluso na lista com indice 0, então indetificamos o indice do aluno com o indexOf e  e usamos para obter a média dele. Assim imprimidos o aluno e a média.
