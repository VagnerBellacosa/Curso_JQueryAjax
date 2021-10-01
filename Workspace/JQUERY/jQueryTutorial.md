
Artigo[Invista em você! Saiba como a DevMedia pode ajudar sua carreira.](https://www.devmedia.com.br/jquery-tutorial/27299#modulo-mvp)

# jQuery Tutorial

## Veja neste artigo uma breve introdução à biblioteca JavaScript jQuery, aprendendo como realizar o download e utilizar seletores CSS.

[Artigos](https://www.devmedia.com.br/artigos/)[HTML e CSS](https://www.devmedia.com.br/artigos/front-end-web)jQuery Tutorial

##### Guia do artigo: jQuery Tutorial

- [Introdução ao jQuery](https://www.devmedia.com.br/jquery-tutorial/27299#Introducao)
- [O que é a jQuery?](https://www.devmedia.com.br/jquery-tutorial/27299#jQuery)
- [Utilidade do jQuery](https://www.devmedia.com.br/jquery-tutorial/27299#Utilidade)
- [Suporte ao jQuery](https://www.devmedia.com.br/jquery-tutorial/27299#Suporte)
- [Instalação do jQuery](https://www.devmedia.com.br/jquery-tutorial/27299#Instalacao)
- [Incluindo arquivo jQuery no HTML](https://www.devmedia.com.br/jquery-tutorial/27299#Incluindo)
- [Construtor jQuery](https://www.devmedia.com.br/jquery-tutorial/27299#Construtor)
- [Função $(document).ready()](https://www.devmedia.com.br/jquery-tutorial/27299#Funcao)

------

### Introdução ao jQuery

Nesse artigo vamos falar sobre jQuery, uma **[biblioteca JavaScript](http://www.devmedia.com.br/javascript-tutorial/37257)** desenvolvida por [John Resig](https://en.wikipedia.org/wiki/John_Resig), e que se tornou uma das bibliotecas JavaScript mais populares na internet, de código aberto e disponibilizada sobre as licenças MIT e GPL. Desse modo, é uma biblioteca que podemos utilizar para fins comerciais e pessoais, sem termos que pagar qualquer tipo de licença de uso.

Sua criação teve como foco a simplicidade e o objetivo de facilitar nossa vida no desenvolvimento de aplicações que necessitariam de linhas e mais linhas de código para obtermis um determinado efeito, ou efetuar uma [requisição Ajax](https://www.devmedia.com.br/ajax-com-jquery-trabalhando-com-requisicoes-assincronas/37141). Com **jQuery** esse trabalho é substituído por poucas instruções, o que faz da **jQuery** uma ferramenta ideal para aqueles designers e desenvolvedores com pouco conhecimento em **JavaScript**.

### O que é a jQuery?

jQuery é uma biblioteca de funções em [JavaScript](https://www.devmedia.com.br/guia/javascript/34372) que interage com o [HTML](https://www.devmedia.com.br/guia/html/38051), desenvolvida para simplificar os scripts interpretados no navegador do usuário (client-side). Criada em dezembro de 2006 no BarCamp de Nova York por [John Resig](https://johnresig.com/about/). Usada por cerca de 77% dos 10 mil sites mais visitados do mundo, jQuery é a mais popular das bibliotecas JavaScript.

**jQuery é uma biblioteca de código aberto (open source)** e possui licença dual, fazendo uso da [Licença MIT](https://pt.wikipedia.org/wiki/Licença_MIT) ou da [GNU General Public License](https://pt.wikipedia.org/wiki/GNU_General_Public_License) versão 2. A sintaxe do jQuery foi desenvolvida para simplificar a navegação em documentos HTML, a seleção de elementos DOM, criar animações, manipular eventos, desenvolver aplicações [AJAX](http://www.devmedia.com.br/introducao-ao-ajax-revista-easy-java-magazine-19/24797) e criação de plugins sobre ela. Permitindo aos desenvolvedores criarem camadas de abstração para interações de baixo nível de modo simplificado em aplicações web de grande complexidade.

<iframe src="https://www.youtube.com/embed/FKnkPtEvfws?rel=0" frameborder="0" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Saiba mais: [Curso de jQuery](http://www.devmedia.com.br/curso/o-que-e-jquery/1973)

A jQuery é leve, seu tamanho é em torno de 30kb, extensível, oferece suporte a plug-ins e conta ainda com uma grande equipe de desenvolvedores que vem diariamente adicionando novos recursos e funções a está biblioteca, nos disponibilizando uma grande quantidade de controles para interface.

### Utilidade do jQuery

Podemos utilizar a jQuery para:

- Adicionarmos efeitos visuais e animações;
- Acessarmos e manipularmos o DOM;
- Carregarmos componentes Ajax;
- Provermos interatividade;
- Fazer alteração de conteúdo;
- Simplificarmos tarefas JavaScript.

### Suporte ao jQuery

A jQuery foi desenvolvida para ser uma biblioteca com suporte a qualquer navegador Web. Ela facilita a nós desenvolvedores a muitas vezes difícil tarefa de desenvolvermos aplicações em JavaScript, tendo que atingir a enorme quantidade de navegadores em que nossa programação poderá ser executada. Como sabemos, cada navegador possui seu próprio conjunto de características de implementação que ainda pode dificultar mais ainda, de acordo com a variação de plataforma e sistema operacional onde esteja executando. Já com a **jQuery**, nossa programação é única e transparente.

Com a **jQuery** possuímos suporte também às CSS3, onde podemos [utilizar seletores CSS3](https://www.devmedia.com.br/css3-selectors-conhecendo-os-seletores-das-css3/24782) mesmo que o navegador não tenha suporte a esta folhas de estilo. Isso é possível porque a própria **jQuery** implementa os seletores CSS3, o que faz com que ela seja independente do navegador em que estiver sendo executada.

### Instalação do jQuery

Podemos estar obtendo a jQuery gratuitamente no [site](https://jquery.com/).

![Download da jQuery](https://arquivo.devmedia.com.br/artigos/Ricardo_Teixeira/Introducao_jQuery/Introducao_jQuery1.jpg)
**Figura 1:** Download da jQuery

Nessa página inicial clique no botão “download jQuery” localizado no canto direito em laranja, como podemos ver na figura 1, e a seguinte página será aberta.

![Escolha da versão para download da jQuery](https://arquivo.devmedia.com.br/artigos/Ricardo_Teixeira/Introducao_jQuery/Introducao_jQuery2.jpg)**Figura 2:** Escolha da versão para download da jQuery

Agora na página de download ficamos com duas opções para que você escolha a que vai melhor se adequar ao seu projeto. Porém, antes de efetuarmos o download de uma das duas, vamos conhecer a diferença entre elas.

**Production:** Esta versão serve para ambientes de produção, é uma versão com o código em formato compactado, sem quebra de linhas e com o código sem comentários, possuindo apenas 15% do tamanho da que veremos a seguir.

![Versão production jQuery 1.9.1](https://arquivo.devmedia.com.br/artigos/Ricardo_Teixeira/Introducao_jQuery/Introducao_jQuery3.jpg)**Figura 3:** Versão production jQuery 1.9.1

**Development:** Esta versão é para desenvolvimento, é a versão não compactada da biblioteca e possui o código todo comentado. Sendo ideal para ambientes de desenvolvimento, por se integrar facilmente com as ferramentas e IDEs.

![Versão development jQuery 1.9.1](https://arquivo.devmedia.com.br/artigos/Ricardo_Teixeira/Introducao_jQuery/Introducao_jQuery4.jpg)**Figura 4:** Versão development jQuery 1.9.1

Agora que já conhecemos ambas as versões disponíveis, basta escolher a versão que desejamos usar e clicar nos links mostrados na figura 3 e na figura 4, de acordo com a versão escolhida para o download. A biblioteca vai abrir em formato de código **JavaScript** no próprio navegador. Para salvá-la, podemos ir no meu arquivo < Salvar e salvarmos na pasta de desenvolvimento ou onde preferir. Nomes recomendados para cada versão.

- Versão production: jquery.min.js;
- Versão Development: jquery.js.

Uma dica para a melhor organização do nosso projeto é criarmos uma pasta js dentro da pasta principal do projeto e salvar a **jQuery** dentro dessa pasta.

### Incluindo arquivo jQuery no HTML

Agora que já fizemos o download e salvamos a jQuery dentro da pasta do nosso projeto, vamos referenciar a mesma utilizando o parâmetro SRC da tag SCRIPT dentro da tag HEAD.

**Listagem 1:** Fazendo referencia arquivo jQuery.

```
<html>
<head>
<title>...</title>
<!-- Versão development jQuery -->
<script type="text/javascript" src="jquery.js"></script>
</head>
```

### Construtor jQuery

Com a **jQuery** temos que utilizar a função $() para encontrarmos um elemento HTML dentro da aplicação e utilizarmos as funções da biblioteca. Essa função [e tecnicamente conhecida como construtor ou função construtora e ela estará presente em todas as aplicações que **utilizarmos a jQuery**.

É denominada desse modo para ser fácil de decorar, e o fato de se chamar $ evita a possibilidade de ocorrer conflitos com outras funções da biblioteca do usuário. Ocasionalmente podemos vir a utilizar alguma outra biblioteca que também tenha como uso uma função chamada $. Caso isso acontece podemos usar como alternativa a função jQuery().

O construtor faz uso do seguinte parâmetro, onde alvo é um seletor CSS para TAG, ID ou classe.

- $ (alvo)

Vejamos alguns exemplo de sua utilização.

- $(‘h1’)
- $(‘p’)
- $(‘#conteudo’)
- $(‘.teste’)

Como podemos ver, no exemplo acima estamos fazendo com que a **jQuery** encontre os elementos, H1, P, e os elementos com id="conteúdo" e a class="teste". O requisito mínimo para a utilização da jQuery é saber utilizar os seletores CSS.

### Função $(document).ready()

Essa função é uma das primeiras coisas que devemos aprender na **jQuery**. De forma simples podemos dizer que essa função é responsável por executar o conteúdo do método ready(), tão logo o navegador tenha carregado todos os elementos HTML.

O modo mais comum de utilizarmos ela é em conjunto com uma função anônima, contendo os comandos que desejamos executar. Vejamos um exemplo.

**Listagem 2:** Função anomina dentro da função $(document).ready()

```
<script type="text/javascript">
        $(document).ready(function(){

//o nosso código jquery vai aqui.

        });
    </script>
```

Vamos então unir tudo que aprendemos até agora e ver como seria o seu funcionamento na prática. Para isso vamos unir todos os códigos que geramos ate agora em um único arquivo e executarmos para ver se a mensagem de página carregada ira realmente aparecer.

**Listagem 4:** Modelo jQuery completo

```
<head>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1" />
<title>Introdução jQuery </title>
<!-- Referencia a biblioteca jquery (JS) -->
<script type="text/javascript" src="jquery.js"></script>
<!-- Funcionalidades da página -->
<script type="text/javascript">
$(document).ready(function(){
alert("página carregada")
});
</script>
</head>
<body>
<h1>Página demonstração</h1>
<h2>jQuery biblioteca javascript.</h2>
</body>
</html>
```

Resultado:

![Exemplo página usando jQuery](https://arquivo.devmedia.com.br/artigos/Ricardo_Teixeira/Introducao_jQuery/Introducao_jQuery5.jpg)**Figura 5:** Exemplo página usando jQuery

É importante acessar a página oficial da biblioteca e consultar a documentação, bastante completa.

Assim concluirmos mais esse artigo, espero que tenha sido do agrado e entendimento de todos os leitores. Fiquem à vontade para estar deixando sugestões, dicas e pedidos de novos artigos.

Um abraço a todos.

#### Mais sobre jQUery

[![Primeiros passos com a jQuery](https://arquivo.devmedia.com.br/cursos/imagem/curso_criando-botoes-com-a-jquery_2112.png)Primeiros passos com a jQueryCurso](https://www.devmedia.com.br/curso/curso-jquery/2112)

[![jQuery](https://arquivo.devmedia.com.br/marketing/img/guia-jquery-34340.png)jQueryGuia](https://www.devmedia.com.br/guia/jquery/34340)

[![jQuery substitui o JavaScript?](https://arquivo.devmedia.com.br/noticias/devcast/devcast_a-jquery-substitui-o-javascript_37647.jpg)jQuery substitui o JavaScript?DevCast](https://www.devmedia.com.br/a-jquery-substitui-o-javascript/37647)

Tecnologias: