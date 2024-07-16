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
