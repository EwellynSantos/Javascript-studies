# Manipulando Objetos part. 2



### Adicionando e alterando&#x20;

Podemos <mark style="color:yellow;">**adicionar propriedades e alterar valores**</mark> de maneira simples. Segue abaixo a sintaxe:

```javascript
//adicionando:
nomeObjeto.nomePropriedadeNova = 'valor da nova propriedade';

//alterando:
nomeObjeto.nomePropriedadeExistente = 'novo valor da propriedade'
```

Exemplo:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
};

//adicionando a propriedade telefone com o valor '9111111555'
estudante.telefone = '9111111555';
console.log(estudante);

//atribuindo o valor 'Julio Bernardo' a propriedade nome
estudante.nome = 'Julio Bernardo';
console.log(estudante)


//Resultados:
{
  nome: 'Jose Silva',
  idade: 15,
  cpf: '157811111111',
  telefone: '9111111555' //propriedade adicionada
}
{
  nome: 'Julio Bernardo', // valor alterado
  idade: 15,
  cpf: '157811111111',
  telefone: '9111111555'
}
```



### Deletar propriedades

para <mark style="color:yellow;">**deletar propriedades de um objeto**</mark> podemos utilizar o método delete, a sintaxe é bem simples:

```javascript
delete nomeObjeto.propriedade
```

Exemplo:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
};

//aqui estou deletando a proproedade cpf
delete estudante.cpf

console.log(estudante)

//Resultado: { nome: 'Jose Silva', idade: 15 }

```
