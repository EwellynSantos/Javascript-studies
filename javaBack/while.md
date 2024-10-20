# While

O while é uma estrutura de repetição simples que ocorre enquanto a condição for true. lmbrando qeu sempre precisamos adicionar algo que torne a condição false, ou teremos um loop infinito.

sintaxe:

```javascript
while(condição) {
    ação a ser executada

    ação para tornar a condição false
}

```

Exemplo:

```javascript
var x = 0;

while(x < 0) {
    console.log('o número é: ' + x);

    x++;
}
```
