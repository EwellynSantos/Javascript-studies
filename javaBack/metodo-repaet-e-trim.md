# Método repaet e trim



### Repeat

o método repeat é utilizado para repetir caracteres no console, veja a sintaxe:

```javascript
'elemento'.repeat(quantidade)
```

<mark style="color:blue;">veja um exemplo:</mark>

```javascript
function staircase(n) {
let arvore = '';
    for(let i = 0; i < n; i++){
        let tamanhoEspaco = n - i - 1;
        arvore += ' '.repeat(tamanhoEspaco) + '#'.repeat(i + 1) + '\n';    
    }
    console.log(arvore)
    return arvore.trim();
}

resultado: suponto que o n seja 6

     #
    ##
   ###
  ####
 #####
######
```

no caso estou repetindo o " "(espaço) e o # de acordo quan a quantidade definida.





### Trim

O método `trim()` é usado para **remover espaços em branco** (e quebras de linha) do início e do final de uma string.&#x20;

<mark style="color:blue;">Exemplo:</mark>

como é visto no código acima, tinhamos uma quebra de linha definida dentro do for, ou seja, no fim da execução do código, o resultado teria uma quebra de linha que nao queriamos.
