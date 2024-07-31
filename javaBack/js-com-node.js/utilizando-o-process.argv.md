# Utilizando o process.argv

Neste caso, utilizaremos esse módulo para que possamos  atribuir a a uma variavel o caminho do arquivo que desejamos acessar. Inicialmente poderíamos utilizar o require para importar modulos, no entanto nem todos os módulos/arquivos estarão de acordo com os requisitos dele.

No caso do process.argv, podemos atribuir o caminho do arquivo direto no console, quando formos rodar o projeto, assim a variavel pode ser alterada, sem manter um valor padrão.  a sintaxe é:

```javascript
node caminhoArquivoAtual caminhoArquivoAcessar

node: é o comando para iniciar o node
caminhoArquivoAtual: é o arquivo com a qual trabalhamos no momento, 
que é o arquivo que estamos estamos escrevendo nosso código.
caminhoArquivoAcessar: é o caminho do arquivo que deseja acessar 
```

\
Veja só:

```javascript
const caminhoArquivo = process.argv; //aqui atribuimos o método a uma variavel
const link = caminhoArquivo[2]; //aqui atribuimos a variavel link o método que 
//utilizará o 2 indice como parametro

console.log(link)//só para vermos o resultado: arquivos/texto-web.txt
```

no console ficou:

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

#### <mark style="color:blue;">O que houve?</mark>

como adicionamos o parametro de indice 2, entao o console só exibiu o conteudo do indice 2.
