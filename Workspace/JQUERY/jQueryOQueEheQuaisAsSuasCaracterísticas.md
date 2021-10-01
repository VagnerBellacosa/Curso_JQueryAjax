# jQuery: O que é e quais as suas características

*Conheça mais sobre o jQuery, a biblioteca mais popular para JavaScript.*

O **JQUERY** é um biblioteca leve, rápida e cheia de recursos para Javascript.
Ele facilita a manipulação de eventos, animações, elementos HTML e utilização de Ajax. Basicamente, ele mudou e facilitou a escrita de códigos em Javascript. Foi lançado oficialmente em 2006 e possui código aberto. A biblioteca também oferece a possibilidade de criação de plugins sobre ela. Através do jQuery é possível desenvolver aplicações web de alta complexilidade.
Site oficial: [https://jquery.com](https://jquery.com/)
 

## ALGUMAS CARACTERÍSTICAS DO JQUERY

 **É bem leve**
A biblioteca compactada e minificada possui apenas 32kB.

 **Suporte a diversos navegadores web**
O JQuery funciona em todos os navegadores mais utilizados no mundo, entre eles: Google Chrome, Firefox, Edge, Safari, Internet Explorer, Android, iOS e outros mais.

 **Suporte a CSS3**
Por consequência da integração com HTML, também suporta seletores CSS3 para encontrar elementos, bem como na manipulação de propriedade de estilo.

 **Possui diversos plugins**
Conta com mais de 2600 plugins o repositório oficial que pode ser acessado através do seguinte link: [http://plugins.jquery.com](http://plugins.jquery.com/).

## COMPARANDO CÓDIGOS EM JAVASCRIPT E JQUERY

No primeiro exemplo, o resultado esperado é alterar a cor de background da tag body.
CÓDIGO JAVASCRIPT

```
Function changeBackground(color) {
        Document.body.style.background = color;
}
Onload=”changeBackground (‘blue’);”
```

CÓDIGO JQUERY

```
$ (‘body’) .css (‘background’, ‘#555ada’);
```

 

No segundo exemplo, deve ser atribuído o valor “14” a um elemento
CÓDIGO JAVASCRIPT

```
document.getElementById( 'Elemento' ).value = 14;
```

CÓDIGO JQUERY

```
$( '#Elemento' ).val( 14 );
```