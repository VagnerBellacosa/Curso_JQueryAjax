<!-- PROJECT SHIELDS -->

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
![Bootcamps na Digital Innovation One](BootCamps/Images/capa.png "Bootcamps")





# Curso_JQueryAjax
Primeiros passos em JQuery e Ajax







# O Que é jQuery e Para Que Serve?

![O Que é jQuery e Para Que Serve?](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/01/O-que-e-jquery.png)

jQuery é uma biblioteca popular do [JavaScript](https://www.hostinger.com/tutorials/what-is-javascript). Ela foi criado por John Resig em 2006 com o propósito de facilitar a vida dos desenvolvedores que usam JavaScript nos seus sites. Não é uma linguagem de programação separada, funciona em conjunto com o JavaScript. Com jQuery, você vai conseguir fazer muito mais com menos – eu vou explicar logo mais.

Criar códigos pode ser um pouco cansativo, especialmente quando isso envolve muitas strings. A jQuery compacta várias linhas de código em uma única função. Assim, você não precisa reescrever todos os blocos repetidamente para concluir sua tarefa.

Conteúdo

- [Exemplos de jQuery](https://www.hostinger.com.br/tutoriais/o-que-e-jquery#Exemplos-de-jQuery)
- [Recursos Importantes do jQuery](https://www.hostinger.com.br/tutoriais/o-que-e-jquery#Recursos-Importantes-do-jQuery)
- [Vantagens jQuery](https://www.hostinger.com.br/tutoriais/o-que-e-jquery#Vantagens-jQuery)

## **Exemplos de jQuery**

Você pode criar efeitos de slide com apenas algumas linha de código.

Você pode usar os comandos **SlideDown()**, **SlideUp()** e **SlideToogle()**.

```
$("#flip").click(**function**(){

 $("#panel").slideDown();

});

```

Com jQuery, você também pode esconder os elementos em HTML com os comandos **Hide()** e **Show()**. Veja:

```
$("#hide").click(**function**(){

 $("p").hide();

});

$("#show").click(**function**(){

 $("p").show();

});

```

E aqui está um exemplo de animação:

```
$("button").click(**function**(){

 $("div").animate({

​     left: '250px',

​     height: '+=150px',

​     width: '+=150px'

 });

});
```

E aqui você vê o fragmento de um código para entender como manipular o CSS.

```
$("button").click(**function**(){

 $("h1, h2, p").toggleClass("blue");

});
```

## **Recursos Importantes do jQuery**

Uma característica do motivo pelo qual o jQuery se tornou tão famoso e popular é, provavelmente, os recursos de plataforma cruzada. Os erros são corrigidos automaticamente e a execução acontece da mesma maneira nos navegadores mais usados, como Chrome, Firefox, Safari, MS Edge, IE, Android e iOS.

jQuery também torna o Ajax muito mais simples. Ajax funciona de forma assíncrona com o código, que significa que o código escrito com o Ajax pode se comunicar com o servidor e atualizar seu conteúdo sem precisar recarregar a página.

Mas isso vem com alguns problemas. Diferentes navegadores executam a API do Ajax de maneira diferente. Assim, o código deve aderir a todos os navegadores. Se for feito manualmente, esse é um trabalho difícil e demorado. Felizmente, o jQuery faz todo o trabalho manual e adapta o código a todos os navegadores da web.

Depois, há a manipulação do [DOM (Document Object Model)](https://www.w3.org/TR/WD-DOM/introduction.html) com vários meios sobre como fazer isso. Mas, para simplificar, ele permite que você insira e/ou remova elementos DOM em uma página HTML, bem como linhas mais simples.

Criar animações também é simples com o jQuery. Como no exemplo de código acima, você consegue executar tudo com algumas linhas de código, tudo o que você precisa é inserir as variáveis.

A transferência de documentos HTML, bem como a manipulação de efeitos e eventos, também são melhores com o jQuery.

#### 

Você precisa conhecer melhor a Hostinger! Nós temos o plano ideal para cada projeto e mais de 800 extensões de domínio. É só escolher!

Para o melhor projeto, a melhor oferta!

[Usar Cupom](https://www.hostinger.com.br/cart/add/hosting-hostinger-premium/order_period/3?coupon=START_BLOG)


## **Vantagens jQuery**

Os benefícios de usar o jQuery são substanciais. O slogan “Escreva menos, faça mais” tem tudo a ver com a jQuery. Quando você aprender a como usar jQuery (que é muito fácil), você será capaz de executar todas os tipos de ações com facilidade.

Considerando que é a biblioteca JavaScript mais popular disponível, existem muitos materiais que ensinam como [aprender jQuery](https://www.bitdegree.org/tutorials/learn-jquery/). Mas, para isso, é preciso um conhecimento básico de JavaScript, [HTML](https://www.hostinger.com/tutorials/what-is-html) e CSS.

Se você está usando JavaScript, é quase obrigatório usar a jQuery por tantos benefícios que isso traz, já que o único desafio será aprender como usar e então aplicar no seu trabalho!

----

# O Que é AJAX e Como Funciona?

![O Que é AJAX e Como Funciona?](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/01/O-Que-e-AJAX-e-Como-Funciona.png)

**AJAX** significa ***Asynchronous JavaScript and XML\***, ou **JavaScript e XML Assíncronos**, em bom português. Ele é um conjunto de técnicas de desenvolvimento voltado para a web que permite que aplicações trabalhem de modo assíncrono, processando qualquer requisição ao servidor em segundo plano.

Pareceu um pouco confuso? Não se preocupe, vamos explicar a terminologia de cada palavra para você entender perfeitamente.

O **JavaScript** é uma linguagem de programação bem conhecida. Entre suas funcionalidades, está a capacidade de gerenciar conteúdos dinâmicos de um site e permitir a interação dinâmica com o usuário. O XML  (*eXtensible Markup Language*), como o nome sugere, é uma variação de linguagem de marcação no estilo do HTML. Enquanto o HTML é utilizado para exibir dados, o XML os armazena e transmite.

Tanto o JavaScript quanto o XML trabalham de forma assíncrona no AJAX. Assim, qualquer aplicação que use AJAX pode enviar e receber dados do servidor sem precisar recarregar a página inteira.

## Conteúdo

- [Exemplos de AJAX na Prática](https://www.hostinger.com.br/tutoriais/o-que-e-ajax#Exemplos-de-AJAX-na-Pratica)
- [Como o Ajax Web Funciona?](https://www.hostinger.com.br/tutoriais/o-que-e-ajax#Como-o-Ajax-Web-Funciona)
- [Conclusão](https://www.hostinger.com.br/tutoriais/o-que-e-ajax#Conclusao)

## **Exemplos de AJAX na Prática**

Imagine a ferramenta de sugestões de pesquisa do Google. Ela ajuda a completar as palavras que você digita em tempo real enquanto a página permanece estática.

No início dos anos 90, quando a internet ainda não era tão avançada, a mesma funcionalidade iria exigir que a página fosse recarregada sempre que uma nova sugestão de pesquisa aparecesse na tela. O AJAX permite a troca de informações simultânea sem interferir com outras funções.
![Caixa de pesquisa do google sugerindo outras opções com o AJAX web](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/01/sugestao-de-pesquisa-do-google-1.png)

Na realidade, o conceito de AJAX já existe desde a metade da década de 90. Porém, só começou a receber mais reconhecimento quando o Google o incorporou no Google Mail e Google Maps em 2004. Atualmente, ele é bastante utilizado em diversas aplicações web para melhorar o processo de comunicação com o servidor.

Esses são alguns exemplos de como o AJAX impacta nossas vidas diariamente.

- **Sistemas de Votação e Avaliação**

Você já avaliou algum produto que comprou na internet? Já preencheu algum formulário online? Ambas as operações utilizam o AJAX. Ao clicar no botão de voto ou de avaliação o site irá atualizar os cálculos sem precisar recarregar a página.

- **Canais de Chat**

Alguns sites possuem canais de bate-papo em sua página principal para se comunicar com seus clientes e prestar serviço de suporte técnico. Com o AJAX, você pode continuar navegando no site enquanto troca mensagens sem que elas desapareçam.

- **Notificações de Trending do Twitter**

O Twitter recentemente passou a utilizar o AJAX em suas atualizações. Sempre que novos tweets são feitos sobre um certo *trending topic* o Twitter automaticamente atualiza as novas figuras sem afetar a página principal.

Simplificando, o AJAX torna o processo de multitarefas mais simples. Sempre que você encontrar uma situação em que duas operações funcionam simultaneamente, uma em execução e a outra ociosa, é bem provável que o AJAX esteja envolvido.

#### 

Se você deseja melhorar seu site, não se esqueça de mostrar ao Google e aos seus clientes que você cuidou dos problemas de segurança. Você pode [comprar SSL](https://www.hostinger.com.br/comprar-ssl) na Hostinger agora mesmo e garantir a proteção dos seus visitantes!

 
## **Como o Ajax Web Funciona?**

É importante lembrar que o AJAX não é uma única tecnologia, ou até mesmo uma linguagem de programação. Como mencionado antes, o AJAX é uma série de técnicas de desenvolvimento voltadas para web. O sistema geralmente é composto por:

- **HTML/XHTML** para linguagem principal e CSS para a apresentação.
- **O** ***Document Object Model\*** **(DOM)** para exibição dinâmica dos dados e interação.
- **XML** para a troca de dados e XSLT para a manipulação. Muitos desenvolvedores começaram a substituir pelo **JSON** por ser mais semelhante ao JavaScript.
- O objeto **XMLHttpRequest** para a comunicação assíncrona.
- Finalmente, a linguagem de programação **JavaScript** para juntar todas essas tecnologias.

É preciso um pouco de conhecimento técnico para entender completamente o funcionamento. Porém, o procedimento geral de como o AJAX funciona é relativamente simples. Confira o diagrama e a tabela de comparação abaixo para entender melhor.

### **Diagrama** ![Gráfico informativo sobre o que é AJAX web](https://www.hostinger.com.br/tutoriais/wp-content/uploads/sites/12/2019/01/O-Que-e-AJAX-e-Como-Funciona-infografico.png)

### **Tabela de comparação**

| **Modelo convencional**                                      | **Modelo AJAX**                                              |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Uma requisição HTTP é enviada do navegador para o servidor.O servidor recebe a requisição e busca os dados.O servidor envia os dados requisitados para o navegador.O navegador recebe os dados e recarrega a página para fazer com que apareçam.Durante esse processo, os usuários não conseguem fazer nada além de esperar que seja concluído. Além de ser uma perda de tempo para o usuário, também demanda muitos recursos do servidor. | O navegador gera uma chamada do JavaScript que então ativa o XMLHttpRequest.Em segundo plano o navegador cria uma requisição HTTP para o servidor.O servidor recebe a requisição, busca os dados e envia para o navegador.O navegador recebe os dados requisitados que irão aparecer imediatamente na página. Não é necessário recarregar. |

## **Conclusão**

Além de aprender o que é AJAX, um dos propósitos do tutorial é explicar como o AJAX melhora a experiência do usuário. Seus visitantes não precisam mais aguardar um tempão para ter acesso ao seu conteúdo. Claro que muito se baseia na sua necessidade. O Google, por exemplo, permite que os usuários escolham entre o AJAX e a versão convencional ao utilizar o Google Mail. Por isso, fica a nossa dica: coloque sempre as necessidades de seus visitantes em primeiro lugar antes de decidir.





---

#### * DIO - Digital Inovation One *
######  [Inscreva-se na Dio](https://web.dio.me/sign-up?ref=R5J3ZLTIFS)  

######  [Vagner Bellacosa perfil na Dio](https://web.dio.me/users/vagnerbellacosa?tab=achievements)  

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/VagnerBellacosa/Curso_JQueryAjax.svg?style=for-the-badge
[contributors-url]: https://github.com/VagnerBellacosa/Curso_JQueryAjax/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/VagnerBellacosa/Curso_JQueryAjax.svg?style=for-the-badge
[forks-url]: https://github.com/VagnerBellacosa/Curso_JQueryAjax/network/members
[stars-shield]: https://img.shields.io/github/stars/VagnerBellacosa/Curso_JQueryAjax.svg?style=for-the-badge
[stars-url]: https://github.com/VagnerBellacosa/Curso_JQueryAjax/stargazers
[issues-shield]: https://img.shields.io/github/issues/VagnerBellacosa/Curso_JQueryAjax.svg?style=for-the-badge
[issues-url]: https://github.com/VagnerBellacosa/Curso_JQueryAjax/issues
[license-shield]: https://img.shields.io/github/license/VagnerBellacosa/Curso_JQueryAjax.svg?style=for-the-badge
[license-url]: https://github.com/VagnerBellacosa/Curso_JQueryAjax/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/VagnerBellacosa/
[product-screenshot]: BootCamps/images/capa.png
