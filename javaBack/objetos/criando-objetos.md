# Criando Objetos

Objetos sao utilizados para armazenar grupos mais complexos de informações, ele reflete as coisas da vida real. Ele sempre é composto por conjuntos de chave e valor . Exemplo de como criar um objeto:

```javascript
const objPessoa = {
    nome: 'Jose Silva',
    idade: 32,
    cpf: '111111111111',
    turma: 'java'
}
```

Para acessar uma propriedade do objeto devemos usar a **Notação de Ponto**

```javascript
nomeObj.propriedade
```

Exemplo:

```javascript
const objPessoa = {
    nome: 'Jose Silva',
    idade: 32,
    cpf: '111111111111',
}
//aqui estou acessando a propriedade nome do onjeto objPessoa
console.log(`o nome do estudante é: ${objPessoa.nome}`);

//Resultado: o nome do estudante é: Jose Silva
```

