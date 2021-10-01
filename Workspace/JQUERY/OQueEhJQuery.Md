# JQuery

## O Que é jQuery e Para Que Serve?

jQuery é uma biblioteca popular do JavaScript. Ela foi criado por John Resig em 2006 com o propósito de facilitar a vida dos desenvolvedores que usam JavaScript nos seus sites. Não é uma linguagem de programação separada, funciona em conjunto com o JavaScript. Com jQuery, você vai conseguir fazer muito mais com menos – eu vou explicar logo mais.

Criar códigos pode ser um pouco cansativo, especialmente quando isso envolve muitas strings. A jQuery compacta várias linhas de código em uma única função. Assim, você não precisa reescrever todos os blocos repetidamente para concluir sua tarefa.

###Conteúdo

[Exemplos de jQuery]]
[Recursos Importantes do jQuery]
[Vantagens jQuery]
[Exemplos de jQuery]

Você pode criar efeitos de slide com apenas algumas linha de código.

Você pode usar os comandos SlideDown(), SlideUp() e SlideToogle().

~~~javascript
$("#flip").click(function(){
 $("#panel").slideDown();
});
~~~

Com jQuery, você também pode esconder os elementos em HTML com os comandos Hide() e Show(). Veja:

~~~javascript
$("#hide").click(function(){
 $("p").hide();
});
$("#show").click(function(){
 $("p").show();
});
~~~javascript

E aqui está um exemplo de animação:

~~~javascript
$("button").click(function(){
 $("div").animate({
     left: '250px',
     height: '+=150px',
     width: '+=150px'
 });
});
~~~javascript

E aqui você vê o fragmento de um código para entender como manipular o CSS.

~~~javascript
$("button").click(function(){
 $("h1, h2, p").toggleClass("blue");
});
~~~javascript

## Recursos Importantes do jQuery

Uma característica do motivo pelo qual o jQuery se tornou tão famoso e popular é, provavelmente, os recursos de plataforma cruzada. Os erros são corrigidos automaticamente e a execução acontece da mesma maneira nos navegadores mais usados, como Chrome, Firefox, Safari, MS Edge, IE, Android e iOS.

jQuery também torna o Ajax muito mais simples. Ajax funciona de forma assíncrona com o código, que significa que o código escrito com o Ajax pode se comunicar com o servidor e atualizar seu conteúdo sem precisar recarregar a página.

Mas isso vem com alguns problemas. Diferentes navegadores executam a API do Ajax de maneira diferente. Assim, o código deve aderir a todos os navegadores. Se for feito manualmente, esse é um trabalho difícil e demorado. Felizmente, o jQuery faz todo o trabalho manual e adapta o código a todos os navegadores da web.

Depois, há a manipulação do DOM (Document Object Model) com vários meios sobre como fazer isso. Mas, para simplificar, ele permite que você insira e/ou remova elementos DOM em uma página HTML, bem como linhas mais simples.

Criar animações também é simples com o jQuery. Como no exemplo de código acima, você consegue executar tudo com algumas linhas de código, tudo o que você precisa é inserir as variáveis.

A transferência de documentos HTML, bem como a manipulação de efeitos e eventos, também são melhores com o jQuery.

Você precisa conhecer melhor a Hostinger! Nós temos o plano ideal para cada projeto e mais de 800 extensões de domínio. É só escolher!

## Vantagens jQuery

Os benefícios de usar o jQuery são substanciais. O slogan “Escreva menos, faça mais” tem tudo a ver com a jQuery. Quando você aprender a como usar jQuery (que é muito fácil), você será capaz de executar todas os tipos de ações com facilidade.

Considerando que é a biblioteca JavaScript mais popular disponível, existem muitos materiais que ensinam como aprender jQuery. Mas, para isso, é preciso um conhecimento básico de JavaScript, HTML e CSS.

Se você está usando JavaScript, é quase obrigatório usar a jQuery por tantos benefícios que isso traz, já que o único desafio será aprender como usar e então aplicar no seu trabalho!

[Artigo original](https://www.hostinger.com.br/tutoriais/o-que-e-jquery)