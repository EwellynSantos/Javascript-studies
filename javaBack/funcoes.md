# Funções

### Função

As funções são blocos de códigos que possuem alguma função, ele podem ter parametros e retorno.

```javascript
//parametros
//retorno

//segue um exemplo

function exemplo(parametro){
    return "retorno"
}


//segue outro exemplo

function exibeInfos(nome, nota){
    return `o nome é ${nome} e a nota é ${nota}` 
}

const resultado = exibeInfos('ana', 10);

console.log(resultado)
//retorna "o nome é ana e a nota é 10"


```

é importante se atentar a ordem que voce fornece os valores, pois podem alterar a ordem.&#x20;



### Expressão de função

quando fazemos a expressão de uma função, envolvemos ela numa const, ou seja, ao inver de o valor da const ser uma string, um int ou algo assim, na verdade ela é uma função.&#x20;

```javascript
// Some code

const estudanteReprovou = function (notaFinal, faltas){
    if (notaFinal < 7 && faltas > 4){
        return true;
    } else {
        return false;
    }
}

console.log(estudanteReprovou(6, 5));
console.log(estudanteReprovou(10, 2));

```



### Diferença entre função e expressão de função



Caso eu declare uma função e em algum momento eu mova o console.log  acima da função, ela continua funcionando, pois por "debaixo dos panos" ocorre o que chamados de hoisting.\
\
Quando o arquivo é lido pelo javascript, as funçoes declaradas e as variaveis criadas com var são "puxadas pra cima", elas são lidas primeiro, então quando fazemos as chamada acima da função, o javascript já sabe qual é a função.\


E quando declaramos uma expressão de função, não ocorre o hoisting com ela, então caso façamos uma chamada acima dela, retornará um erro, pois essa função não foi lida ainda.&#x20;

Exemplos:

<pre class="language-javascript"><code class="lang-javascript">//função

console.log(exemplo(parametro)) //chamada antes da função ser declarada

function exemplo(parametro){
    return `retorno ${parametro}`
}

<strong>//O retorno da certo
</strong>
//expressão de função

console.log(exemplo(parametro)) //chamada antes da expressão de função ser declarada

const exemplo = function (parametro){
    return `retorno ${parametro}`
}

<strong>//O retorno da erro
</strong>

</code></pre>

