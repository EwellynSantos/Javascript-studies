# Encontrando um Objeto(includes/find)

Quando recebemos um JSON com diversos conteudos, é comum que seja um array de objetos. Exemplo: um array de estudantes que possui os objetos estudante..  por ai vai.

No caso abaixo, recebemos então um arquivo json que possui diversos objetos em um array'. Por se tratar de um array, quando importarmos o arquivo poderemos utilizar métodos de arrays nele. Veja só:\


```javascript
const estudantes = require('./estudantes.json')//importando o arquivo json

//O paramtro lista receberá o array, o parametro chave recebera o nome da propriedade
//do objeto e o parametro valor receberá o conteudo que queremos encontrar.
function buscaInfo(lista, chave, valor){
    //aqui utilizamos o metodo de array includes
    //também podemos usar o método find, mas ele nao estrará nos arrays dos array
    //por isso utilizamos o include nesse caso
    return lista.find((estudante) => estudante[chave].includes(valor))
}

const estudanteEncontrado = buscaInfo(estudantes, 'nome', 'Juliet');

console.log(estudanteEncontrado);

//resultado:
{
  nome: 'Juliet',
  email: 'jelphey4@wikipedia.org',
  telefone: [ '1198123183', '11998123183' ],
  endereco: { logradouro: 'Rua Crownhardt', numero: '07', cep: '184366' }
}
```

