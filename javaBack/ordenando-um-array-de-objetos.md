# Ordenando um array de objetos

Para ordenar objetos utilizaremos o método sort. Detalhe, ele ordena os objetos mas nao ordena as propriedade, ou seja, se eu quiser ordenar apenas a propriedade nome e visualizar ela, nao será possivel, pois podemos ordenar os objetos inteiros, então se eu passar como parametro uma propriedade, ele ordenara os objetos com base no parametro fornecido. Veja só:

```javascript
const estudantes = require('./estudantes.json')//importamos um array de objetos

function ordena(lista, propriedade) {
    //aqui chamamos o método callback sort
    return lista.sort((a, b) => {//por padrão definomos os nomes das variaveis de a e b
        //se o a for menor b, o a fica uma posição a menos do b
        if (a[propriedade] < b[propriedade]) return -1;
        //se a for maior que b, o a fica uma posição a mais do b
        if (a[propriedade] > b[propriedade]) return 1;
        //se nao, retornar 0, ou seja, nao muda de lugar
        return 0;
    })
}

//aqui paramos como parametro o array estudantes.json e a propriedade nome
const listaOrdenada = ordena(estudantes, 'nome');
console.log(listaOrdenada)

Resultado:
[
  {
    nome: 'Amye',
    email: 'aranahan2@yellowbook.com',
    telefone: [ '1918820860', '19918820860' ],
    endereco: {
      logradouro: 'Rua Karstens',
      numero: '59',
      cep: '627533',
      complemento: 'ap 401'
    }
  },
  {
    nome: 'Blakeley',
    email: 'bmccaughran5@blog.com',
    telefone: [ '7919437785', '79919437785' ],
    endereco: { logradouro: 'Rua Stone Corner', numero: '40429', cep: '1000' }
  },
  {
    nome: 'Carolina',
    email: 'ckauschea@reddit.com',
    telefone: [ '1877479960', '18977479960' ],
    endereco: {
      logradouro: 'Rua Mosinee',
      numero: '28672',
      cep: '8314',
      complemento: 'Bar dos coroas'
    }
  },
  {
    nome: 'Cecelia',
    email: 'cmacgrayg@unc.edu',
    telefone: [ '3569848931', '35969848931' ],
    endereco: { logradouro: 'Rua Karstens', numero: '115', complemento: 'ap 71' }
  },
  {
    nome: 'Dorothea',
    email: 'dmutimere@bizjournals.com',
    telefone: [ '6804913737', '68904913737' ],
    endereco: { logradouro: 'Rua Morrow', numero: '1' }
  },
  {
    nome: 'Emilee',
    email: 'eempsonc@bloomberg.com',
    telefone: [ '4775323087', '47975323087' ],
    endereco: { logradouro: 'Rua West', numero: '8' }
  }
]
```

<mark style="color:blue;">**O que houve?**</mark>

Com base nos parâmetros fornecidos, o método sort  ordenou os objetos de acordo com a propriedade nome. Veja que eles estão em ordem alfabética.
