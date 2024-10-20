# Switch ...case

O switch é utilizado quando precisamos fazer muitas comparações, ele recebe uma variavel e compara os cases com a variavel recebida, caso ele encontre um case true, entao executa o código abaixo do case. Impotante lembrar de colocar o break, se nao ele continuará as comparações de cases. Após os cases, devemos também adicionar um compotamento default, para caso a variavel nao se encaixe em nenhum case. Sintaxe:

```javascript
switch (variavel) {
    case 'caso a ser comparado' :
    codigo a ser executado se true;
    break;
    
    default:
    código a ser executado
}
```

exemplo:

```javascript
let permissao; //comum, gerente ou diretor

switch(permissao) {
    case 'comum':
        console.log('usuário comum');
        break;
    case 'gerente':
        console.log('usuário gerente');
        break;
    case 'diretor':
        console.log('usiário diretor');
        break;
    default:
        console.log('usuário desconhecido')  
}

```
