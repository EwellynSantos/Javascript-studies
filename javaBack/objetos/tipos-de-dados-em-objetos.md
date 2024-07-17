# Tipos de dados em Objetos

### Array em Objetos

Há alguns tipos de dados que já conhecemos, como o Int, String, bool.. E em objetos também podemos ter arrays, podemos utilizar eles para aqueles casos em que <mark style="color:yellow;">**uma propriedade possui mais de um valor**</mark>.  Exemplo:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    telefones: ['11988888888', '119548884444'] 
    //aqui criamos a propriedade telefones que possui um array
    
};

console.log(estudante.telefones)

//resultado: [ '11988888888', '119548884444' ]

//para ver um valor em um indice específico: EX: console.log(estudante.telefones[0])
```



### Objetos em Objetos

Usamos os objetos para juntar dados que pertencem a um mesmo contexto, então no caso abaixo podemos utilizar <mark style="color:yellow;">**objetos dentro de objetos**</mark> facilmente. Veja abaixo como podemos fazer:

```javascript
//aqui temos um primeiro objeto estudante
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    telefones: ['11988888888', '119548884444']
};

//aqui estamos criando o endereço dentro do objeto estudante
estudante.endereco = {
    rua: 'Rua Carolina Ribeiro',
    numero: '33',
    complemento: 'ap 159'
}

console.log(estudante)

//Resultado:
{
  nome: 'Jose Silva',
  idade: 15,
  cpf: '157811111111',
  telefones: [ '11988888888', '119548884444' ],
  endereco: { rua: 'Rua Carolina Ribeiro', numero: '33', complemento: 'ap 159' }
}
```

Caso queira acessar uma informação dentro do objeto do objeto, é só usar as notações, como a notação de ponto neste caso:

```javascript
console.log(estudante.endereco.rua)

//Resultado: Rua Carolina Ribeiro

```
