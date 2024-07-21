# Operador de espalahamento Spred

O operador de espalhamento é util para quando precisamos montar objetos que possuem partes de outros objetos. Além disso, ele deixa de maneira mais automática a visualização de alguns dados. Vejamos os exemplos:



#### <mark style="color:yellow;">Visualizando o conteudo</mark>

Aqui mostramos uma maneira diferente de visualizar o conteudo do objeto:

<pre class="language-javascript"><code class="lang-javascript">const estudante = {
    nome: 'Jose Silva',
    idade: 15,
    cpf: '157811111111',
    media: 7.5,
    telefones: ['11999999999', '119888555455'],
    estaAprovado: function(mediaBase){
        return this.media >= mediaBase ? true : false
    },
    enderecos: [
        {
        rua: 'rua alguma coisa',
        numero: '123'
    },
        {
        rua: 'rua alguma coisa',
        numero: '123'
    }]   
};

//aqui criamos uma função para visualizar os telefones
function exibeTelefones(tel1, tel2){
    console.log(`ligar para ${tel1}`)
    console.log(`ligar para ${tel2}`)
}
//dessa maneira deixamos muito manual, pois estamos colocando exatamente os indices 
//e o ideal é que nao precisemos fazer isso
exibeTelefones(estudante.telefones[0], estudante.telefones[1])

//neste caso, usamos o spred para espalhar o conteudo da chave, e assim, obtemos os
//primeiros valores que utilizados nos parametros da função
<strong>exibeTelefones(...estudante.telefones)
</strong>
Resultados:
ligar para 11999999999//resultado do primeiro console
ligar para 119888555455

ligar para 11999999999//resultado do segundo console
ligar para 119888555455
</code></pre>

De cara, é o mesmo resultado, mas a maneira como deixamos de modo mais automático no código faz uma diferença.&#x20;

#### <mark style="color:yellow;">Usando o espalhamento</mark>

aqui utilizamos o mesmo código acima, mas dessa vez estamos realizando o espalhamento de dados, neste caso nao estamos juntando objetos diferentes, mas há a possibilidade:

<mark style="color:red;">**Uma maneira menos prática seria:**</mark>

```javascript
const dadosEnvio = {
    destinatario: estudante.nome,
    endereco: estudante.enderecos
}

Resultado:

{
  destinatario: 'Jose Silva',
  endereco: { rua: 'rua alguma coisa', numero: '123' }
}
```

Mas dessa maneira estamos visualizando a propriedade nome  e o array endereço, e nao é bem isso que queremos, nós queremos visualizar as propriedades apenas.\
\
<mark style="color:green;">**Veja como pode ser feito:**</mark>&#x20;

```javascript
const dadosEnvio = {
    destinatario: estudante.nome,
    ...estudante.enderecos[0] //aqui espalhamos o conteudo/valor da propriedade e 
    //e definimos que o valores que queremos visualizar iniciam do 0
}

console.log(dadosEnvio)

Resultado:

{ destinatario: 'Jose Silva', rua: 'rua alguma coisa', numero: '123' }
```

Aqui temos um resultado só, os valores são as propriedades do objeto apenas.
