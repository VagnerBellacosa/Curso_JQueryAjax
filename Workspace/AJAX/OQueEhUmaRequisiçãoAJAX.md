# O que é uma requisição AJAX?

Hoje, é relativamente comum estarmos em contato com requisições AJAX. Confira neste artigo como essa requisição funciona.

 cerca de 1 ano atrás

[Artigos](https://www.treinaweb.com.br/blog)O que é uma requisição AJAX?

Hoje, é relativamente comum estarmos em contato com requisições **AJAX**. Sabe quando você está preenchendo um formulário de uma aplicação e você clica no botão para enviar os dados, mas a página não é atualizada? Ali, por “debaixo dos panos”, está acontecendo uma requisição AJAX. Ao clicar no botão, automaticamente a página envia os dados ao servidor e recebe uma mensagem de volta, seja de sucesso ou de erro, sem que a página seja recarregada.

**AJAX** é um acrônimo para *Asynchronous Javascript and XML*, ou *JavaScript e XML Assíncronos*. É uma técnica utilizada pelos desenvolvedores para criar aplicações capazes de manter a comunicação assíncrona com o servidor. Essa técnica combina várias tecnologias como **[HTML](https://www.treinaweb.com.br/blog/o-que-e-e-como-comecar-com-html-e-css/)** ou **xHTML**, que fornecem os objetos para a estrutura do documento; e o **DOM** *(Document Object Model)*, que define a estrutura que esse documento terá. O [JavaScript](https://www.treinaweb.com.br/blog/o-que-e-e-como-comecar-com-javascript/) utiliza a estrutura definida pelo DOM para acessar dinamicamente partes desse documento.

Além disso, o JavaScript utiliza um objeto chamado **XMLHttpRequest**. Este objeto é o responsável por realizar as requisições AJAX, permitindo o compartilhamento assíncrono de informações entre cliente e servidor. As informações trocadas entre cliente e servidor geralmente estão no formato de um [JSON](https://www.treinaweb.com.br/blog/o-que-e-json/).

Alguns exemplos de aplicações que fazem o uso de requisições AJAX são as notificações de Trending Topics do Twitter e os chats.



![JQuery Completo](https://d2knvm16wkt3ia.cloudfront.net/assets/svg-icon/jquery.svg)

##### CursoJQuery Completo

[Conhecer o curso](https://www.treinaweb.com.br/curso/jquery)

### Como o AJAX funciona?

Primeiramente, temos que relembrar que, quando acessamos uma página por um navegador, o navegador está do lado do cliente, enquanto a página está no servidor.

Precisamos saber como funciona uma requisição no modelo de comunicação **síncrona**. Neste primeiro caso, ao fazer uma requisição, a aplicação cliente ficará em espera e não permitirá que os usuários continuem interagindo até receber uma resposta do servidor. Este servidor realizará uma série de tarefas e depois retornará as informações solicitadas em outra página, produzindo um recarregamento completo da aplicação.

![img](https://dkrn4sk0rn31v.cloudfront.net/uploads/2020/08/modelo-comunicacao-sincrona.png)

Para ajudar a melhorar a [experiência do usuário](https://www.treinaweb.com.br/blog/ux-a-importancia-da-experiencia-do-usuario-nos-projetos/), no AJAX, a requisição é chamada em segundo plano.

O navegador gera uma chamada do JavaScript que irá ativar o XMLHttpRequest. Com isso, em segundo plano, o navegador cria uma requisição [HTTP](https://www.treinaweb.com.br/blog/http-2-o-que-voce-deve-saber/) para o servidor. Este recebe a requisição, busca os dados e envia para o navegador. O navegador, ao receber a resposta de volta, utiliza o DOM para modificar a página atual de maneira que esta reflita a resposta que veio do servidor. Como a reação na página acontece via navegação e modificação do [DOM](https://www.treinaweb.com.br/blog/o-que-e-dom-virtual-dom-e-shadow-dom/), a página não é recarregada, o que oferece uma experiência muito mais fluída para o usuário.

![img](https://dkrn4sk0rn31v.cloudfront.net/uploads/2020/08/modelo-comunicacao-assincrona-AJAX.png)

As aplicações web que implementam AJAX são capazes de se atualizar continuamente, sem a necessidade de recarregar a página completamente, já que o JavaScript somente manipula o DOM quando recebe a resposta assíncrona recebida do servidor. Isso é possível porque o AJAX funciona como um intermediário entre o cliente e o servidor: as solicitações e respostas produzidas serão gerenciadas em segundo plano, otimizando dessa maneira a velocidade, interatividade e usabilidade das aplicações.

- [#requisição](https://www.treinaweb.com.br/blog/tag/requisicao)
- [#AJAX](https://www.treinaweb.com.br/blog/tag/ajax)
- [#JavaScript. XML](https://www.treinaweb.com.br/blog/tag/javascript-xml)