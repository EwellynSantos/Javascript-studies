# Método filter

como o nome diz, o filter é utilizado para filtrar. veja abaixo um exemplo:

```javascript
// Some code

const alunos = ['ana', 'lucas', 'millena', 'julio'];
const medias = [6, 9, 8, 5];

// aqui estamos acessando o array alunos, que possui o aparmetro aluno
// e estamos acessando o array medias usando o parametro indice. se a média for menor
//que 7, retornará o nome do aluno
const reprovados = alunos.filter((aluno, indice) => {
    return medias[indice] < 7;
});

console.log(reprovados);

//Resultado: [ 'ana', 'julio' ]
```

\
