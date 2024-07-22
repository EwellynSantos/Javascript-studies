# Filtrando objetos(filter)

Podemos utilizar também o método callback filter para buscar dados dentro de um array de objetos. veja só:\


```javascript
const estudantes = require('./estudantes.json')

function filtraPorPropriedade(lista, propriedade) 
    return lista.filter((estudante) => {
        //definimos aqui que buscaremos aqueles objetos que nao tem a propriedade cep
        return !estudante.endereco.hasOwnProperty(propriedade);
    })
}
const listaEnderecosIncompletos = filtraPorPropriedade(estudantes, 'cep');
console.log(listaEnderecosIncompletos)

Resultado:
[
  {
    nome: 'Greer',
    email: 'gtumielli3@vimeo.com',
    telefone: [ '9466883489', '94966883489' ],
    endereco: { logradouro: 'Rua Algoma', numero: '077' }
  },
  {
    nome: 'Leeann',
    email: 'lhuckleby6@tuttocitta.it',
    telefone: [ '9045673092', '90945673092' ],
    endereco: { logradouro: 'Rua Center', numero: '549' }
  },
  {
    nome: 'Tildi',
    email: 'tmilthorpe7@answers.com',
    telefone: [ '3149463623', '31949463623' ],
    endereco: { logradouro: 'Rua Clyde Gallagher', numero: '3962' }
  },
  {
    nome: 'Stephine',
    email: 'smullard9@etsy.com',
    telefone: [ '5327428873', '53927428873' ],
    endereco: {
      logradouro: 'Rua Ruskin',
      numero: '36819',
      complemento: 'Bloco 16 ap 202'
    }
  },
  {
    nome: 'Jerrome',
    email: 'jbletsorb@dmoz.org',
    telefone: [ '2492442110', '24992442110' ],
    endereco: {
      logradouro: 'Rua Arkansas',
      numero: '3983',
      complemento: 'Mercadinho'
    }
  },
  {
    nome: 'Emilee',
    email: 'eempsonc@bloomberg.com',
    telefone: [ '4775323087', '47975323087' ],
    endereco: { logradouro: 'Rua West', numero: '8' }
  },
  {
    nome: 'Dorothea',
    email: 'dmutimere@bizjournals.com',
    telefone: [ '6804913737', '68904913737' ],
    endereco: { logradouro: 'Rua Morrow', numero: '1' }
  },
  {
    nome: 'Flori',
    email: 'fbattersbyf@freewebs.com',
    telefone: [ '2047970414', '20947970414' ],
    endereco: {
      logradouro: 'Rua Forest',
      numero: '43',
      complemento: 'Na frente da quadra de basquete'
    }
  },
  {
    nome: 'Cecelia',
    email: 'cmacgrayg@unc.edu',
    telefone: [ '3569848931', '35969848931' ],
    endereco: { logradouro: 'Rua Karstens', numero: '115', complemento: 'ap 71' }
  },
  {
    nome: 'Izaak',
    email: 'ikarbyj@home.pl',
    telefone: [ '5193301028', '51993301028' ],
    endereco: { logradouro: 'Rua Grim', numero: '480' }
  }
]
```

#### <mark style="color:blue;">O que houve?</mark>

Veja que usamos o filter para filtrar as propriedade do array, e em sua execução iniciamos com o !, ou seja, buscamos por estudantes que nao tem endereço com cep. A interrogação representa o negativo.&#x20;



