# Manipulando Objetos

### Notação de Ponto

Usada para  <mark style="color:yellow;">**acessar propriedades de objetos**</mark>. Sintaxe:

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
//aqui estou acessando a propriedade nome do objeto objPessoa
console.log(`o nome do estudante é: ${objPessoa.nome}`);

//Resultado: o nome do estudante é: Jose Silva
```

### Método Substring

podemos utilizar o método substring para <mark style="color:yellow;">**pegar uma parte específica de uma string**</mark>, como parametro nó colocamos o inicio e o fim. Ressalto que quando colocamos um parametro de fim, ele não inclui aquele parametro. Ex (0, 4), o inicio é o zero, e o fim é o quatro, mas ele não está incluso no resultado. então será: 0, 1, 2, 3 o resultado.

Exemplo:

```javascript
const objPessoa = {
    nome: 'Jose Silva',
    idade: 32,
    cpf: '157811111111',
}
//aqui definimos que o parametro incia no indice 0 e termina no indice 3
console.log(`Os tres primeiros n° do cpf são: ${objPessoa.cpf.substring(0, 3)}`)

//Resultado: Os tres primeiros n° do cpf são: 157
```

no exemplo acima, o segundo parametro é tres, mas nao inclui o conteudo do indice dele, que seria 8.





### Notação de Colchetes

Através da notação de conchete podemos <mark style="color:yellow;">**acessar as propriedades**</mark> passando ela como um dado variavel. Segue abaixo 2 exemplos de como podemos utilizar essa notação:

Exemplo 1:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
};

//aqui usamos a notação de colchetes para passar a prorpiedade nome do objeto estudante
console.log(estudante['nome'])

//Resultado: Jose Silva
```



Exemplo 2:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
};

//aqui criamos uma função que recebe como parametro um objeto e uma propriedade
function exibeInfosEstudantes(objEstudante, infoEstudante) {
    return objEstudante[infoEstudante]
}

//aqui passamos os parametros estudante(obj) e nome(prop)
console.log(exibeInfosEstudantes(estudante, 'nome'))

//Resultado: Jose Silva
```

Nota-se que para os dois casos utilizamos os colchetes, um direto no console.log e outro na função. Importante lembrar que a propriedade sempre deve estar entre aspas, ou dará erro.&#x20;
