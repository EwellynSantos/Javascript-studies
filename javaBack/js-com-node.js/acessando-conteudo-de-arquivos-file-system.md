# Acessando conteudo de arquivos(File System)

Para que possamos <mark style="color:yellow;">acessar o conteudo de um arquivo</mark>, utilizaremos o fs que é uma biblioteca do js, que permite diversos tipos de interação de uma aplicação com o sistema de arquivos do computador,  e ele é uma biblioteca que precisa de callback, ou seja uma função.

Sintaxe:

```javascript
fs.metodoModulo(variavelLink, 'utf-8'(tipo de conteudo), (variavelError, variavelConteudo) => {
    conteudoFunção;
});

```

Veja só:

```javascript
const fs = require('fs')// aqui impotamos o File System e atribuimos a var fs

const caminhoArquivo = process.argv;//utilizamos para pegar o caminho do arquivo
const link = caminhoArquivo[2];//atribuimos o caminho digitado no indice 2 a var link

//usamos o método readFile para ler o conteudo do arquivo
//parametro 1 é a variavel contendo o link
//parametro 2 é o tipo do arquivo, utf-8 é para que leia o conteudo em string 
//parametro 2 a var erro, para receber erro e a var texto é a que receberá o conteudo
fs.readFile(link, 'utf-8', (erro, texto) => {
    console.log(texto);//aqui imprimimos o conteudo do aquivo
});
```

Resultado:

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>



### Caminho absoluto

Chamamos de caminho absoluto quando a localização de um arquivo ou pasta é especificado a partir do diretório-raiz do sistema operacional. Por exemplo:

```bash
#caminho para um diretório (a última `/` é opcional)
/home/juliana/Documents/alura/projeto-js

#caminho para um arquivo dentro do diretório
/home/juliana/Documents/alura/projeto-js/index.js
```

### Caminho relativo

Um caminho relativo para um diretório ou arquivo é definido a partir de sua relação com o `pwd`, ou seja, o **present working directory** (diretório de trabalho atual). Na linha de comando, `pwd` também é o comando **print working directory** (imprimir o diretório de trabalho), que usamos justamente para saber onde na estrutura do sistema operacional se encontra o diretório em que estamos.

Veja no exemplo abaixo uma representação em árvore de um diretório, como o do curso em que estamos trabalhando (o diretório `node_modules` foi excluído para facilitar a leitura, pois é muito extenso):

```bash
/home/juliana/Documents/nodejs-lib
.
├── arquivos
│   ├── texto-aprendizado.txt
│   ├── texto-kanban.txt
│   └── texto-web.txt
├── lib
│   ├── index.js
```

Na representação acima, consideramos como `pwd` o diretório `nodejs-lib`. Então, o caminho relativo do arquivo `texto-web.txt`, por exemplo, seria `./arquivos/texto-web.txt`, e o caminho absoluto seria `/home/juliana/Documents/texto-web.txt`.
