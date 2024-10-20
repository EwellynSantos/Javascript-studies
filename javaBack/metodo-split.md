# Método split

O método split é utilizado paar separar conteudo de acordo com o marcado.

exemplo:

```javascript
const texto = "Exemplo   de\nconteúdo para  separar";
const palavras = texto.split(/\s+/); // Qualquer quantidade de espaço em branco
console.log(palavras); //neste caso resultaá em um array

//["Exemplo", "de", "conteúdo", "para", "separar"]
```

Aqui, `\s+` é uma expressão regular que corresponde a qualquer quantidade de espaços em branco, como espaços, quebras de linha ou tabulações.



mas também podemos querer atribuir os valores em const separadas:

```javascript
//aqui receberemos uma entrada no terminal: 3.0 4.5 5.2
const entrada = readlineSync.question('');

const [A, B, C ] = entrada.split(" ").map(Number);
//aqui criamos um array e usamos o split para separar o conteudo e entao mapeamos
//e trasnformamos em number
```
