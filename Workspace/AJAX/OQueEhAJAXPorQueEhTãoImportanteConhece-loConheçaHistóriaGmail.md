# O que é AJAX e por que é tão importante conhece-lo? Conheça a história do Gmail

O AJAX não é novo, mas revolucionou o funcionamento da web e é muito importante até hoje. Neste artigo entenda o por quê!

![img](https://res.cloudinary.com/wagon/image/upload/c_fill,h_40,q_auto,w_40/v1595013216/qffcs1hionbb2pp0b9ig.webp)

Vitor ZucherPublicado em Jun 10, 2020

![O que é AJAX e por que é tão importante conhece-lo? Conheça a história do Gmail](https://res.cloudinary.com/wagon/image/upload/c_fill,g_face,h_460,q_auto,w_488/v1595014098/pbh74vhdeq9vojpvmirg.webp)

Compartilhar artigo

- [*Twitter*](https://twitter.com/intent/tweet?url=https://www.lewagon.com/pt-BR/blog/o-que-e-ajax-a-historia-do-gmail&text=O que é AJAX e por que é tão importante conhece-lo? Conheça a história do Gmail)
- [*Facebook*](https://www.facebook.com/sharer/sharer.php?u=https://www.lewagon.com/pt-BR/blog/o-que-e-ajax-a-historia-do-gmail)
- [*Linkedin*](http://www.linkedin.com/shareArticle?mini=true&url=https://www.lewagon.com/pt-BR/blog/o-que-e-ajax-a-historia-do-gmail&title=O que é AJAX e por que é tão importante conhece-lo? Conheça a história do Gmail&source=lewagon.com)

*Foto: Dmitry Baranovskiy |* [*CC BY 2.0*](https://creativecommons.org/licenses/by/2.0/deed.pt_BR) *
*

- O que é AJAX e como funciona?
- O que é uma requisição HTTP?
- Requisições Sincronizadas e Requisições Assíncronas
- Qual a importância do AJAX para programação?
- AJAX, UX e Performance
- Como surgiu AJAX: A história do Gmail
- A origem do Javascript: HTML, jQuery, XML e node.js
- AJAX e APIs
- Os primeiros passos para aprender a programar em Javascript

### O que é AJAX e como funciona?

Imagine que toda vez que você escrevesse algo na barra de pesquisa do Google, a página inteira tivesse que carregar novamente para mostrar uma sugestão. Ou se tivesse que regarregar toda vez que você arrastasse o mapa no Google Maps. Até mesmo quando você vai verificar se um usuário já existe, por exemplo, no Twitter. Seria muito ruim ficar esperando toda a página recarregar de novo e de novo sempre que ela precisasse conectar ao servidor, certo? E é aí que entra o AJAX. Essa sigla vem de Asynchronous Javascript and XML (Javascript e XML assíncronos). Esse termo se refere a técnicas de programação usadas para fazer com que uma página web se torne mais dinâmica e interativa. O AJAX permite que tudo aconteça numa mesma página, sem que seja preciso recarregá-la por completo toda vez que for necessário conectar ao servidor. Em vez disso, são trocadas pequenas quantidades de informações quando solicitadas **alterando somente o DOM**. (Não sabe o que é o DOM? Então leia [este artigo sobre o básico do JavaScript](https://www.lewagon.com/pt-BR/blog/modern-javascript-in-the-browser)). Isso faz com que além de rápidas, as páginas sejam mais responsivas, o que melhora a experiência do usuário. O primeiro a dar o nome de AJAX para essa técnica foi o Jesse James Garrett, em um artigo chamado “Ajax: A New Approach to Web Applications” (Uma nova abordagem para aplicações web). Apesar de já estar sendo utilizada antes desse texto, foi ele que estabeleceu o nome AJAX e trouxe essa técnica à tona para o mundo da programação. 

### O que é uma requisição HTTP?

O HTTP (Hypertext Transfer Protocol) possui métodos, também chamados de verbos, e é por meio dele que se estabelece a comunicação entre [sites](https://rockcontent.com/br/blog/site/) na web e servidores. 

Mas afinal, o que é esse HTTP? Ele é basicamente um protocolo de pedido e resposta, utilizado para a transferência de página HTML do servidor para a internet. E é por isso que quando você vai entrar em algum site pelo [navegador](https://rockcontent.com/br/blog/navegador/), aparece a expressão HTTP no endereço, é o que está definindo o protocolo usado. Um protocolo é basicamente uma “língua falada” pelo navegador e pelo servidor web, ou seja, um conjunto de regras bem definidas, que descrevem como duas entidades se comunicam. A requisição HTTP possui um cabeçalho (header) e um corpo da mensagem que diz ao servidor o que está sendo requisitado, ao fazer isso, um verbo é utilizado. Ele identifica o que deve ser feito em um determinado recurso. Existem alguns métodos diferentes nessas requisições, são eles



- GET

- POST

- PUT

- PATCH

- DELETE

  

No método GET é por onde nós pedimos a representação de um recurso, ou seja, você faz um pedido para receber informações, e geralmente usamos ele quando estamos navegando em sites através de seus links, pois a requisição é feita por meio da URL. No entanto, existe um limite de caracteres: A string da URL não pode ser maior do que 255. 



Mas já o método POST é usado para a aplicação receber informações do usuário e acrescentá-las à aplicação. E, por causa do número de caracteres, é possível enviar os parâmetros no corpo da mensagem, não estando visíveis na URL. Além do método da requisição, é possível, também, passar parâmetros GETs para o servidor via URL, desde que não ultrapasse o limite definido, mas, se precisar, basta fazer pelo método POST. A resposta que é recebida do servidor é chamada de HTTP response. No header dela tem informações como data, tamanho, tipo de arquivo e informações sobre o servidor.



Já os métodos PUT, PATCH e DELETE são bem simples. Os dois primeiros são para atualizar informações em aplicações web, a diferença é que com o verbo PUT, você pode alterar campos inteiros de dados, já com o PATCH, é possível apenas alterar uma parte. O DELETE, se você sabe inglês, já até imagina o que seja, não é mesmo? Sim, é bem intuitivo: a função dele é remover dados.



### *Mas como isso acontece?*

Bom, primeiro o cliente, (o navegador ou a máquina) pede para o servidor um recurso, ao enviar um pacote de headers, ou cabeçalhos, a um URI ou URL. Ao receber esse pedido, o servidor verifica entre os dados e envia uma resposta, podendo ser outro recurso ou headers. Existem tecnologias como servidores web, linguagens de programação e banco de dados que são executadas na parte de trás do nosso site, ou seja, no back-end. Por outro lado, as tecnologias que são interpretadas pelo navegador, chamamos de tecnologias front-end, pois representa uma camada de interface com o usuário do nosso site. 



Requisições síncronas e requisições assíncronas



Agora que você já sabe o que é uma requisição, vamos entender a diferença entre requisições síncronas e assíncronas. A ideia é que uma requisição síncrona é feita pelo próprio navegador para o servidor web, como quando você digita uma URL ou clica em um link. Essa é uma requisição tradicional. Um exemplo muito comum no nosso dia a dia está em todos os sites que acessamos diariamente. Vamos pegar o Twitter como exemplo: Um usuário digita a URL, dá enter e espera carregar uma página em branco. Enquanto isso, o navegador envia uma requisição da página inicial do Twitter, o servidor web recebe, procura no sistema de arquivos dele se pode responder, monta uma resposta e a entrega para o navegador um arquivo HTML. Ao receber o arquivo HTML, o navegador começa a ler e mostrar algumas coisas para que o usuário possa voltar a interagir. E se o usuário clica no perfil de alguém? Bom, aí o processo se repete: é outra requisição síncrona que será feita, o Twitter vai olhar o banco de dados, ver o que foi publicado por essa pessoa e enviar mais uma resposta para o usuário que estava esperando o navegador mostrar algo para voltar a interagir.

*O twitter especificamente, utiliza de tecnologias como AJAX, atreladas à tecnologia do framework de front-end na linguagem Javascript, conhecido como React para dinamizar a experiência do usuário, adicionando novas informações à interface, sem ter que realizar múltiplas requisições HTTP

Certo, mas e quando você está rolando pela página inicial, vendo os tweets e chega no final, o que acontece? Aparecem mais postagens, não é mesmo? Dessa forma, você consegue continuar interagindo com a página e sem precisar recarregar a página novamente, fazendo outra HTTP request para ter acesso à novas informações. Isso acontece devido à requisição assíncrona: quando o servidor responde e essa resposta chega no navegador, um código JavaScript é chamado e executa uma ação na página, manipulando a DOM do HTML, como por exemplo, pegando os dados das novas publicações e criando elementos HTML dinâmicos.

### Qual a importância do AJAX para a programação?

O AJAX tornou-se mais famoso por volta de 2005, quando Jesse James Garrett escreveu o seu artigo chamado “Ajax: A New Approach to Web Applications”, como dito anteriormente e quando a Google começou a utilizar a técnica (mas sobre ela eu conto daqui a pouco). A partir de então, AJAX começou a fazer muito sucesso, pois as pessoas começaram a perceber que um site poderia ser tão fluido como um software baixado. Essa técnica trouxe diversas utilidades na programação, pois melhorou a tanto o trabalho do desenvolvedor na programação quanto a experiência do usuário. 

Uma das coisas muito úteis e uma das primeiras a ficar muito conhecida, foi a sugestão de busca do Google. Enquanto você insere um termo, o AJAX se conecta com o Google pelos bastidores e então você vê uma caixinha aparecendo bem embaixo de onde está sendo digitado, com sugestões de pesquisa que provavelmente vão coincidir com o que você está querendo procurar. A utilidade do AJAX é tremenda, pois essa técnica surgiu em um momento que os navegadores precisavam se mostrar cada vez mais rápidos para se sobressaíram no mercado, pois a velocidade e a disponibilidade dos servidores não eram tão eficientes. Hoje, com o uso da internet móvel tendo cada vez mais peso em relação à navegação web dos desktops, é muito importante que os sites sejam elaborados com o foco em usabilidade fluida e maior velocidade de carregamento. 


Não só para a evolução da programação, quanto para a vida profissional do programador, o conhecimento em AJAX é muito importante, pois, como você pode ver [neste artigo](https://www.lewagon.com/pt-BR/blog/barreiras-entrada-mercado-ti), pode ser uma ótima ferramenta para te ajudar a se adequar ao mercado de TI se você quiser investir no front-end.



### AJAX, UX e Performance

Apesar de a experiência do usuário (UX) dar mais relevância a quem está usufruindo do site e prestar mais atenção na sua jornada por ele, não é só o marketing que importa, mas o conhecimento técnico e visual acompanhados de fases de monitoramento e testes como testes A/B. Ao focar nesses quatro pontos, a qualidade do site aumenta significativamente pois o torna mais simples, fácil de usar e rápido, o que por consequência, melhora a usabilidade, otimizando a taxas de conversão de visitantes em leads, podendo significar resultados concretos de negócio. Por exemplo, tornar seu site responsivo é essencial. Ser responsivo significa ser capaz de dimensionar as telas adequadamente em qualquer dispositivo, seja em computadores, tablets ou celulares. Além disso, é muito importante que ele seja acessível para todos, como idosos e pessoas com deficiência. 

Para melhorar a navegabilidade, ao programar o site é necessário levar duas coisas em conta. Primeiro, o usuário deve saber onde ele está, ser capaz de determinar sua localização na página atual e saber como voltar nela. Uma navegação estrutural é uma ótima escolha para esse fim. Segundo que o usuário deve conseguir encontrar o que ele quiser rapidamente, por isso é necessário integrar um mecanismo de busca eficiente. Aí é que entra o AJAX. Sites em que os programadores constroem com uma arquitetura moderna baseada no AJAX, podem utilizar técnicas muito interessantes para tornar a navegação rápida. 

Antes, os computadores e a capacidade de processamento de informações eram muito lentos, então as requisições feitas para os servidores, que em maioria, eram localizados nos EUA, junto com a velocidade, não eram uma boa combinação. Principalmente por causa disso, os usuários não exigiam muito de um site. Mas hoje em dia as coisas são muito diferentes, portanto, é essencial cativá-los assim que chegarem no site. Um dos pontos que é muito importante e faz muita diferença são os tempos curtos de carregamento e navegação suave. A performance pode ser melhorada significativamente minimizando o número de solicitações, medindo arquivos CSS e JavaScript e comprimindo respostas. 

Com base em uma estrutura 100% AJAX, somos capazes de criar sites que são personalizados às necessidades dos clientes, fornecer navegação fluida e que funcionam em um alto nível de dinamicidade.

### Como surgiu AJAX: a história do Gmail

Tudo começou quando o engenheiro da Google, Paul Buchheit, resolveu fazer um serviço de correio eletrônico interno para a empresa. Ele pegou o que tinha de mais deficiente nos serviços populares, como os da Yahoo! e da Microsoft e, a partir disso, desenvolveu o produto.

O surgimento do Gmail aconteceu lá em 2004. O produto ganhou popularidade rapidamente porque ele chegou com uma notícia extraordinária: teria 1gb de memória, enquanto seus concorrentes teriam no máximo 6mb. Além de ser uma grande conquista para a época, ainda foi lançado dia 1° de abril, então algumas pessoas acharam que aquilo era algum tipo de brincadeira ou pegadinha, por conta do tamanho desse avanço tecnológico, poderia ‘’ser bom demais para ser verdade’’. Por causa disso, outras organizações que ofereciam serviço de webmail tiveram que se reinventar. Um ano mais tarde, a Google resolveu inovar ainda mais lançando um projeto chamado Infinity Plus One que resolvia alguns problemas que os concorrentes tinham, como a interface, que não era muito agradável, linguagens de programação ultrapassadas e falta de organização das mensagens no inbox. Outra coisa que colocava o Gmail muito à frente dos outros era a velocidade em que os processos aconteciam, muito mais rápidos do que as outras plataformas, que eram muito lentas. Posteriormente o Gmail foi melhorado com a chegada do AJAX, a sua técnica foi implementada ao serviço de webmail e isso aprimorou mais ainda suas ferramentas.

### A origem do Javascript: HTML, jQuery e XML

Primeiramente é bom lembrar que o Javascript é uma linguagem de programação interpretada, não compilada, e é executada no interior de um programa, que no caso é o navegador. Ela serve para criar páginas dinâmicas, como vimos, e é uma das linguagens utilizada para criar um site com a técnica do AJAX. Ela é uma das linguagens de programação mais utilizada na atualidade. Mesmo sendo relativamente antiga, lançada em 1996, ela continuou evoluindo, a todo momento são lançados novos frameworks. 

Você também pode dar uma olhada [neste post](https://www.lewagon.com/blog/modern-javascript-in-the-browser) sobre conceitos que você precisa dominar para trabalhar com Javascript.

Quando foi criado, o Javascript recebeu o nome de Mocha e, posteriormente, foi chamado de Livescript. Isso aconteceu porque os desenvolvedores tinham a intenção de dar mais “vida” às páginas com ela, com mais interatividade, porque na época só existiam sites estáticos escritos em HTML. Só que, como sabemos, esse não foi seu nome final. Muita gente acaba se enganando, ao pensar que Java e Javascript, têm alguma coisa a ver, mas isso não passou de uma jogada de marketing, porque na época o Java já era uma linguagem de programação muito popular, e por isso o nome Javascript, foi uma maneira de pegar carona na popularidade do Java. Atualmente ele é mantido pela ECMA, uma associação de software que fez ele se popularizar entre os navegadores.

### HTML

HTML é um acrônimo para Hypertext Markup Language, que significa linguagem de marcação de hipertexto. Ela é a linguagem responsável por exibir, estruturar e organizar a informação do site. Podemos dizer que o HTML é a forma que escrevemos o nosso código para que os navegadores entendam o que queremos e, através das tags, organizamos e damos significado à nossa informação.

### JQuery


O jQuery é uma biblioteca de multiplataforma projetada para simplificar a criação de scripts e foi criada em 2006 pelo Engenheiro de Software John Resig. A maioria dos sites da web utilizam essa biblioteca atualmente, isso dá-se principalmente pelo fato de ela simplificar a sintaxe para encontrar, selecionar e manipular os elementos de uma estrutura de HTML no DOM .




Já o XML é um formato de arquivo criado para que informações pudessem ser lidas facilmente tanto por humanos, quanto por máquinas, além de permitir que informações sejam adicionadas ou repetidas sem que houvesse uma mudança estrutural. 



### AJAX e APIs

API significa Application Programming Interface (Interface de Programação de Aplicações). Ela serve para que um sistema possa se comunicar, ou seja, compartilhar informações, como por exemplo protocolos e ferramentas, com o outro. Seria um “minissistema” que interliga um maior com quem quiser utilizar os recursos da API. 

Ok, mas e uma API RESTful? Bom, esse segundo nome não muda muita coisa, pra falar a verdade. API REST acaba sendo como uma API qualquer, a diferença é que a primeira utiliza a versão 1.1 do protocolo HTTP e, além disso, faz todas as 4 CRUD actions: Create, Read, Update e Delete. Para fazer uma requisição HTTP, você deve utilizar o método fetch, pois, ao ser invocado, ele traz dados da URL que o programador especifica no argumento. É uma opção que estão utilizando muito ultimamente e sendo implementada nos navegadores para substituir como as requisições HTTP eram feitas no browser antes. Vale lembrar, também, que esse pedido é assíncrono, ou seja, o usuário não fica preso, esperando a resposta enquanto a requisição é feita.

### Os primeiros passos para aprender a programar em Javascript & AJAX requests

Hoje em qualquer computador é possível rodar Javascript, mesmo zerado, todo formatado, basta ter um navegador para rodar um código Javascript, o que facilita muito a linguagem que é uma das mais populares da atualidade. Mas é bom lembrar que, se você quiser escrever o código, é necessário instalar, por exemplo, o Node.js.

Para desenvolvimento web, primeiro, tente aprender HTML, pois é uma linguagem de marcação, não de programação, então é um ótimo lugar pra começar e uma das bases para Javascript.

Você também pode desenvolver projetos pessoais, mesmo sem ter aprofundado muito. Participe de fóruns, tire dúvidas, faça networking, conheça outros desenvolvedores, seja no seu local de estudo, trabalho ou até mesmo na internet. As comunidades do github e do facebook podem te ajudar a tirar muitas dúvidas sobre carreira e primeiros passos.

Leia código, veja os de outras pessoas, participe de projetos. Dessa forma, você pode ver o que outros desenvolvedores profissionais trabalham, como usam a lógica para solucionarem problemas de programação com a linguagem. Você também pode usá-los como base para o seu projeto. Outros lugares que você também pode ver exemplos de códigos, são em livros de Javascript, alguns muito bons e famosos são: You don’t know Javascript; Use a cabeça! Programação Javascript; PHP, My SQL & Javascript for dummies e Segredos do Javascript ninja.

Além disso, se já tiver certeza que quer aprender a programar mas não sabe como? Ou quer um caminho menos formal do que um curso acadêmico em Ciências da Computação, você pode fazer um ***bootcamp\***. Não sabe o que são bootcamps? [Esse post](https://www.lewagon.com/pt-BR/blog/bootcamps-programação-funcionam) explica bem direitinho o que são e se funcionam, vale a pena dar uma conferida. 