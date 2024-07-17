# Funções em Objetos

Além de propriedade, objetos também pode ter funções. Veja como podemos fazer isso:

```javascript
const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    media: 7.5,
    //aqui estamos criando a function estaAprovado
    estaAprovado: function(mediaBase){
        return this.media >= mediaBase ? true : false 
    }   //utilizamos o this para referenciar alguma propriedade do objeto
};

console.log(estudante.estaAprovado(7))

```
