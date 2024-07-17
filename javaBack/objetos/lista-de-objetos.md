# Lista de Objetos

Podemos utilizar a lista de objetos quando pracisamos <mark style="color:yellow;">**centralizar em um lugar objetos do mesmo tipo**</mark>. Lembrando que quando transformamos os dados do objeto em um array, podemos utilizar os métodos de array nos dados. Segue o exemplo abaixo:

Neste caso temos um objeto dentro de um objeto.

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    telefones: ['11988888888', '119548884444'],
    //aqui temos um novo objeto, e os dados dele estão envoltos por chaves[]
    //neste caso o conteudo do objeto esderecos é um array
    enderecos : [{
        rua: 'Rua Carolina Ribeiro',
        numero: '33',
        complemento: 'ap 159'
    }]
};

//aqui estamos adicionando um novo dado de array ao objeto enderecos
estudante.enderecos.push({ //o push é um método só para arrays
    rua: 'Rua Ribeiro Carolina ',
    numero: '66',
    complemento: ''
})
console.log(estudante.endereco)
console.log(estudante.endereco[0])//aqui estamos acessando o dado com indice 0 no obj

//Resultados:

[
  { rua: 'Rua Carolina Ribeiro', numero: '33', complemento: 'ap 159' },
  { rua: 'Rua Ribeiro Carolina ', numero: '66', complemento: '' }
]
{ rua: 'Rua Carolina Ribeiro', numero: '33', complemento: 'ap 159' }
```

usamos esse método, pois um estudante pode ter mais de um endereço, e endereços possuem diversos dados.
