# AJAX Tutorial

## Neste artigo aprenderemos um pouco sobre o que é AJAX. AJAX é o acrônimo de Asynchronous Javascript and XML, que em português significa “Javascript e XML assíncronos”.

- [Artigos](https://www.devmedia.com.br/artigos/)[JavaScript](https://www.devmedia.com.br/artigos/javascript)AJAX Tutorial

Neste artigo aprenderemos um pouco sobre **o que é AJAX**, quais as ideias de interface do usuário que o motivaram e quais as tecnologias envolvidas em seu funcionamento. Em seguida, construiremos uma aplicação de exemplo utilizando JSF 2, que possui o AJAX já embutido, para mostrar como podemos melhorar sua interatividade e responsividade.

### O que é AJAX?

**AJAX é o acrônimo de Asynchronous Javascript and XML, que em português significa “Javascript e XML assíncronos”**. Entendendo melhor o significado, seria a chamada de um recurso no servidor a partir de um código Javascript no navegador web, de forma que o resultado atualize apenas uma parte da página sem precisar fazer uma atualização dela inteira. Esta chamada é assíncrona, ou seja, o script que a chamou continua sua execução sem esperar pela resposta. Quando o servidor responde, uma função Javascript especificada trata corretamente os dados retornados, fazendo a atualização de parte da tela apenas.

<iframe src="https://www.youtube.com/embed/C2khVGYh__M" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Assista agora: [Curso de AJAX](https://www.devmedia.com.br/curso/o-que-e-ajax/2175)

O termo AJAX foi criado por Jesse [James Garrett](https://pt.wikipedia.org/wiki/Jessé_James_Garret), em 2005, em seu artigo chamado “Ajax: A New Approach to Web Applications” (AJAX: Uma Nova Abordagem para Aplicações Web), onde comparava a interatividade proporcionada pelas aplicações desktop com as aplicações web. Neste artigo, ele utiliza tal termo para referir-se ao uso conjunto de tecnologias que já existiam há muito tempo, como [Javascript](http://www.devmedia.com.br/guia/guia-de-referencia-javascript/34372), DOM, CSS, XML, etc., para a criação de interfaces mais dinâmicas e responsivas. Ele cita as ferramentas do Google como exemplo de boa interação. Portanto, quando você usa AJAX, você está utilizando um conjunto de técnicas ou, ainda melhor, uma abordagem de programação para a web focada em proporcionar uma melhor interação para o usuário. Não é uma ferramenta ou framework que pode ser baixado de algum site, pois os componentes de software que são fundamentais para esta abordagem estão presentes em todos os navegadores web: [HTML](http://www.devmedia.com.br/guia/html/38051), XHTML e XML; CSS; DOM; Javascript; e, o principal, um componente chamado XMLHttpRequest. Nos parágrafos seguintes, abordaremos brevemente o que é cada um deles e como contribuem para o AJAX.

O tema é útil para desenvolvedores, projetistas e arquitetos envolvidos com a construção de interfaces de usuário que procuram criar softwares mais interativos, com interfaces mais ricas, intuitivas e responsivas.

Neste artigo, introduziremos o **conceito de AJAX**, abordando sobre a origem do termo e mostrando cada uma das tecnologias envolvidas em seu funcionamento, como XHTML, CSS, DOM e JavaScript. O AJAX agora vem integrado ao JavaServer Faces 2, parte integrante do Java EE 6, dispensando a necessidade de uso de frameworks externos. Para demonstrar essa integração, criaremos uma aplicação na prática, explicitando como é fácil **utilizar o AJAX** da forma como hoje ele é disponibilizado.

Tendo em vista que o que vamos aprender neste artigo é como utilizar scripts síncronos e assíncronos, um dos principais conceitos que devemos entender é “o que é sincronia”. Dizemos que duas coisas são síncronas quando há uma exata coincidência no tempo ou no ritmo delas. No esporte, sempre ouvimos falar em nado sincronizado, onde as atletas coincidem todos os movimentos do início ao fim da execução da coreografia.

Na computação, quando uma tarefa precisa aguardar a tarefa anterior ser concluída para iniciar sua execução, dizemos que estas tarefas são síncronas. Por outro lado, vamos supor agora que duas ou mais tarefas precisam ser executadas e que não há nenhuma dependência entre elas. Ganharíamos tempo se elas fossem executadas ao mesmo tempo, contanto que o instante de conclusão de cada uma não importasse nem influenciasse a outra. Neste caso, dizemos que as tarefas foram executadas de forma assíncrona. Tais conceitos são fundamentais para entendermos como criar aplicações mais dinâmicas e interativas.

Sempre foi um grande desafio para os desenvolvedores de software para internet criar interfaces que fossem fáceis de operar, intuitivas e que procurassem minimizar a demora de comunicação com o servidor de internet para exibir dados na tela. Quando o conceito de AJAX surgiu, veio propondo uma nova abordagem de interação para o desenvolvimento de interfaces para internet. Algumas aplicações disponíveis na época de seu surgimento, como sítios de webmail, busca, mapas, mensagens instantâneas, entre outros, já utilizavam as **tecnologias do AJAX**. Tais sítios eram exemplos de inovação em interatividade.

Na época, já havia vários frameworks para o desenvolvimento da camada de apresentação das aplicações que procuravam atender às novas necessidades de evolução das interfaces web. Para o Java, a partir de 2004, lançaram o [JavaServer Faces](https://www.devmedia.com.br/guia/jsf-javaserver-faces/38322) 1.0 (JSF), cujo objetivo era facilitar o desenvolvimento destas interfaces de usuário de aplicações Java para a internet. Com o Java EE 6, veio a versão 2.0 do JSF. Tal framework oferece recursos similares aos encontrados em interfaces para desktop, evita que equipes de desenvolvimento precisem dominar tecnologias como JavaScript, HTML e CSS, maximizava a produtividade dos desenvolvedores, auxilia na criação e reuso de **componentes visuais e já vem com AJAX integrado**.

Considerando vantagens como facilidade, interatividade, entre outras citadas até agora, **neste artigo apresentamos o que é AJAX**, quais os benefícios do sincronismo/assincronismo propiciado por ele, quais as tecnologias envolvidas e veremos como ele está embutido no JSF 2 através de uma aplicação exemplo.

### HTML, XML e XHTML

Todo navegador web compreende HTML (HyperText Markup Language ou Linguagem de Marcação de Hipertexto), que é uma linguagem formada por tags, ou marcadores, que são interpretadas pelos navegadores. Estes marcadores indicam como renderizar e exibir o conteúdo das páginas web. Um exemplo de uma página simples com suas tags HTML pode ser visto a seguir:

```
<html>

    <body>
      <h1>Aqui seria o título da página</h1>
      <p>Algum texto</p>
    </body>
  </html>
```

Não havia muito rigor quanto à utilização correta das tags: elas poderiam ser formadas por letras maiúsculas e/ou minúsculas, era possível ter uma tag de abertura, <p> por exemplo, sem ter a de fechamento,</p>, e ainda assim alguns navegadores conseguiam renderizar as páginas corretamente, embora, às vezes, o resultado da renderização fosse uma página com formatação irregular. Como hoje há muitos dispositivos diferentes que utilizam navegadores web, nem todos possuem um interpretador HTML poderoso, que consiga lidar com estes erros. Por conta destes e de outros fatores, ao longo dos anos, houve algumas melhorias para auxiliar os interpretadores HTML dos navegadores, de forma que agora as tags seguem o padrão XML (eXtensible Markup Language ou Linguagem de Marcação Extensível) para representar as páginas web, chamado XHTML (eXtensible HyperText Markup Language).

A principal diferença entre HTML e XHTML é que a formação das tags fica um pouco mais rigorosa, de forma que se houver qualquer erro, o documento não é considerado válido. Com XHTML, as tags devem sempre ser formadas por letras minúsculas e possuir as tags de abertura e fechamento corretamente definidas. Por esta formalização, XHTML tem se tornado um padrão.

**Nota**: HTML e XHTML tratam da representação dos elementos de uma página web, sejam eles visíveis ou não. A seguir falaremos de uma técnica para estilização gráfica destes elementos.

### CSS

A HTML não tinha como objetivo possuir tags para formatação de cor, fonte e estilo dos elementos de uma página. Seu papel era apenas o de definir o conteúdo da mesma. A partir da HTML 3.2, resolveu-se adicionar tais tags para formatação visual. No entanto, o que parecia ajudar na construção de interfaces mais ricas, representou o início de um pesadelo para os desenvolvedores de sítios web, pois agora eles podiam ter os elementos visualmente mais agradáveis, mas precisavam adicionar estas novas tags em cada elemento de cada página. Imagine possuir um portal com todos os cabeçalhos das páginas, títulos, fonte, cor dos textos, tudo padronizado. O problema ocorria quando havia necessidade de alterar alguma característica de uma letra, ou estabelecer outro padrão visual, pois era preciso fazer a mudança em todas as páginas onde a tag era utilizada.

Procurando resolver este problema, a W3C ([World Wide Web Consortium](https://www.w3.org/)) criou o [CSS](http://www.devmedia.com.br/guia/css/38149) (Cascading Style Sheets), ou simplesmente Folhas de Estilo, que são marcações para formatação visual dos elementos de uma página web, e lançou o HTML 4.0, padronizando-o. Isto possibilitou a remoção de todas as tags de formatação dos documentos HTML, colocando-as à parte em um arquivo CSS separado. Desta forma, quando se faz necessário alterar a fonte de uma letra em todas as páginas, basta alterar neste arquivo que a mudança se reflete em todos os lugares.

Com XHTML e CSS, os navegadores podem renderizar corretamente os elementos de uma página web e exibi-los de uma forma graficamente rica. A seguir abordaremos como se dá a representação e a manipulação destes elementos internamente no navegador.

### DOM

DOM, abreviação para Document Object Model (Modelo de Objeto de Documentos), representa uma página web como uma hierarquia ou estrutura de árvore, onde cada elemento da página, tais como imagens, botões, tabelas e textos, são representados como nós e renderizados pelo navegador web. Um exemplo de acesso a um nó utilizando a estrutura disponibilizada pelo DOM seria

document.form1.button.value = "Click Me". Neste caso, estaríamos alterando o texto de um botão de um formulário HTML cujo nome é form1, que é um nó filho do nó raiz document.

Veremos a seguir como é possível criar um script que manipule esta árvore dinamicamente, inserindo, excluindo ou alterando os nós da mesma.

### JavaScript, a linguagem para juntar tudo

JavaScript é uma linguagem de script criada inicialmente para o navegador web Netscape Navigator, em 1995. Com as possibilidades que JavaScript propiciava para a interação de páginas web, a Microsoft resolveu criar uma implementação de script própria para o IE, chamada JScript, definindo assim uma segunda linguagem, ou dialeto, de script de navegador. Procurando evitar que os navegadores tivessem que lidar com linguagens de script diferentes, em 1996 resolveu-se padronizá-las, quando a Ecma International criou o padrão ECMAScript.

A partir daí, todo navegador web passou a ter um interpretador JavaScript (também chamado de motor) que deve ser compatível com o ECMAScript e obedecer aos padrões da W3C (que padroniza as APIs da linguagem).

**Nota**: A título de curiosidade, os navegadores Firefox, Google Chrome, Internet Explorer e Safari utilizam os interpretadores JägerMonkey, V8, Chakra e Nitro, respectivamente.

A combinação entre [JavaScript](https://www.devmedia.com.br/guia/javascript/34372), DOM e XHTML representa um conjunto poderoso de ferramentas para criação de uma interface de usuário web. O XHTML força a criação de uma página web bem formatada. Esta formatação sem erros facilita a identificação correta dos elementos na hora da criação da árvore DOM, onde cada elemento da página será um nó da árvore. Com esta estrutura de árvore em memória, é possível [utilizar JavaScript](https://www.devmedia.com.br/javascript-tutorial/37257) para manipular seus nós, através da definição de funções que são chamadas quando o usuário realiza alguma operação, como um clique, movimento do mouse, pressionar de alguma tecla, entre outros. O exemplo a seguir mostra uma função que, ao ser chamada a partir de algum evento, cria um novo elemento div e o adiciona à página web:

Saiba mais: [JavaScript DOM: introdução à API](https://www.devmedia.com.br/javascript-dom-introducao-a-api/30161)

```
function insereDiv() {

  var newTag = document.createElement("div");
  document.body.appendChild(newTag);
}
```

As linhas de código anteriores são um exemplo bem elementar de uso do JavaScript, através da função insereDiv(), e de uso dos nós do DOM, como document e body, e seus métodos createElement() e appendChild().

Para a nossa compreensão completa das **tecnologias envolvidas no AJAX<**, abordaremos a seguir o último elemento deste conjunto que favorece interfaces mais interativas e responsivas.

### O objeto XMLHttpRequest

XMLHttpRequest é o componente técnico que torna possível a comunicação assíncrona com o servidor. O que vimos até então, limita-se a trabalhar no lado cliente da comunicação na internet, ou seja, [CSS](https://www.devmedia.com.br/guia/css/38149), XHTML, DOM e JavaScript funcionam apenas no navegador.

Inicialmente, a Microsoft criou um objeto ActiveX, que estabelecia uma conexão com recursos no servidor. Esta ideia logo foi padronizada pela W3C, criando-se o objeto XMLHttpRequest e integrando-o ao JavaScript. Deste modo, para estabelecer uma comunicação com o servidor, bastaria ter uma função JavaScript com um código similar ao mostrado a seguir:

```
var xmlhttp;
xmlhttp=new XMLHttpRequest();
xmlhttp.onreadystatechange=funcaoTrataRespostaServidor;
xmlhttp.open("GET","nome_recurso_servidor",true);
xmlhttp.send();
```

De uma maneira muito elementar (na prática precisaria de alguns detalhes a mais), estas são as linhas de código que permitiriam a uma função Javascript, em um navegador, acessar algum recurso no servidor. Os grandes responsáveis por esta mágica são os métodos open() e send() e a propriedade onreadystatechange, na qual você indica o nome da função JavaScript que tratará a resposta do servidor. O parâmetro booleano do método open() indica se a comunicação será assíncrona ou síncrona.

Basicamente, todo framework para **desenvolvimento web que disponibiliza recursos AJAX** faz uso das técnicas descritas até aqui, combinando-as de forma a tornar bem mais fácil indicar que recursos serão chamados no servidor e que componentes serão atualizados a partir da resposta, aumentando a interação do usuário com os sistemas web.

### Comunicação entre Navegador e Servidor

Jesse James Garrett, em seu artigo citado anteriormente (Ajax: Uma Nova Abordagem para Aplicações Web), descrevia sobre as possibilidades das interfaces web copiarem um pouco da interatividade e da riqueza das interfaces desktop. Talvez muitos leitores não se lembrem, mas antes do AJAX, a comunicação entre o navegador web e o servidor era, muitas vezes, irritante. Imagine por exemplo que, ao preencher um formulário em uma página web, você estivesse selecionando o seu país de origem em uma combobox. Ao selecioná-lo, outra combobox logo abaixo enumeraria os estados deste país. Ao selecionar o país, uma requisição seria submetida ao servidor e, dependendo da velocidade da rede e do tempo gasto no processamento desta requisição, o usuário ficaria olhando para uma tela congelada ou em branco. Após a resposta, o navegador receberia o retorno da requisição (coleção de estados do país selecionado) e renderizaria a tela novamente para que o usuário pudesse selecionar o estado e informar os demais dados. Havia muito interage-para-interage-para.

**Com AJAX, a requisição poderia ser submetida ao servidor de forma assíncrona**, o usuário poderia continuar visualizando a tela e/ou interagindo com ela, e, ao obter a resposta, o navegador renderizaria apenas os componentes que deveriam ser atualizados, que no nosso exemplo, seria a combobox dos estados de um país. Veja na **Figura 1** uma ilustração desta comunicação.

Embora o termo AJAX (Asynchronous JavaScript and XML) contenha o termo Assíncrono em sua definição, pode-se escolher se a requisição ao servidor será assíncrona ou síncrona. No método open() do objeto **XMLHttpRequest**, o último parâmetro booleano determina como será a chamada: **true** para assíncrona, e **false** para síncrona.

![Aplicações web tradicionais versus aplicações com AJAX](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image001.gif)**Figura 1**. Aplicações web tradicionais versus aplicações com AJAX (fonte: Jesse James Garret / adaptivepath.com).

Na **Figura 1**, no lado esquerdo, está a representação de como funciona a **comunicação com um servidor web sem AJAX**. Ao interagir com algum componente que requeira atualização de dados, uma requisição HTTP é enviada e uma resposta envia a página inteira no formato [HTML](https://www.devmedia.com.br/html-basico-codigos-html/16596) e CSS para atualizar toda a tela do navegador. Com AJAX, no lado direito da **Figura 1**, ao interagir com o componente, uma requisição é enviada a um recurso específico via Javascript, os dados, [em XML](https://www.devmedia.com.br/xml-tutorial/24936) ou outro formato, são retornados e atualizam apenas os componentes, ou a parte da tela, que deve ser atualizada.

Na **Figura 2**, é possível verificar que, na interação do usuário com o navegador web, há várias interrupções na linha do tempo, que representam os momentos em que o usuário fica aguardando. Na parte de baixo da mesma figura, representando a interação com AJAX, é possível ver que a interação é contínua, isto é, não há interrupções.

![adrão de interação síncrona tradicional versus a assíncrona do AJAX](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image002.gif)**Figura 2**. Padrão de interação síncrona tradicional versus a assíncrona do AJAX (fonte: Jesse James Garret / adaptivepath.com).

O importante a compreender até o momento é que AJAX é uma nova abordagem para [desenvolvimento de aplicações web](https://www.devmedia.com.br/introducao-ao-desenvolvimento-de-aplicacoes-web/29798). E que esta nova abordagem está embutida em muitos frameworks atuais. Neste artigo, veremos um exemplo [utilizando JSF 2](https://www.devmedia.com.br/jsf-2-introducao/23678).

### Preparando o ambiente

Neste projeto estamos utilizando o [Facelets](https://www.devmedia.com.br/introducao-ao-facelets/5332), a linguagem de representação gráfica oficial do JSF 2, que é baseada em XHTML, o Eclipse Indigo como IDE e o GlassFish 3.1.1 como servidor de aplicação. Nos parágrafos seguintes, veremos como configurar corretamente o nosso ambiente.

### Instalando o GlassFish

O servidor de [aplicações GlassFish](https://www.devmedia.com.br/novidades-do-glassfish-3-1-artigo-java-magazine-91/21124) foi o primeiro a implementar as especificações do [Java EE 6](https://www.devmedia.com.br/introducao-java-ee-6/21364), como JPA 2.0, Servlets 3.0, EJB 3.1, dentre outras especificações do Java Enterprise. Este servidor possui uma versão que é instalada como plugin do [Eclipse](https://www.devmedia.com.br/conhecendo-o-eclipse-uma-apresentacao-detalhada-da-ide/25589) e há uma versão independente de IDE para instalação. Utilizando esta segunda, é possível estar mais à vontade para utilizá-lo com aplicações desenvolvidas em qualquer IDE, inclusive baixar outras aplicações e testá-las ou usá-las sem restrição de ambiente de desenvolvimento. Portanto, é com ela que trabalharemos neste artigo.

É possível baixar esta versão do GlassFish a partir da URL: http://glassfish.java.net/downloads/3.1.1-final.html. Neste endereço pode-se verificar duas versões disponíveis: a de código aberto e a comercial. O link indicado já direciona para a primeira opção. A distribuição utilizada neste artigo foi a Full Platform, em formato executável para Windows. Dito isso, inicie a instalação e, quando solicitado sobre o tipo da mesma, selecione a opção “Instalação Típica”. Siga confirmando as opções padrão até finalizar a instalação.

Para testar a instalação ao concluir, abra um prompt de comando, acesse a pasta de instalação do GlassFish, entre na pasta bin e digite asadmin start-domain. Este comando iniciará o servidor. Após isto, abra o seu navegador web e digite http://localhost:8080 para verificar se o servidor foi iniciado corretamente. Aparecerá uma tela com a mensagem Your server is now running (seu servidor está em execução). Para pará-lo, na mesma janela do prompt de comando, digite asadmin stop-domain.

Além da linha de comando, também é possível iniciar e parar o servidor a partir do Eclipse, mas para isso é necessário configurá-lo na view Servers. Deste modo, navegue no menu Window | Show View > Servers, clique com o botão direito do mouse e em seguida escolha New > Server. Na tela New Server, selecione o servidor desejado, que no nosso caso é o Glassfish Server Open Source Edition 3. Ao lado da combobox Server Runtime Environment, há um link Add..., como indicado na **Figura 3**. Ao clicar neste link, a tela New Server Runtime Environment será aberta, onde, no campo Application Server Directory, você indicará o local da instalação do Glassfish Server.

![Tela para configuração do servidor de aplicação](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image003.jpg)**Figura 3**. Tela para configuração do servidor de aplicação.

Após estes passos o servidor GlassFish estará disponível através da view Servers do Eclipse. Para iniciá-lo ou pará-lo, basta clicar com o botão direito em cima de seu nome e selecionar as opções Start ou Stop do menu que aparece, ou ainda pressionar os botões disponíveis na view. A partir deste momento estamos prontos para iniciar o nosso projeto.

### O projeto: consultando livros com mais responsividade

O nosso projeto tem como objetivo ilustrar o uso das funcionalidades AJAX do JSF 2. Trata-se de um sistema para cadastro e consulta de livros, onde, na opção de cadastro, o usuário informa os dados de um exemplar como título, autor, editora e ISBN e o armazena. Esta opção está presente apenas para podermos ter livros para consultar. Já na opção de pesquisa, há os mesmos campos para servir de filtro da consulta, mais uma tabela que nos mostra uma lista de livros filtrados a partir dos dados informados. Também há o botão para pesquisar que, ao ser pressionado, envia uma requisição AJAX para o servidor que devolve uma lista de livros. Lembre-se, esta requisição ao servidor (podendo ser síncrona ou assíncrona) é diferente de uma requisição convencional que submete a página inteira. Os dados retornados atualizam apenas a lista de livros, sem ter que redesenhar a tela inteira.

Para criarmos nosso projeto, no Eclipse, clique em File | New > Dynamic Web Project. No campo Project Name, informe “Livraria”. No campo Target Runtime, selecione a instalação do GlassFish que instalamos antes, ou seja, GlassFish Server Open Source Edition 3. Na área Configurarion, clique no botão Modify, e na tela Project Facets, marque a opção JavaServer Faces. Em seguida, verifique se a versão desta opção está com 2.0, como indica a **Figura 4**. Clique em OK e depois em Next.

![Habilitando o JavaServer Faces no projeto](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image004.jpg)**Figura 4**. Habilitando o JavaServer Faces no projeto.

![Tela de Web Module](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image005.jpg)**Figura 5**. Tela de Web Module, indicando a criação do web.xml.

Na próxima tela de configuração, a do Build Path, apenas clique em Next novamente. Na tela seguinte, Web Module, marque a opção Generate web.xml deployment descriptor, como indicado na **Figura 5**, e clique em Next. A tela seguinte é a de JSF Capabilities. Nela, certifique-se de que os valores estão como indicados na **Figura 6**. Ao clicar em Finish, nosso projeto estará criado.

![Tela de configuração do Servlet do JavaServer Faces](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image006.jpg)**Figura 6**. Tela de configuração do Servlet do JavaServer Faces.

Ao abrir o arquivo web.xml, é possível verificar que ele contém a declaração do Servlet do JavaServer Faces necessário à execução de um projeto com esta tecnologia. A partir de agora, estamos prontos para iniciar a parte de implementação da nossa aplicação.

Vamos iniciar com o código da classe Livro, exposto na **Listagem 1**. Como dito antes, esta classe contém os atributos **titulo**, **autor**, **editora** e **isbn** de um livro. É a partir dela que criaremos o nosso CRUD (Create, Retrieve, Update e Delete).

```
public class Livro implements Serializable{

 private Long id;
 private String titulo;
 private String autor;
 private String editora;
 private String isbn;

 public Livro(){}
 // Getters e Setters omitidos
}
```

**Listagem 1**. Código da classe de domínio Livro

Representando a camada de negócios de nossa aplicação, criamos a classe mostrada na **Listagem 2**, AplCadastroLivros. Esta classe proverá os métodos necessários às operações da classe controladora, mostrada na **Listagem 3**, que discutiremos em seguida.

```
public class AplCadastroLivros {

  private List<Livro> listaLivros = new ArrayList<Livro>();
  private List<Livro> listaLivrosFiltrados = new ArrayList<Livro>();

  public AplCadastroLivros() { }

  public void limparListaLivrosFiltrados() {
    this.listaLivrosFiltrados.clear();
  }

  public void cadastrarLivro(Livro livro) {
    listaLivros.add(livro);
  }

  public boolean salvarLivro(Livro livroParaAtualizar) {
    boolean atualizado = false;
    if (listaLivros.contains(livroParaAtualizar)) {
      for (Livro livroPersistido : listaLivros) {
        if (livroPersistido.equals(livroParaAtualizar)) {
          livroPersistido = livroParaAtualizar;
          atualizado = true;
          break;
        }
        else
          atualizado = false;
      }
    }
    else
      atualizado = false;
    return atualizado;
  }

  public boolean excluirLivro(Livro livroParaExcluir) {
    boolean excuido = false;
    if (listaLivros.contains(livroParaExcluir)) {
      listaLivros.remove(livroParaExcluir);
      excuido = true;
    }
    else
      excuido = false;
    return excuido;
  }

  public void filtrarLivro(Livro livroASerPesquisado) {
    listaLivrosFiltrados.clear();
    if (!livroASerPesquisado.getTitulo().equals("")) {
      for (Livro livro : listaLivros) {
        if (livro.getTitulo().contains(livroASerPesquisado.getTitulo())) {
          listaLivrosFiltrados.add(livro);
        }
      }
    }
  }
}
```

**Listagem 2**. Código da classe de negócio AplCadastroLivros

Além de nossas classes básicas, em um projeto com JSF 2, é possível interagir com classes que são chamadas de Beans Gerenciados, ou seja, classes controladoras que podem ser referenciadas diretamente a partir das páginas web através de EL (Expression Language). Neste caso, a nossa classe será a CadastroBean, exibida na **Listagem 3**.

```
@ManagedBean
@SessionScoped
public class CadastroBean {

 private Livro livro = new Livro();
 private AplCadastroLivros aplCadastroLivros = new AplCadastroLivros();
 private boolean editar;

 public void cadastrarLivro() {
  aplCadastroLivros.cadastrarLivro(livro);
  this.livro = new Livro();
 }

 public void salvarLivro() {
  aplCadastroLivros.salvarLivro(livro);
  editar = false;
  aplCadastroLivros.limparListaLivrosFiltrados();
  this.livro = new Livro();
 }

 public void editarLivro(Livro livroAEditar) {
  this.livro = livroAEditar;
  editar = true;
 }

 public void excluirLivro(Livro livroAExcluir) {
  boolean retorno = aplCadastroLivros.excluirLivro(livroAExcluir);
 }

 public void filtrarLivros() {
  aplCadastroLivros.filtrarLivro(livro);
 }

 public List<Livro> getListaLivros() {
  return aplCadastroLivros.getListaLivros();
 }

 public void setListaLivros(List<Livro> listaLivros) {
  aplCadastroLivros.setListaLivros(listaLivros);
 }

 public List<Livro> getListaLivrosFiltrados() {
  return aplCadastroLivros.getListaLivrosFiltrados();
 }

 public void setListaLivrosFiltrados(List<Livro> listaLivrosFiltrados) {
  aplCadastroLivros.setListaLivrosFiltrados(listaLivrosFiltrados);
 }

}
```

**Listagem 3**. Classe CadastroBean para o cadastro de livros

Observe algumas anotações especiais, como @ManagedBean e @SessionScoped. A primeira define que a classe CadastroBean será um Bean Gerenciado. A segunda define que nossa classe terá um escopo de sessão, que significa que para cada sessão de uso de nossa aplicação, ou seja, para cada cliente diferente, haverá uma instância desta classe. Assim, se dois navegadores forem abertos acessando a aplicação, serão duas sessões diferentes, e por consequência, duas instâncias de CadastroBean também diferentes.

A **Listagem 4** mostra como os Beans Gerenciados podem ser acessados a partir das nossas páginas. Nela, estamos definindo nossa tela de cadastro de livros.

```
<?xml version="1.0" encoding="ISO-8859-1" ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:h="http://java.sun.com/jsf/html"
  xmlns:f="http://java.sun.com/jsf/core">
<h:head>
  <meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1" />
  <title>Cadastro de Livros</title>
</h:head>
<h:body>
  <h:link outcome="pesquisa" value="Pesquisar Livros" />
  <h1><h:outputText value="Cadastrar Livros" /></h1>
  <h:form id="form-livro">
    <h:panelGrid columns="2">
      <h:outputText value="Título"/>
      <h:inputText id="titulo" value="#{cadastroBean.livro.titulo}"/>
      <h:outputText value="Autor"/>
      <h:inputText id="autor" value="#{cadastroBean.livro.autor}"/>
      <h:outputText value="Editora"/>
      <h:inputText id="editora" value="#{cadastroBean.livro.editora}"/>
      <h:outputText value="ISBN"/>
      <h:inputText id="isbn" value="#{cadastroBean.livro.isbn}"/>
    </h:panelGrid>
    <h:panelGrid columns="1">
      <h:commandButton id="cadastrar"
          rendered="#{!cadastroBean.editar}" value="Cadastrar" >
        <f:ajax render=":form-livro" execute=":form-livro"
          listener="#{cadastroBean.cadastrarLivro()}"/>
      </h:commandButton>
      <h:commandButton id="editar"
          rendered="#{cadastroBean.editar}" value="Salvar" >
        <f:ajax render=":form-livro" execute=":form-livro"
          listener="#{cadastroBean.salvarLivro()}"/>
      </h:commandButton>
    </h:panelGrid>
    <h:panelGrid columns="1">
      <h:panelGroup id="tabelaDosLivros">
        <h:dataTable value="#{cadastroBean.listaLivros}" var="item">
          <h:column>
            <f:facet name="header">Titulo</f:facet>
            <h:outputText value="#{item.titulo}" />
          </h:column>
          <h:column>
            <f:facet name="header">Autor</f:facet>
            <h:outputText value="#{item.autor}" />
          </h:column>
          <h:column>
            <f:facet name="header">Editora</f:facet>
            <h:outputText value="#{item.editora}" />
          </h:column>
          <h:column>
            <f:facet name="header">ISBN</f:facet>
            <h:outputText value="#{item.isbn}" />
          </h:column>
          <h:column>
            <f:facet name="header">Editar</f:facet>
            <h:commandLink id="editar" value="Editar">
              <f:ajax render=":form-livro"
                listener="#{cadastroBean.editarLivro(item)}"/>
            </h:commandLink>
          </h:column>
          <h:column>
            <f:facet name="header">Excluir</f:facet>
            <h:commandLink id="excluir" value="Excluir">
              <f:ajax render=":form-livro:tabelaDosLivros"
                listener="#{cadastroBean.excluirLivro(item)}"/>
            </h:commandLink>
          </h:column>
        </h:dataTable>
      </h:panelGroup>
    </h:panelGrid>
  </h:form>
</h:body>
</html>
</html>
```

**Listagem 4**. Página cadastro.xhtml para cadastro de livros

Como dito na seção **“O que é AJAX”**, o código da **Listagem 4** está em XHTML. Observe que há um cabeçalho como o de qualquer arquivo XML. Observe também que na tag <html> definimos os namespaces (espaços de nomes), que permitem que usemos elementos que representem componentes JSF, através dos atributos xmlns, xmlns:h e xmlns:f. Tais namespaces apontam para as bibliotecas de tags do JSF. Iniciamos a implementação do código da página a partir das tags <h:head>, <h:body> e <h:form>, que são equivalentes a <head>, <body> e <form> do HTML puro.

Na página de cadastro, definimos os nossos controles dentro do form, iniciando com a tag <h:panelGrid> com o atributo columns com valor 2. Isto permite que a nossa tela tenha duas colunas, de forma que os nomes dos campos fiquem do lado esquerdo e os campos propriamente ditos fiquem do lado direito. <h:outputText> é a tag para se exibir textos, enquanto <h:inputText> é a tag equivalente ao <input type=”text”> do HTML.

Nos dois primeiros botões exibidos na **Listagem 4** (cujos identificadores são cadastrar e editar), há o atributo rendered, que determina se os mesmos serão ou não renderizados pelo navegador. A condição para a renderização é o atributo booleano editar de nosso bean gerenciado. Como seu valor inicial é falso, a expressão !cadastroBean.editar utilizada no atributo rendered, cujo sinal “!” indica negação, é avaliada como verdadeira. Desta forma, o botão cadastrar será renderizado e o botão editar não. Obviamente, se o valor do atributo editar mudar para true, o botão editar será renderizado, enquanto que o cadastrar não. Portanto, apenas um dos dois será mostrado, adequando o formulário para inclusão e edição de livros.

Ainda na nossa tela de cadastro, há uma tabela mostrando uma lista com os livros já inseridos. A novidade entre as tags aqui fica por conta de <h:dataTable> e suas tags filhas <h:column> e <f:facet>. Com a primeira, estamos criando uma tabela e mostrando os livros da coleção listaLivros do bean gerenciado CadastroBean, indicado no atributo value de nossa tag. O atributo var determina que cada elemento da coleção será referenciado pelo nome item, e os atributos de cada um desses itens serão acessados usando item.titulo, item.autor, item.editora e item.isbn. Com a segunda (<h:column>), definimos as colunas de nossa tabela. E com a terceira tag (<f:facet>), definimos os cabeçalhos das colunas.

Até aqui, implementamos os passos para o nosso cadastro de livros. Nossa aplicação também possui uma tela separada para pesquisa. Poderíamos ter várias outras telas, mas estas duas são suficientes para mostrarmos os recursos de AJAX e sua tag <f:ajax>, sobre a qual falaremos mais adiante. A tela de pesquisa pode ser vista na **Listagem 5**.

```
<?xml version="1.0" encoding="ISO-8859-1" ?>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xmlns:h="http://java.sun.com/jsf/html"
 xmlns:f="http://java.sun.com/jsf/core">
<h:head>
  <meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1" />
  <title>Pesquisa de Livros</title>
</h:head>
<h:body>
  <h:link outcome="cadastro" value="Cadastrar Livros" />
  <h1><h:outputText value="Pesquisar Livros" /></h1>
  <h:form id="form-livro">
    <h:panelGrid columns="2">
      <h:outputText value="Título"/>
      <h:inputText id="titulo" value="#{cadastroBean.livro.titulo}">
        <f:ajax event="keyup" render=":form-livro:tabelaDosLivros"
            listener="#{cadastroBean.filtrarLivros}"
            execute="titulo" immediate="false"/>
      </h:inputText>
      <h:panelGroup id="tabelaDosLivros">
        <h:dataTable value="#{cadastroBean.listaLivrosFiltrados}"
            var="item">
          <h:column>
            <f:facet name="header">Autor</f:facet>
            <h:outputText value="#{item.autor}" />
          </h:column>
          <h:column>
            <f:facet name="header">Titulo</f:facet>
            <h:outputText value="#{item.titulo}" />
          </h:column>
          <h:column>
            <f:facet name="header">Editora</f:facet>
            <h:outputText value="#{item.editora}" />
          </h:column>
        </h:dataTable>
      </h:panelGroup>
    </h:panelGrid>
  </h:form>
</h:body>
</html>
```

**Listagem 5**. Página pesquisa.xhtml, para pesquisar na lista de livros

Para pesquisar um livro em nossa aplicação, basta que o usuário digite alguns caracteres no campo Titulo. Feito isso, a tabela logo abaixo deste campo será preenchida automaticamente, via requisição AJAX, com uma lista de livros cujo título corresponde aos caracteres digitados, como mostra a **Figura 8**.

### Onde está o AJAX?

O AJAX fica por conta da tag <f:ajax>, dentro das tags <h:commandButton> e <h:commandLink>, como mostrado na **Listagem 4**, e dentro da tag <h:inputText>, como mostrado na **Listagem 5**. Sempre que adicionamos a tag do AJAX dentro de alguma tag de componente, significa que uma requisição AJAX será realizada a partir de algum evento gerado pelo componente. No caso da **Listagem 4**, temos a tag do AJAX dentro das tags dos botões cujos identificadores são cadastrar e editar.

A **sintaxe do AJAX** no primeiro exemplo da **Listagem 4** é <f:ajax render=":form-livro" execute=":form-livro" listener="#{cadastroBean.cadastrarLivro()}"/>, onde o atributo render contém o identificador do componente visual que será atualizado após a resposta da requisição AJAX (sem precisar atualizar a página inteira) e o atributo execute contém o identificador de um ou mais componentes visuais cujos valores serão submetidos junto com a requisição, como parâmetros da mesma. Tanto no render quanto no execute, o valor é o formulário form-livro inteiro. O atributo listener contém o nome do método que é chamado na requisição AJAX, no caso o método cadastrarLivro() do nosso bean gerenciado CadastroBean.

Ainda na **Listagem 4**, observe a tag <f:ajax> em duas colunas de nossa tabela, “editar” e “excluir”. Nestes casos, elas estão dentro da tag <h:commandLink> e iniciarão requisições AJAX quando os links forem clicados. No link para edição, o atributo render contém o identificador do formulário inteiro porque todos os campos do mesmo devem ser atualizados. O atributo listener indica que o método a ser chamado será o editarLivro(item), passando o objeto da linha atual da tabela. No caso, item é um objeto da classe Livro. No bean gerenciado, o **método chamado pelo AJAX** recebe este objeto item, estabelece que ele será a instância atual do atributo livro e determina que o valor do atributo editar será true. Desta forma, quando a requisição AJAX concluir sua execução e atualizar o form-livro, os campos do formulário estarão exibindo os atributos do objeto livro e o botão salvar será renderizado. Ao alterar os valores dos campos e clicar em “Salvar”, o objeto livro será atualizado e o atributo editar receberá false, o que fará com que o botão cadastrar seja renderizado agora e o botão editar desapareça. Por último, a tabela será atualizada mostrando a linha do livro editado com os valores atualizados.

Já no link para exclusão, apenas a tabela tabelaDosLivros é indicada no atributo render da tag <f:ajax>, pois apenas ela será atualizada após o retorno do resultado da requisição AJAX. O atributo listener indica que o método a ser chamado no bean gerenciado será o excluirLivro(item), quando o link “excluir” for clicado. Daí, o método excluirá o item recebido e, quando a tabela for renderizada, não mais exibirá o livro excluído.

Na nossa página de pesquisa, mostrada na **Listagem 5**, a tag <f:ajax> está dentro da tag <h:inputText>. O recurso chamado, como indicado no atributo listener, é o método filtrarLivros() de nosso bean gerenciado CadastroBean. O evento que dispara a requisição AJAX é o keyup, lançado quando soltamos uma tecla pressionada, indicado no atributo event da tag <f:ajax>. Este atributo (event) deve ser utilizado sempre que desejarmos que um evento, que não seja o padrão de um componente, inicie a chamada AJAX.

Os valores para o atributo event são alguns eventos já conhecidos, como: blur, change, keydown, keypress, action, etc. Enquanto os atributos execute e render recebem os identificadores dos componentes que são, no caso do primeiro, enviados para a **requisição AJAX** e que serão, no caso do segundo, atualizados na tela, também é possível utilizar algumas notações especiais para representar tais componentes, como:

- @all: Representando todos os componentes da página;
- @none: Nenhum componente será renderizado. É a opção default;
- @this: Representa o próprio componente que contém a tag <f:ajax>;
- @form: Representa todos os identificadores dos componentes do formulário no qual a tag <f:ajax> está contida.

![Tela de cadastro de livros](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image007.jpg)**Figura 7**. Tela de cadastro de livros.

![Tela de pesquisa de livros](https://arquivo.devmedia.com.br/REVISTAS/easyjava/imagens/19/3/image008.gif)**Figura 8**. Tela de pesquisa de livros.

A partir deste momento, podemos executar nossa aplicação para cadastro de livros. As **Figuras 7** e **8** ilustram como ficariam nossas telas. No momento da pesquisa dos livros já cadastrados, veremos que a lista dos mesmos é atualizada a cada pesquisa que fazemos sem que a página fique, nem por um instante, toda em branco ou travada sem possibilidade de interação.

#### Conclusões

Neste artigo, aprendemos sobre o que é o AJAX, seus fundamentos, sua história e a definição das ideias iniciais. O conceito por traz do AJAX é o de comunicação assíncrona (ou até síncrona) com o servidor, a partir de um objeto Javascript, no cliente. Abordamos um pouco de suas tecnologias constituintes, como XHTML, CSS, DOM e Javascript, e traçamos uma comparação de interação/navegação do usuário com e sem as tecnologias do AJAX.

Com o lançamento do Java EE 6, a especificação do JSF 2 agora possui **suporte nativo ao AJAX**, o que antes requeria frameworks de terceiros e tornava a **utilização do AJAX** complexa e às vezes incompatível com as bibliotecas empregadas em uma aplicação. Neste artigo, criamos um projeto para exemplificar o **uso do AJAX** exibindo a grande novidade que é a tag <f:ajax/>.

Assim, esperamos ter demonstrado de forma clara e didática os fundamentos do AJAX, como utilizá-lo e, principalmente, ter mostrado que ao se adotar AJAX o grande objetivo é uma interação mais responsiva e dinâmica com o usuário de sistemas web.

------

#### Links Úteis

- [Modelagem de dados: 1:N ou N:N?](http://www.devmedia.com.br/modelagem-de-dados-1-n-ou-n-n/38894): Você sabe quando usar um relacionamento do tipo 1:N ou N:N? Optar pelo tipo incorreto pode impactar diretamente no negócio.
- [Como criar minha primeira classe em PHP](http://www.devmedia.com.br/como-criar-minha-primeira-classe-em-php/38895): Neste conteúdo você aprenderá a criar sua primeira classe na linguagem PHP. Aprenda também a usar herança e interfaces, bem como métodos, atributos e propriedades.
- [Curso de Vue.js: Como criar sua primeira aplicação](http://www.devmedia.com.br/curso/curso-de-vue-js-como-criar-sua-primeira-aplicacao/2071): Neste curso você aprenderá a criar sua primeira aplicação com Vue.js, um dos principais frameworks JavaScript do mercado atualmente.

------

#### Saiba mais sobre AJAX ;)

- [Adoramos Ajax](http://www.devmedia.com.br/adoramos-ajax/37919): Neste DevCast veremos como a equipe de programação da DevMedia utilizou a técnica de Lazy Load, com jQuery, para otimizar o tempo de carregamento da página por meio de requisições Ajax.
- [Dominando Ajax com jQuery](http://www.devmedia.com.br/curso/dominando-ajax-com-jquery/1471): Neste curso vamos aprender como utilizar a função Ajax da biblioteca jQuery para realizar requisições a uma Web API RESTful.
- [JavaServer Faces: Como interceptar requisições Ajax](http://www.devmedia.com.br/javaserver-faces-como-interceptar-requisicoes-ajax/37487): Veja neste artigo como interceptar, no JavaServer Faces (JSF), uma requisição Ajax criada pelos seus próprios componentes.

**Links**:

- [Link do artigo de Jesse James Garrett que estabeleceu o termo AJAX](http://www.adaptivepath.com/ideas/ajax-new-approach-web-applications).
- [Artigo introdutório sobre AJAX](http://www.wrox.com/WileyCDA/Section/What-is-Ajax-.id-303217.html).
- [Site com vários pequenos tutoriais sobre as tecnologias envolvidas pelo AJAX](http://www.w3schools.com/).
- [Especificação do JSF 2 com capítulo sobre AJAX](http://www.jcp.org/en/jsr/detail?id=314).

Tecnologias: 

- Ajax
-  

- [CSS](https://www.devmedia.com.br/css/)
-  

- [HTML](https://www.devmedia.com.br/html/)
-  

- [Java](https://www.devmedia.com.br/java/)
-  

- [JavaScript](https://www.devmedia.com.br/javascript/)

[Saiba mais](https://www.devmedia.com.br/pro/)

![autor](https://www.devmedia.com.br/imagens/fotoscolunistas/image017-4.jpg)

Por [João](https://www.devmedia.com.br/perfil/joao-dos-prazeres-farias)Em 2012

##### RECEBA NOSSAS NOVIDADES

Receber Newsletter

Suporte ao aluno[Minhas dúvidas](https://www.devmedia.com.br/notificacoes/?suporte)

![img](https://www.devmedia.com.br/imagens/fotoscolunistas/avatar/avatar-4.png)

