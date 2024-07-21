# For...in

O for in é utilizado para percorrer objetos. Veja sua sintaxe:

```javascript
for(let nomeVariavel in nomeObjeto){
}
```

Segue abaixo um exemplo:



### Percorrendo Propriedades

do modo abaixo, estamos percorrendo as propriedades do objeto, sendo nome, idade, cpf...

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    media: 7.5,
    estaAprovado: function(mediaBase){
        return this.media >= mediaBase ? true : false
    },
    enderecos: [
        {
        rua: 'tua alguma coisa',
        numero: '123'
    },
        {
        rua: 'tua alguma coisa',
        numero: '123'
    }]   
};

//aqui criamos o laço de repetição
for(let chave in estudante) {
    console.log(chave) //aqui imprimimos o conteudo da chave
}

// Resultado:
nome
idade       
cpf
media       
estaAprovado
enderecos  
```



### Percorrendo valores

Neste caso, estamos percorrendo os valores das propriedades do objeto

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    media: 7.5,
    estaAprovado: function(mediaBase){
        return this.media >= mediaBase ? true : false
    },
    enderecos: [
        {
        rua: 'tua alguma coisa',
        numero: '123'
    },
        {
        rua: 'tua alguma coisa',
        numero: '123'
    }]   
};
//aqui criamos o laço que percorre os valores das propriedade
for(let chave in estudante) {
    console.log(estudante[chave])
}

//Resultados:
Jose Silva
15
157811111111
7.5
[Function: estaAprovado]
[
  { rua: 'tua alguma coisa', numero: '123' },
  { rua: 'tua alguma coisa', numero: '123' }
]
```
