# Operadores de Comparação



### ==

quando utilizamos 2 == estamos comparando valores/conteudos, conforme abaixo:

<pre class="language-javascript"><code class="lang-javascript">// Some code

if ('0' == 0) {
    console.log("aprovado")
} else {
    console.log("reprovado")
}

<strong>//resultado é "aprovado"
</strong>
</code></pre>

ou seja, apesar de o primeiro ser uma string, o valor dele é um zero, e o segundo também é um zer, então retorna "aprovado"



### ===

quando utilizamos 3 === estamos comparando não apenas o conteudo/valor como também o tipo, conforme abaixo:

<pre class="language-javascript"><code class="lang-javascript">// Some code


if ('0' === 0) {
    console.log("aprovado")
} else {
    console.log("reprovado")
}

<strong>//resultado é "reprovado"
</strong>
</code></pre>

ou seja, apesar de os valores serem 0, eles possuem tipos diferentes, sendo uma string e um int.

O ideal é utilizar os 3 ===, pois assimgarante que realmente estamos comparando os dados de maneira correta.&#x20;
