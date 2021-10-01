# O que é jQuery?

## É um framework JavaScript

Lançada em 2006, por [John Resig](https://twitter.com/jeresig), jQuery, segundo definição consta em seu site, trata-se de uma rápida, pequena e rica em *features* biblioteca JavaScript.

Como o lema *"Write less, do more."* (escreva menos, faça mais), jQuery revolucionou o desenvolvimento web, sendo presente em inúmeros projetos atualmente.

### Mas, por que é tão utilizado?

Exatamente pelo seu lema. Com jQuery é possível fazer diversos efeitos com poucas linhas e, que custariam dezenas de linhas em JavaScript puro.

Alguns recursos oferecidos facilmente pelo jQuery:

- Seleção e manipulação de elementos HTML
- Manipulação de CSS
- Efeitos e animações
- *Navegação* pelo DOM
- Ajax
- Eventos

### Como uso?

Igualmente qualquer arquivo JavaScript você precisa inseri-lo na página com as tags `script`. Você pode fazer o link para uma CDN como a do [Google](https://developers.google.com/speed/libraries/devguide?hl=pt-br#jquery) ou fazer o download do framework no seu projeto e linkar direto (vale lembrar que se optar por essa opção, faça o link para a versão **minificada**).

```html
<script src="js/jquery.min.js"></script>
```

### A sintaxe

A sintaxe básica é a seguinte:

```javascript
$('seletorHTML').acao();
```

### Alguns exemplos práticos

#### Manipulação HTML

```javascript
$( "#botao" ).html( "Sucesso!" )
```

No exemplo acima, selecionamos o elemento com *ID* botão e inserimos a *string* "Sucesso!".

#### Eventos

```javascript
var box = $( "#box" );
$( "#botao" ).on( "click", function( event ) {
  box.show();
});
```

No *snippet* acima, guardarmos em uma [variável](https://tableless.github.io/iniciantes/manual/js/variaveis.html) o elemento com *ID* box. Em seguida, adicionao ao elemento com *ID* 'botao' o evento do *clique*. Ao ser disparado, esse evento mostra o elemento, que guardarmos na variável box anteriormente, através do método `show()`.