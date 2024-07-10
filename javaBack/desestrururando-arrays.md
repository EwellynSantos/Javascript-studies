# Desestrururando Arrays

Para casos em que nós criamos listas contendo listas, nós podemos desestrurura-las da seguinte maneira:

```javascript
// lista1 e lista2 são as listas que nós temos dentro da lista pricipal.
//colocando no código dessa maneira, desestruturamos a lista principal.
[lista1, lista2] = listaPrincipal;
```

Lembrando que sempre olhamos da direita pra esquerda, ou seja, a lista principal agora será desestruturada em 2 listas, a lista1 e lista2. De acordo com a ordem, cada indice irá pra sua nova lista.

Exemplo:\


```javascript
const alunos = ['Joao', 'Lucas', 'Bruno', 'Millena'];
const media = [10, 8, 7.5, 9];

const lista = [alunos, media];

function exibeNomeENota(aluno) {
    if(lista[0].includes(aluno)) {
    //aqui desestruturamos o array lista, entao a parti do array listas,
    //estamos criando 2 novos arrays chamados alunos e medias.
    //ps: poderia ser qualquer outro nome 
        const [alunos, medias] = lista;
        const indice = alunos.indexOf(aluno);
        const mediaAluno = medias[indice];
        console.log(`${aluno} tem a média ${mediaAluno}`);
    } else {
        console.log('Estudante não existe na lista')
    }
}

exibeNomeENota('Lucas');
exibeNomeENota('mi');
```
