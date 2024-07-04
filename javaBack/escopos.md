# Escopos

### Global

Qualquer variável que esteja no escopo global pode ser acessada por outras partes do programa. Uma variável é considerada global quando não é declarada dentro de nenhuma função ou bloco.

```javascript
// Some code
const nome = ‘Camila’; // variável global

function cumprimentar() {
  console.log(`Olá, ${nome}!`); // Acessa a var global
}

cumprimentar(); // ‘Olá, Camila!”

```

### Bloco

Variáveis declaradas dentro de chaves `{ }`, como no caso de `if`, `for`, `while` etc., não ficam acessíveis para código que esteja de fora. Chamamos o código dentro das `{ }` de **bloco**.

```javascript
// Some code

if (1 > 0) {
  let nome = ‘Ana’;
  console.log(nome); // ‘Ana’
}

// variável `nome` não está acessível
console.log(nome); // Error: nome is not defined

```

obs: as variaveis declarada com var nao seguem essa regra de escopo.



### Função

Variáveis declaradas dentro de uma função são consideradas “locais” (ou seja, o oposto de “globais”) e não podem ser acessadas por código que esteja fora do bloco da função.

```javascript
// Some code
function cumprimentar() {
  const nome = 'Camila'; // variável local
  const cumprimento = 'Olá'; // variável local
  console.log(`${cumprimento}, ${nome}!`); // “Olá, Camila!”
}

// as variáveis não podem ser acessada de fora da função
console.log(`${cumprimento}, ${nome}!`); // Dará erro de “not defined” no console

```
