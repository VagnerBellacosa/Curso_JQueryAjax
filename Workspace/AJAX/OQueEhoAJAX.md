# O que é o AJAX

## AJAX, acrônimo de Asynchronous JavaScript and XML, é uma técnica de desenvolvimento Web que permite a criação de aplicações mais interativas.



[Artigos](https://www.devmedia.com.br/artigos/)[JavaScript](https://www.devmedia.com.br/artigos/javascript)O que é o AJAX

##### Guia do artigo:

- [O que é AJAX?](https://www.devmedia.com.br/o-que-e-o-ajax/6702#1)
- [Tecnologias usadas no AJAX](https://www.devmedia.com.br/o-que-e-o-ajax/6702#2)
- [Histórico do AJAX](https://www.devmedia.com.br/o-que-e-o-ajax/6702#3)
- [Web 2.0](https://www.devmedia.com.br/o-que-e-o-ajax/6702#4)
- [O que é o W3C?](https://www.devmedia.com.br/o-que-e-o-ajax/6702#5)
- [JavaScript](https://www.devmedia.com.br/o-que-e-o-ajax/6702#6)
- [Objeto XMLHttpRequest](https://www.devmedia.com.br/o-que-e-o-ajax/6702#7)
- [DOM](https://www.devmedia.com.br/o-que-e-o-ajax/6702#8)
- [JSON](https://www.devmedia.com.br/o-que-e-o-ajax/6702#9)
- [O que é o ASP.NET AJAX 1.0?](https://www.devmedia.com.br/o-que-e-o-ajax/6702#10)
- [Front-end e JavaScript](https://www.devmedia.com.br/o-que-e-o-ajax/6702#11)
- [Cursos de JavaScript](https://www.devmedia.com.br/o-que-e-o-ajax/6702#12)
- [Curso de Introdução ao JavaScript](https://www.devmedia.com.br/o-que-e-o-ajax/6702#13)

### O que é AJAX?

**AJAX, acrônimo de Asynchronous JavaScript and XML, é uma técnica de desenvolvimento Web que permite a criação de aplicações mais interativas**. Um dos principais objetivos é tornar as respostas das páginas Web mais rápidas pela troca de pequenas quantidades de informações com o servidor Web, nos bastidores.

Além disso, evita-se que a página Web inteira tenha que ser recarregada cada vez que alguma nova informação precisa ser consultada no servidor. Em geral, isso significa que páginas Web com **recursos AJAX** permitem maior interatividade, velocidade de processamento e usabilidade.

Este é o primeiro de uma série de artigos sobre ASP.NET AJAX. O objetivo deste primeiro artigo é apresentar os bastidores do AJAX, independente do framework ASP.NET AJAX da Microsoft.

A idéia é fornecer uma base consistente de como trabalhar com **várias das tecnologias usadas no AJAX** para desenvolver uma infra-estrutura que permita criar aplicações Web mais interativas.

Para um bom entendimento deste artigo, é ideal que o leitor tenha um nível de conhecimento de básico a intermediário em HTML/XHTML, [CSS](https://www.devmedia.com.br/guia/css/38149), XML, ASP.NET 2.0 e C# 2.0 (ou Visual Basic 2005) e um nível de intermediário a avançado em [JavaScript](https://www.devmedia.com.br/guia/javascript/34372) e DOM.

Os artigos posteriores estarão focados nas funcionalidades do framework gratuito ASP.NET AJAX, que foi disponibilizado pela Microsoft como uma extensão ao ASP.NET 2.0. Os leitores que entenderem os conceitos apresentados neste artigo, terão um domínio maior sobre o que acontece nos bastidores do framework ASP.NET AJAX, como em qualquer outro **framework AJAX**.

<iframe src="https://www.youtube.com/embed/UqzQwR-L-OQ?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Esse conhecimento é muito importante para um maior domínio do assunto, principalmente para aqueles desenvolvedores Web que pretendem criar componentes não visuais do lado do cliente ou controles ASP.NET AJAX personalizados.

### Tecnologias usadas no AJAX

AJAX utiliza uma combinação de várias tecnologias padronizadas e não padronizadas de desenvolvimento para Web, conforme apresentado a seguir:

- [HTML (HyperText Markup Language)](https://www.devmedia.com.br/guia/html/38051)/XHTML (Extensible HyperText Markup Language): linguagem para criação de documentos Web;
- CSS (Cascade Style Sheets): mecanismo para adicionar estilos aos documentos Web;
- XML (Extensible Markup Language): formato que permite a criação de documentos estruturados com dados hierárquicos, sendo muito usado para troca de dados na Web;
- ECMAScript: padrão de linguagem de script, cujas principais implementações são o JavaScript e o JScript;
- XMLHttpRequest: objeto que define uma API com funcionalidades para scripts do lado do cliente para comunicação entre um cliente e um servidor usando o protocolo HTTP;
- DOM (Document Object Model) para manipular a estrutura e o estilo de documentos Web dinamicamente;
- [JSON](https://www.devmedia.com.br/o-que-e-json/23166) (JavaScript Object Notation): formato leve para intercâmbio de dados;
- XSLT (Extensible Stylesheet Language for Transformation): linguagem para transformação de documentos XML;
- Dentre outras tecnologias possíveis de serem utilizadas.

Todas as tecnologias citadas anteriormente, com exceção de XSLT, serão descritas em maiores detalhes e utilizadas para construir um exemplo prático completo.

Será apresentado um breve histórico do AJAX, uma explicação do termo Web 2.0, que tem sido muito utilizado atualmente e uma descrição da aplicação Web de exemplo a ser desenvolvida.

### Um breve histórico do AJAX

Assim como DHTML (Dynamic HyperText Markup Language) e SPA (Single Page Application), o AJAX não é uma tecnologia, mas sim um termo que representa o uso de um grupo de tecnologias de [desenvolvimento para Web](https://www.devmedia.com.br/programacao-web-por-onde-comecar/31953). Antes da introdução do termo AJAX, um grande número de páginas já utilizava recursos do DHTML. O DHTML corresponde a um grupo de tecnologias usadas em conjunto para a criação de sites interativos e animados pela combinação de HTML, JavaScript, CSS e DOM.

Apesar de usar um subconjunto das tecnologias utilizadas pelo AJAX, o DHTML afeta dinamicamente a aparência de uma página com [conteúdo HTML](https://www.devmedia.com.br/html-basico-codigos-html/16596) depois que ela foi completamente carregada e está sendo visualizada. Porém, sempre que há a necessidade de comunicação com o servidor Web, a página deve ser recarregada como um todo.

Uma das principais tecnologias nos bastidores do AJAX é o objeto XMLHttpRequest, que torna possível a característica mais atraente do AJAX: a sua natureza assíncrona. Esse objeto pode ser usado pelo [JavaScript](https://javascript.com.br/) para transferir XML e outros dados textuais de um servidor Web para uma página Web, usando o [protocolo HTTP](https://www.devmedia.com.br/exemplo/documentacao-protocolo-http/77) por meio do estabelecimento de um canal de comunicação independente entre páginas Web do lado do cliente e do lado do servidor.

Apesar de, anteriormente, alguns desenvolvedores terem utilizado frames ocultos ou elementos IFRAME para comunicar com o servidor nos bastidores de forma assíncrona, atualmente o XMLHttpRequest é mais amplamente utilizado por ser suportado pelos browsers mais modernos do mercado e por permitir um maior controle na comunicação entre o cliente e o servidor.

O termo AJAX foi introduzido recentemente para designar um conjunto de tecnologias que permitem tornar a interação de usuários com a interface de uma aplicação Web mais rica e produtiva.

Conforme foi citado anteriormente, o acrônimo AJAX significa Assyncronous JavaScript and XML. Ele foi introduzido por Jesse James Garrett, presidente e fundador da empresa Adaptive Path, no artigo “Ajax: A New Approach to Web Applications”, que foi publicado há pouco mais de 2 anos, em 18 de fevereiro de 2005.

O artigo não apresentou nenhuma técnica revolucionária de desenvolvimento para Web, mas introduziu um novo termo simples e representativo para um conjunto de tecnologias que já estavam sendo utilizadas.

Além disto, Garret explicou de forma clara e sucinta como essas tecnologias melhoravam a experiência dos usuários com aplicações Web, inclusive citando as seguintes aplicações pioneiras como exemplo: Google Suggest e Google Maps.

No final deste artigo são apresentados links para essas aplicações e para o texto que introduziu o termo AJAX.

### Web 2.0

O termo Web 2.0 não possui uma definição formal, mas é comumente usado para se referir a aplicações Web que encorajam interação social e contribuição coletiva para o bem comum. O termo também é usado para se referir a técnicas de programação Web que têm como principal objetivo fornecer uma interface rica e amigável. Atualmente, o conjunto dessas técnicas de programação Web tem sido comumente denominado AJAX.

#### Descrição da aplicação Web de demonstração

Durante a apresentação teórica do artigo, uma aplicação Web de demonstração será desenvolvida para ilustrar várias das tecnologias usadas no AJAX. A interface será desenvolvida com XHTML 1.1 e uso de CSS 2 para sua formatação.

ASP.NET 2.0 e ADO.NET 2.0, com a linguagem C# 2.0 (uma versão com a linguagem Visual Basic 2005 estará disponível para download), e outros recursos do .NET Framework 2.0 serão usados para consultar o SQL Server 2005 e construir respostas dinâmicas para o cliente.

A comunicação entre o browser e o servidor Web será estabelecida com uso do objeto XMLHttpRequest, sendo que os dados serão transportados nos formatos: XML e JSON. O JavaScript 1.5 será usado do lado do cliente nos bastidores, de modo a funcionar nos principais browsers atuais, com a função de estabelecer a comunicação com o servidor Web e atualizar a interface com os dados recebidos como resposta. A tecnologia DOM será usada nos códigos JavaScript do lado do cliente.

Com o objetivo de tornar o artigo acessível a um maior número de desenvolvedores da [plataforma .NET](https://www.devmedia.com.br/desenvolvimento-em-net/18468), na elaboração do exemplo serão utilizados somente softwares e recursos disponíveis gratuitamente. Porém, as versões comerciais também podem ser usadas.

- Browsers: Internet Explorer 5.0 ou superior, Firefox 1.0 ou superior, Opera 8.0 ou superior, Netscape 7.0 ou superior;
- Servidor de banco de dados: SQL Server 2005 Express Edition SP2;
- Banco de dados: AdventureWorks;
- IDE para desenvolvimento: Visual Web Developer 2005 Express Edition SP1.

Os endereços para baixar os softwares e o banco de dados estão colocados no final do artigo.

#### Criando o exemplo

No Visual Web Developer 2005 Express Edition SP1, crie um novo Web Site ASP.NET selecionado o menu (File>New Web Site). No quadro de diálogo New Web Site, em Template selecione ASP.NET Web Site, em Location selecione File System e uma localização para os arquivos do Web Site e em Language selecione Visual C#.

Apague o arquivo Default.aspx, juntamente com o arquivo Default.aspx.cs. Por uma questão de espaço, o artigo apresenta todo o código do lado do servidor somente na linguagem C# 2.0. Porém, a versão em Visual Basic 2005 ficará disponível para download, sendo que o Web Site desenvolvido em C# 2.0 estará na pasta AdvWorksAjaxWebCS e o desenvolvido em Visual Basic 2005 na pasta AdvWorksAjaxWebVB.

Antes de continuarmos o exemplo, vamos examinar mais alguns fundamentos importantes.

### O que é o W3C?

O [World Wide Web Consortium (W3C)](https://www.w3.org/), que foi fundado em 1994, é um consórcio internacional em que membros de organizações, equipes com dedicação em tempo integral e o público trabalham juntos para desenvolver padrões para a Web.

Atualmente, o W3C é composto por, aproximadamente, 450 membros. O consórcio conta com membros de algumas das principais empresas e organizações de TI do mundo, incluindo as desenvolvedoras dos principais browsers do mercado, empresas de telecomunicações, universidades etc.

Segue uma breve relação com alguns dos mais notórios membros: Adobe, AOL, Apple, Canon, Cisco, Fujitsu, Google, HP, IBM, Intel, Lexmark, Microsoft, Motorola, Mozilla, Nokia, Nortel, Oracle, RealNetworks, Samsung, Sun, Symbian, Toshiba, VeriSign, Xerox e Yahoo, dentre outros.

#### HTML 4.01 e XHTML 1.0/1.1

A especificação HTML (HyperText Markup Language) 4.01, recomendada pelo W3C assim como a maioria das demais vistas neste artigo, define a linguagem de marcação de hipertexto para publicação na rede de alcance mundial, a World Wide Web (WWW).

A especificação XHTML (Extensible HyperText Markup Language) 1.0 - Second Edition, corresponde a uma reformulação do HTML 4 como XML 1.0.

A especificação XHTML 1.1 corresponde a uma reformulação do XHTML 1.0 para dividir o XHTML em módulos. Atualmente, o W3C está trabalhando nas especificações XHTML 1.1 (Second Edition) e XHTML 2.0.

A interface da aplicação de demonstração será feita com XHTML 1.1. O layout da página será definido com recursos de CSS para posicionamento e formatação dos elementos, ao invés de utilizar tabelas HTML para esse fim. Essa técnica é denominada Tableless Layout.

Adicione uma página HTML ao Web Site nomeando-a “Pedidos.htm”. A Listagem 1 apresenta o código XHTML 1.1 da página Pedidos.htm.

**Listagem 1** Código XHTML 1.1 da página Pedidos.htm

```
<DOCTYPE html PUBLIC>
  <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="pt-BR">

    <head>
      <title>Adventure Works - Pedidos por empregado </title>
    </head>

    <body>
      <div class="quadroPrincipal">
        <div class="tituloPrincipal">Adventure Works - Pedidos por empregado </div>
        <div class="conteudoPrincipal">
          <div class="quadro">
            <div class="titulo">Filtragem dos pedidos  </div>
            <div class="conteudo">
              <div >Selecione o empregado responsável pelos pedidos:
                <br />
                <select id="selectEmpregados" class="larguraTotal">  </select>
              </div>
              <div>Selecione o mês e ano dos pedidos:  <span id="spanEmpregadoPedidos" class="info">  </span>
                <br />
                <select id="selectMesesAnosPedidos" class="larguraTotal">  </select>
              </div>
            </div>
          </div>
          <div class="quadro">
            <div class="titulo">Pedidos do mês   <span id="spanMesAnoPedidos" class="info"> </span>
            </div>
            <div class="conteudo" id="divMesAnoPedidos"> </div>
          </div>
        </div>
      </div>
      <div id="divMensagem"> </div>
    </body>

    </html>
```

A Figura 1 mostra o documento Pedidos.htm visualizado no browser Opera 9.10 sem a aplicação de CSS.

![Documento XHTML sem CSS apresentado no browser Opera 9.10](https://www.devmedia.com.br/Imagens/msdnmagazine1/edicoes/42/net42-rogerio-ajax_arquivos/image002.jpg)Documento XHTML sem CSS apresentado no browser Opera 9.10.

#### CSS 2

A especificação [CSS (Cascade Style Sheet)](https://www.devmedia.com.br/guia/css/38149) 2 é uma linguagem de folha de estilo que permite anexar estilos a documentos estruturados, como HTML e XML. CSS 2 simplifica a autoria e a manutenção de Web Sites pela separação dos estilos de apresentação do conteúdo dos documentos.

Quer mais sobre CSS? Confira este vídeo:

<iframe width="560" height="315" src="https://www.youtube.com/embed/hRoIcc6qlyM?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Atualmente, o W3C está trabalhando nas especificações CSS 2.1 e CSS 3. A interface da aplicação Web de demonstração, elaborada com XHTML 1.1, será formatada com CSS 2 utilizando a técnica Tableless Layout, descrita anteriormente.

Adicione uma folha de estilo CSS ao Web Site nomeando-a “Estilos.css” (item StyleSheet). A Listagem 2 apresenta o código CSS 2 do arquivo Estilos.css. O arquivo CSS contém estilos para formatação de elementos presentes na página XHTML Pedidos.htm e de outros que serão gerados dinamicamente, como tabelas de dados.

**Listagem 2.** Código CSS 2 do arquivo Estilos.css

```
body,
select {
  background-color: White;
  font-family: Verdana, Arial, Helvetica, Sans-Serif;
  font-size: 9pt;
}
select {
  border: solid 1px #00460A;
}
div#divMensagem {
  position: absolute;
  visibility: hidden;
  top: 100px;
  left: 50%;
  width: 500px;
  margin-left: -260px;
  z-index: 1;
  font-size: 11pt;
  text-align: center;
  padding: 20px 10px 20px 10px;
  border: solid 1px #8A6F28;
  background-color: #F9D52C;
  color: #8A6F28;
}
span.info {
  font-style: italic;
}
div.quadroPrincipal {
  border: solid 2px #00460A;
  background-color: #77B75D;
  padding: 1px;
  width: 560px;
  margin: auto;
}
div.tituloPrincipal {
  background-color: #00460A;
  color: White;
  font-size: 16pt;
  font-weight: bold;
  text-align: center;
  padding: 3px;
}
div.quadro {
  border: solid 1px #00460A;
  background-color: #D4E5CB;
  margin: 5px;
}
div.titulo {
  background-color: #00460A;
  color: White;
  font-size: 12pt;
  padding: 3px;
}
div.conteudo {
  padding: 10px;
}
.larguraTotal {
  width: 100%;
}
table.dados {
  border: solid 1px #00460A;
  border-collapse: collapse;
  width: 100%;
}
table.dados tr th,
table.dados tr td {
  border: solid 1px #00460A;
  padding: 3px;
}
table.dados tr th {
  background-color: #228A11;
  color: White;
}
table.dados tr.alt td {
  background-color: #B7D5AB;
}
```

A Listagem 3 apresenta a sintaxe do elemento que deve ser acrescentado ao cabeçalho da página Pedidos.htm para vinculá-la aos estilos definidos na folha de estilo CSS 2 do arquivo Estilos.css.

**Listagem 3.** Para vincular Pedidos.htm a Estilos.css

```
<head>
  <title>Adventure Works - Pedidos por empregado </title>
  <link href="Estilos.css" rel="stylesheet" type="text/css" />
</head>
```

A Figura 2 mostra o documento XHTML 1.1 Pedidos.htm visualizado no Firefox 2.0 com a aplicação da folha de estilo CSS 2 Estilos.css.

![Documento XHTML formatado com CSS apresentado no Firefox 2.0](https://www.devmedia.com.br/Imagens/msdnmagazine1/edicoes/42/net42-rogerio-ajax_arquivos/image004.jpg)Documento XHTML formatado com CSS apresentado no Firefox 2.0

Comparando as Figuras 1 e 2, pode-se notar o poder dos estilos CSS para formatar páginas Web.

#### XML 1.0

A especificação XML (Extensible Markup Language) 1.0 corresponde a um subconjunto da SGML (Standard Generalized Markup Language) usado para descrever uma classe de objetos de dados chamados documentos XML e descrever parcialmente o comportamento de programas de computador que os processa.

A especificação XML 1.0 (Fourth Edition) substitui a especificação XML 1.0, descrita anteriormente. A especificação XML 1.1 (Second Edition) corresponde a uma atualização da especificação XML 1.0 para não depender de versões específicas do Unicode, além de adicionar verificações de normalização e seguir regras Unicode de finalização de linha mais rigidamente.

A relação de empregados responsáveis por pedidos da empresa Adventure Works será montada a partir de uma consulta no banco de dados AdventureWorks num servidor SQL Server 2005. Sendo que o resultado da consulta será construído em formato XML 1.0 com os seguintes dados: código, primeiro nome, sobrenome do meio, sobrenome final e quantidade de pedidos atendidos por todos os empregados ativos que atenderam a pelo menos um pedido de cliente até a sua conclusão.

Adicione um arquivo de configuração Web.config ao Web Site e configure a string de conexão com o banco de dados, como apresentado na Listagem 4.

**Listagem 4.** Arquivo de configuração Web.config.

```
<xml version="1.0" ?>
  <configuration>
    <connectionStrings>
      <add name="cnAdventureWorks" connectionString="Data Source=localhost\SQLExpress;
        Initial Catalog=AdventureWorks;
        Integrated Security=True" providerName="System.Data.SqlClient" />
    </connectionStrings>
  </configuration>
```

A string de conexão considera que o servidor de banco de dados SQL Server 2005 Express Edition esteja instalado na instância SQLExpress da máquina local e que o banco de dados AdventureWorks esteja instalado nesse servidor. Se necessário, modifique a string de conexão para refletir a sua configuração.

Adicione um Web Form nomeando-o “Empregados.aspx” e selecionando a opção Place code in separate file. Apague todo o código HTML do arquivo Empregados.aspx, deixando somente a diretiva @Page. Codifique o arquivo Empregados.aspx.cs como apresentado na Listagem 5.

**Listagem 5.** Arquivo code-behind Empregados.aspx.cs

```
using System.Data.SqlClient;
using System.Text;
using System.Xml;
public partial class Empregados: System.Web.UI.Page {
  protected void Page_Load(object sender, EventArgs e) {
    Response.ContentType = "text/xml";
    XmlWriter xwEmpregadosPedidos = null;
    SqlConnection cnAdventureWorks = null;
    SqlDataReader drEmpregadosPedidos = null;
    try {
      xwEmpregadosPedidos = new XmlTextWriter(Response.OutputStream, Encoding.GetEncoding("ISO-8859-1"));
      cnAdventureWorks = new SqlConnection();
      cnAdventureWorks.ConnectionString = ConfigurationManager.ConnectionStrings["cnAdventureWorks"].ConnectionString;
      SqlCommand cmEmpregadosPedidos = new SqlCommand();
      cmEmpregadosPedidos.Connection = cnAdventureWorks;
      cmEmpregadosPedidos.CommandText = @"SELECT E.EmployeeID AS Codigo
          , C.FirstName AS PrimeiroNome
          , C.MiddleName AS SobrenomeMeio
          , C.LastName AS SobrenomeFinal
          , COUNT(*) AS QuantidadePedidos
        FROM Purchasing.PurchaseOrderHeader AS POH
          INNER JOIN HumanResources.Employee AS E
            ON POH.EmployeeID = E.EmployeeID
          INNER JOIN HumanResources.EmployeeDepartmentHistory AS EDH
            ON E.EmployeeID = EDH.EmployeeID
              AND EDH.EndDate IS NULL -- Empregado em atividade
          INNER JOIN Person.Contact AS C
            ON E.ContactID = C.ContactID
        WHERE POH.Status = 4 -- Pedido finalizado (Complete)
        GROUP BY E.EmployeeID
          , C.FirstName
          , C.MiddleName
          , C.LastName
        ORDER BY C.FirstName
          , C.MiddleName
          , C.LastName";
      cnAdventureWorks.Open();
      drEmpregadosPedidos = cmEmpregadosPedidos.ExecuteReader();
      xwEmpregadosPedidos.WriteStartDocument();
      xwEmpregadosPedidos.WriteStartElement("Empregados");
      while (drEmpregadosPedidos.Read()) {
        xwEmpregadosPedidos.WriteStartElement("Empregado");
        for (int campo = 0; campo < drEmpregadosPedidos.FieldCount; campo++) {
          xwEmpregadosPedidos.WriteElementString(drEmpregadosPedidos.GetName(campo), drEmpregadosPedidos[campo].ToString());
        }
        xwEmpregadosPedidos.WriteEndElement();
      }
      xwEmpregadosPedidos.WriteEndElement();
    } catch (Exception ex) {
      Response.Clear();
      Response.Write(string.Format("{0}", ex.Message));
    } finally {
      if (drEmpregadosPedidos != null) {
        drEmpregadosPedidos.Close();
      }
      if (cnAdventureWorks != null) {
        cnAdventureWorks.Close();
      }
      if (xwEmpregadosPedidos != null) {
        xwEmpregadosPedidos.Close();
      }
    }
  }
}
```

Observe na Listagem 5, que um objeto da classe SqlDataReader é utilizado para navegar pelos registros do resultado de uma [consulta SQL](https://www.devmedia.com.br/tutorial-sql/2973) para obter dados de empregados em atividade e a quantidade de pedidos por eles atendidos no banco de dados AdventureWorks num servidor [SQL Server](https://www.devmedia.com.br/primeiros-passos-no-sql-server/40653) 2005.

Durante a navegação, um objeto do tipo XmlTextWriter é usado para montar o documento XML dinamicamente. A Listagem 6 apresenta um fragmento de documento XML gerado dinamicamente pela página Empregados.aspx.

**Listagem 6.** Fragmento do documento XML de empregados gerado dinamicamente.

```
<xml version="1.0" encoding="iso-8859-1"?>
<Empregados>
  <Empregado>
    <Codigo>264</Codigo>
    <PrimeiroNome>Annette</PrimeiroNome>
    <SobrenomeMeio>L</SobrenomeMeio>
    <SobrenomeFinal>Hill</SobrenomeFinal>
    <QuantidadePedidos>340</QuantidadePedidos>
  </Empregado>
  ...
</Empregados>
```

Ainda na Listagem 5, pode-se verificar que se ocorrer algum erro durante o processamento, então a exceção lançada será capturada e a mensagem de erro será enviada em uma estrutura XML para o browser cliente.

A Listagem 7 apresenta um documento XML com uma mensagem de erro gerada quando o serviço do servidor de banco de dados do SQL Server 2005 está parado durante o processamento da página Empregados.aspx.

**Listagem 7.** Fragmento de documento XML com um erro de processamento.

```
<Erro>
  An error has occurred while establishing a
  connection to the server. When connecting to SQL
  Server 2005, this failure may be caused by the
  fact that under the default settings SQL Server does
  not allow remote connections. (provider: SQL Network
  Interfaces, error: 26 - Error Locating
  Server/Instance Specified)
</Erro>
```

### JavaScript 1.5, 1.6 e 1.7

JavaScript é uma linguagem de script fundamentada no conceito de programação baseada em protótipos que foi desenvolvida pela Netscape Communications Corporation e introduzida em 1995.

A linguagem JavaScript foi padronizada pela Ecma International em 1997, sendo denominada ECMAScript e, atualmente, seu desenvolvimento é conduzido pela Mozilla Foundation. A implementação do ECMAScript no Internet Explorer é denominada JScript.

<iframe src="https://www.youtube.com/embed/Fu6p9TidKZc?rel=0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen="" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; height: 455.062px; width: 809px;"></iframe>

Porém, atualmente é comum utilizar o nome JavaScript de forma generalizada, incluindo a implementação no browser da Microsoft. A linguagem é mais conhecida pelo seu uso extensivo em Web Sites como JavaScript do lado do cliente, mas também é usada em scripts para acesso a objetos incorporados em outras aplicações.

A linguagem JavaScript 1.5 segue o padrão ECMA-262, 3a edição do ECMAScript Language Specification de dezembro de 1999, criado pela comitê técnico TC39 do Ecma International.

O JavaScript 1.6 introduz novas características ao JavaScript 1.5: E4X (ECMAScript for XML), novos métodos do Array, dentre outras novidades.

O JavaScript 1.7 introduz novas características ao JavaScript 1.6: iterators, expressões let, dentre outras novidades. Por uma questão de compatibilidade com uma quantidade maior de browsers, atualmente é interessante se limitar aos recursos da linguagem JavaScript 1.5.

O JavaScript 2.0 será a próxima revisão principal da [linguagem JavaScript](https://www.devmedia.com.br/guia/javascript/34372). Ela está sendo padronizada pelo Ecma International como a 4a edição do ECMAScript Language Specification.

### Objeto XMLHttpRequest

O XMLHttpRequest define uma API que fornece funcionalidades para scripts do lado do cliente para transferência de dados entre o browser e o servidor Web. O objeto suporta qualquer formato baseado em texto, incluindo XML e JSON. Ele pode ser utilizado para fazer requisições ao servidor Web usando os protocolos HTTP e HTTPS e representa uma das partes mais importantes do AJAX.

O conceito por trás do XMLHttpRequest foi desenvolvido originalmente pela Microsoft como parte do Outlook Web Access 2000. A implementação inicial da Microsoft era chamada XMLHTTP e foi disponibilizada no Internet Explorer 5.0 como um ActiveX, sendo acessível via JScript, VBScript ou outra linguagem de script cliente suportada pelo browser via plug-ins.

Do Internet Explorer 5.0 ao 6.0, o XMLHTTP foi implementado como um ActiveX fornecido pelo MSXML. Baseado no [objeto XMLHTTP da Microsoft](https://www.devmedia.com.br/solucao-do-problema-de-acentos-do-xmlhttp-da-microsoft/4634), a Fundação Mozilla incorporou a primeira implementação nativa do XMLHttpRequest no browser Mozilla 1.0 em 2002.

Posteriormente, o suporte nativo ao XMLHttpRequest foi implementado em outros browsers: Apple Safari desde a versão 1.2, Opera desde a versão 8.0, Konqueror, dentre outros. A própria Microsoft resolveu incluir o XMLHttpRequest como um objeto nativo de script a partir do Internet Explorer 7.0.

A linguagem JavaScript do lado do cliente e o XMLHttpRequest serão utilizados para estabelecer uma comunicação HTTP assíncrona entre o browser e o servidor Web.

No projeto do Web Site, crie uma pasta com nome “Scripts” e dentro dela acrescente um arquivo JScript com o nome “AJAX.js”.

A Listagem 8 apresenta um código JavaScript para criar um XMLHttpRequest de modo cross-browser e utilizá-lo para fazer uma requisição HTTP assíncrona para o servidor Web a partir do browser.

**Listagem 8.** Arquivo JavaScript AJAX.js.

```
var READY_STATE_UNINITIALIZED = 0;
var READY_STATE_LOADING = 1;
var READY_STATE_LOADED = 2;
var READY_STATE_INTERACTIVE = 3;
var READY_STATE_COMPLETE = 4;
var req = null;

function criarXMLHTTPRequest() {
  var xRequest = null;
  if (window.XMLHttpRequest) {
    //Mozilla 1.0+, Netscape 8.0+, Firefox 1.0+,
    //Safari 1.2+, Internet Explorer 7.0+
    xRequest = new XMLHttpRequest();
  } else if (window.ActiveXObject) {
    //Internet Explorer 5.0, 5.5, 6.0
    var progIDs = ["MSXML2.XMLHTTP.6.0", "MSXML2.XMLHTTP.4.0", "MSXML2.XMLHTTP.3.0", "MSXML2.XMLHTTP", "Microsoft.XMLHTTP"];
    for (var i = 0; xRequest == null && i < progIDs.length; i++) {
      xRequest = new ActiveXObject(progIDs[i]);
    }
  }
  return xRequest;
}

function enviarRequisicaoHTTP(url, parametros, metodoHTTP, metodoCallback) {
  if (!metodoHTTP) {
    metodoHTTP = "GET";
  }
  req = criarXMLHTTPRequest();
  if (req) {
    req.onreadystatechange = metodoCallback;
    req.open(metodoHTTP, url, true);
    req.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
    req.send(parametros);
  } else {
    alert("Objeto XMLHttpRequest não suportado pelo " + "browser.");
  }
}
```

No início do script, cinco variáveis auxiliares são definidas com os estados monitorados pelo XMLHttpRequest durante uma comunicação HTTP assíncrona entre o browser e o servidor Web. A variável req é definida para conter uma referência a um XMLHttpRequest. O método criarXMLHttpRequest é responsável por criar um XMLHttpRequest de modo cross-browser, funcionando em versões variadas de diversos browsers.

Finalmente, o método enviarRequisicaoHTTP recebe informações sobre como enviar uma [requisição HTTP assíncrona](https://www.devmedia.com.br/etapas-e-tempos-de-requisicoes-http/32618) do browser para o servidor Web. Observe que um argumento metodo Callback permite definir um método JavaScript de retorno da chamada assíncrona, que será responsável pelo processamento da resposta enviada pelo servidor Web.

A Listagem 9 apresenta o elemento <script> que deve ser acrescentado ao cabeçalho da página Pedidos.htm para vinculá-la ao código JavaScript definido no arquivo AJAX.js.

**Listagem 9.** Script para vincular Pedidos.htm ao script AJAX.js.

```
...
<head>
  <title>Adventure Works - Pedidos por empregado</title>
  <link href="Estilos.css" rel="stylesheet"
    type="text/css" />
  <script type="text/javascript"
    src="Scripts/AJAX.js"></script>
</head>
...
```

### DOM Level 3

O DOM (Document Object Model) Level 3 Core Specification define um conjunto de objetos e interfaces para acessar e manipular documentos HTML e XML.

O DOM Level 3 Load and Save Specification define um conjunto de interfaces para carregar e salvar documentos HTML e XML.

Com o objetivo de tornar o [código JavaScript do lado do cliente](https://www.devmedia.com.br/javascript-tutorial/37257) compatível com um maior número de browsers, somente serão usados [recursos do DOM](https://www.devmedia.com.br/javascript-dom-introducao-a-api/30161) Level 1. Acrescente um arquivo JScript com o nome de “AdvWorks.js” dentro da pasta Scripts.

A Listagem 10 apresenta código JavaScript para, entre outras tarefas, enviar uma requisição HTTP ao servidor Web para receber a relação de empregados no formato XML de forma assíncrona.

**Listagem 10.** Arquivo JavaScript AvdWorks.js

```
var TIPO_INFO_SELECIONAR_EMPREGADO = 1;
var TIPO_INFO_SELECIONAR_MES_ANO_PEDIDOS = 2;

function apresentarMensagemProgresso(mensagem) {
  var divMensagem = document.getElementById("divMensagem");
  with(divMensagem) {
    innerHTML = mensagem;
    style.visibility = "visible";
  }
}

function esconderMensagemProgresso() {
  var divMensagem = document.getElementById("divMensagem");
  with(divMensagem) {
    innerHTML = "";
    style.visibility = "hidden";
  }
}

function apresentarInfo(tipoInfo) {
  var selectEmpregados = document.getElementById("selectEmpregados");
  var selectMesesAnosPedidos = document.getElementById("selectMesesAnosPedidos");
  var spanEmpregadoPedidos = document.getElementById("spanEmpregadoPedidos");
  var spanMesAnoPedidos = document.getElementById("spanMesAnoPedidos");
  var divMesAnoPedidos = document.getElementById("divMesAnoPedidos");
  switch (tipoInfo) {
  case TIPO_INFO_SELECIONAR_EMPREGADO:
    selectMesesAnosPedidos.options.length = 0;
    selectMesesAnosPedidos.options[0] = new Option("Selecione um empregado para obter os meses " + "e anos com pedidos...", "");
    spanEmpregadoPedidos.innerHTML = "";
    spanMesAnoPedidos.innerHTML = "";
    divMesAnoPedidos.innerHTML = "Selecione um " + "empregado e um mês e ano para obter os " + "pedidos do mês...";
    break;
  case TIPO_INFO_SELECIONAR_MES_ANO_PEDIDOS:
    spanMesAnoPedidos.innerHTML = "";
    divMesAnoPedidos.innerHTML = "Selecione um mês " + "e ano para obter os pedidos do mês...";
  }
}

function preencherListaEmpregados() {
  if (req.readyState == READY_STATE_COMPLETE) {
    var selectEmpregados = document.getElementById("selectEmpregados");
    selectEmpregados.options.length = 0;
    selectEmpregados.options[0] = new Option("", "");
    var docEmpregados = req.responseXML;
    var eleRaiz = docEmpregados.documentElement;
    switch (eleRaiz.nodeName) {
    case "Empregados":
      var nodeListEmpregados = eleRaiz.getElementsByTagName("Empregado");
      for (var i = 0; i < nodeListEmpregados.length; i++) {
        var nodeEmpregado = nodeListEmpregados.item(i);
        var obterValor = function (elemento) {
          return nodeEmpregado.getElementsByTagName(elemento).item(0).firstChild.nodeValue;
        };
        var codigo = obterValor("Codigo");
        var primeiroNome = obterValor("PrimeiroNome");
        var sobrenomeMeio = obterValor("SobrenomeMeio");
        var sobrenomeFinal = obterValor("SobrenomeFinal");
        var quantidadePedidos = parseInt(obterValor("QuantidadePedidos"));
        var textoOpcaoSelect = primeiroNome + " " + sobrenomeMeio + " " + sobrenomeFinal + " (" + quantidadePedidos + " pedido" + (quantidadePedidos > 1 ? "s" : "") + ")";
        var valorOpcaoSelect = codigo;
        selectEmpregados.options[i + 1] = new Option(textoOpcaoSelect, valorOpcaoSelect);
      }
      break;
    case "Erro":
      var erro = eleRaiz.firstChild.nodeValue;
      alert("Ocorreu um erro no processo de carga " + "dos empregados.\n(" + erro + ")");
    }
    req = null;
    esconderMensagemProgresso();
  }
}
window.onload = function () {
  apresentarMensagemProgresso("Carregando os " + "empregados responsáveis pelos pedidos...");
  enviarRequisicaoHTTP("Empregados.aspx", null, null, preencherListaEmpregados);
  apresentarInfo(TIPO_INFO_SELECIONAR_EMPREGADO);
};
```

Segue uma breve descrição das funcionalidades presentes no arquivo AdvWorks.js.

- apresentarMensagemProgresso: mostra uma mensagem de progresso de uma chamada assíncrona ao servidor Web para o usuário;
- esconderMensagemProgresso: oculta uma mensagem de progresso após a finalização de uma chamada assíncrona ao servidor Web;
- apresentarInfo: apresenta informações explicativas, de acordo com o tipo escolhido, sobre como o usuário deve proceder para consultar informações de pedidos atendidos por empregados da empresa Adventure Works;
- apresentarInfo: apresenta informações explicativas, de acordo com o tipo escolhido, sobre como o usuário deve proceder para consultar informações de pedidos atendidos por empregados da empresa Adventure Works;
- evento onload do objeto window: executa uma chamada assíncrona ao servidor Web para obter a relação de empregados que atenderam a pedidos de clientes, deixando o usuário informado do progresso e de como proceder.

A Listagem 11 apresenta o elemento <script> que deve ser acrescentado ao cabeçalho da página Pedidos.htm para vinculá-la ao código JavaScript definido no arquivo AdvWorks.js.

**Listagem 11.** Script para vincular Pedidos.htm ao script AdvWorks.js

```
...
<head>
  <title>Adventure Works - Pedidos por empregado</title>
  <link href="Estilos.css" rel="stylesheet"
    type="text/css" />
  <script type="text/javascript"
    src="Scripts/AJAX.js"></script>
  <script type="text/javascript"
    src="Scripts/AdvWorks.js"></script>
</head>
...
```

### JSON

O JSON (JavaScript Object Notation) é um formato leve para troca de dados baseado em um subconjunto da linguagem de programação JavaScript, padrão ECMA-262 3a edição. Na notação JSON:

- objetos são considerados um conjunto não ordenado de pares nome/valor. Um objeto é delimitado por chaves. Cada nome é separado do valor por dois pontos e os pares nome/valor são separados por vírgulas;
- arrays são considerados uma coleção ordenada de valores. Um array é delimitado por colchetes. Os valores são separados por vírgulas.

O uso do formato JSON como mecanismo de transporte de dados tem algumas implicações de segurança. Um método de ataque a aplicações Web denominado JavaScript Hijacking permite o envio de dados não autorizados para um site remoto, iludindo a política de mesma origem (Same Origin Policy) garantida pelos browsers mais modernos.

Para obter informações detalhadas sobre esse tipo de ataque e técnicas de proteção, leia o artigo JavaScript Hijacking publicado pela empresa Fortify Software, cujo link pode ser encontrado no final deste artigo.

O artigo cita a análise de 12 frameworks AJAX populares, incluindo o Microsoft ASP.NET AJAX, concluindo que somente o DWR 2.0 (Direct Web Remoting) implementa mecanismos para prevenir esse tipo de ataque.

Porém, o artigo analisou uma versão anterior à versão 1.0 final do Microsoft ASP.NET AJAX, quando o mesmo ainda era conhecido pelo codinome Microsoft “Atlas”. Em 4 de abril de 2007, o Scott Guthrie (um gerente geral da Divisão de Desenvolvimento da Microsoft) postou em seu blog o artigo “JSON Hijacking and How ASP.NET AJAX 1.0 Avoids these Attacks” que contesta a informação de que o ASP.NET AJAX não implementa mecanismos para prevenir ataques JavaScript Hijacking. Veja o endereço da postagem no blog do Scott Guthrie no final deste artigo.

Adicione um Web Form nomeando-o PedidosPorEmpregado.aspx e selecionando a opção Place code in separate file. Apague todo o código HTML da página PedidosPorEmpregado.aspx, deixando somente a diretiva @PageM. Codifique o arquivo PedidosPorEmpregado.aspx.cs como apresentado na Listagem 12.

**Listagem 12.** Arquivo code-behind PedidosPorEmpregado.aspx.cs.

```
...
using System.Collections.Generic;
using System.Data.SqlClient;
using System.IO;
using System.Text;
public partial class PedidosPorEmpregado: System.Web.UI.Page {
  protected void Page_Load(object sender, EventArgs e) {
    Response.ContentType = "application/json";
    string codigoEmpregado = Request.Form["CodigoEmpregado"];
    int employeeID = (codigoEmpregado == null) ? 0 : int.Parse(codigoEmpregado);
    TextWriter twPedidosMesAno = null;
    SqlConnection cnAdventureWorks = null;
    SqlDataReader drPedidosMesAno = null;
    try {
      cnAdventureWorks = new SqlConnection();
      cnAdventureWorks.ConnectionString = ConfigurationManager.ConnectionStrings["cnAdventureWorks"].ConnectionString;
      SqlCommand cmPedidosMesAno = new SqlCommand();
      cmPedidosMesAno.Connection = cnAdventureWorks;
      cmPedidosMesAno.CommandText = @"
        SELECT MONTH(OrderDate) AS mesPedidos
          , YEAR(OrderDate) AS anoPedidos
          , COUNT(*) AS quantidade
        FROM Purchasing.PurchaseOrderHeader
        WHERE EmployeeID = @EmployeeID
        GROUP BY MONTH(OrderDate)
          , YEAR(OrderDate)
        ORDER BY anoPedidos DESC
          , mesPedidos DESC";
      cmPedidosMesAno.Parameters.Add("@EmployeeID", SqlDbType.Int).Value = employeeID;
      cnAdventureWorks.Open();
      drPedidosMesAno = cmPedidosMesAno.ExecuteReader();
      List < string > arrayObjetosJson = new List < string > ();
      while (drPedidosMesAno.Read()) {
        string[] objetoJson = new string[drPedidosMesAno.FieldCount];
        for (int campo = 0; campo < drPedidosMesAno.FieldCount; campo++) {
          objetoJson[campo] = string.Format("\"{0}\":{1}", drPedidosMesAno.GetName(campo), drPedidosMesAno[campo].ToString());
        }
        arrayObjetosJson.Add(string.Format("{{{0}}}", string.Join(",", objetoJson)));
      }
      twPedidosMesAno = new StreamWriter(Response.OutputStream, Encoding.GetEncoding("ISO-8859-1"));
      twPedidosMesAno.Write(string.Format("[{0}]", string.Join(",\n", arrayObjetosJson.ToArray())));
    } catch (Exception ex) {
      Response.Clear();
      Response.Write(string.Format("{{\"erro\":\"{0}\"}}", ex.Message));
    } finally {
      if (drPedidosMesAno != null) {
        drPedidosMesAno.Close();
      }
      if (cnAdventureWorks != null) {
        cnAdventureWorks.Close();
      }
      if (twPedidosMesAno != null) {
        twPedidosMesAno.Close();
      }
    }
  }
}
```

Observe na Listagem 12 que um objeto da classe SqlDataReader é utilizado para navegar pelos registros do resultado de uma consulta SQL, usada para obter a quantidade de pedidos por mês e ano de um determinando empregado no banco de dados AdventureWorks no servidor SQL Server 2005.

Durante a navegação, uma coleção genérica List <string>, arrays de strings e um objeto StreamWriter são usados para montar um texto no formato JSON. A Listagem 13 apresenta um fragmento de texto no formato JSON gerado dinamicamente pela página PedidosPorEmpregado.aspx quando o parâmetro CodigoEmpregado, passado pelo método HTTP POST, é igual a 264.

**Listagem 13.** Fragmento de texto no formato JSON gerado dinamicamente.

```
[{
  "mesPedidos": 9,
  "anoPedidos": 2004,
  "quantidade": 4
}, {
  "mesPedidos": 8,
  "anoPedidos": 2004,
  "quantidade": 39
}, {
  "mesPedidos": 7,
  "anoPedidos": 2004,
  "quantidade": 35
}, ... {
  "mesPedidos": 2,
  "anoPedidos": 2002,
  "quantidade": 5
}, {
  "mesPedidos": 1,
  "anoPedidos": 2002,
  "quantidade": 1
}]
```

Ainda na Listagem 12, pode-se verificar que se ocorrer algum erro durante o processamento, então a exceção lançada será capturada e a mensagem de erro será enviada no formato JSON para o browser cliente.

A Listagem 14 apresenta um texto com uma mensagem de erro gerada quando o serviço do servidor de banco de dados do SQL Server 2005 está parado durante o processamento da página Web PedidosPorEmpregado.aspx.



**Listagem 14.** Fragmento de texto com um erro de processamento

```
{
  "erro": "An error has occurred while establishing a
  connection to the server.  When connecting to SQL
  Server 2005, this failure may be caused by the fact
  that under the default settings SQL Server does not
  allow remote connections. (provider: SQL Network
  Interfaces, error: 26 - Error Locating
  Server/Instance Specified)"
}
```

Acrescente mais JavaScript ao código de manipulação do evento onload do objeto window no arquivo AdvWorkd.js, um array nomeado meses e um outro método callback nomeado preencherListaMesesAnosPedidos, conforme apresentado na Listagem 15.

**Listagem 15.** Acrescentando código ao arquivo AvdWorks.js

```
window.onload = function () {... //código anterior
  var selectEmpregados = document.getElementById("selectEmpregados");
  selectEmpregados.onchange = function () {
    if (selectEmpregados.selectedIndex == 0) {
      apresentarInfo(TIPO_INFO_SELECIONAR_EMPREGADO);
    } else {
      var spanEmpregadoPedidos = document.getElementById("spanEmpregadoPedidos");
      var codigoEmpregado;
      with(selectEmpregados) {
        spanEmpregadoPedidos.innerHTML = options[selectedIndex].text;
        codigoEmpregado = options[selectedIndex].value;
      }
      var parametroEmpregado = "CodigoEmpregado=" + codigoEmpregado;
      apresentarMensagemProgresso("Carregando os meses e os anos dos pedidos...");
      enviarRequisicaoHTTP("PedidosPorEmpregado.aspx", parametroEmpregado, "POST", preencherListaMesesAnosPedidos);
      apresentarInfo(TIPO_INFO_SELECIONAR_MES_ANO_PEDIDOS);
    }
  };
};
var meses = ["Janeiro", "Fevereiro", "Março", "Abril", "Maio", "Junho", "Julho", "Agosto", "Setembro", "Outubro", "Novembro", "Dezembro"];

function preencherListaMesesAnosPedidos() {
  if (req.readyState == READY_STATE_COMPLETE) {
    var selectMesesAnosPedidos = document.getElementById("selectMesesAnosPedidos");
    selectMesesAnosPedidos.options.length = 0;
    selectMesesAnosPedidos.options[0] = new Option("", "");
    var arrJSONMesesAnosPedidos = eval("(" + req.responseText + ")");
    if (arrJSONMesesAnosPedidos.constructor.toString().indexOf("function Array()") != -1) {
      for (var i = 0; i < arrJSONMesesAnosPedidos.length; i++) {
        with(arrJSONMesesAnosPedidos[i]) {
          var textoOpcaoSelect = meses[mesPedidos - 1] + " de " + anoPedidos + " (" + quantidade + " pedido" + (quantidade > 1 ? "s" : "") + ")";
          var valorOpcaoSelect = mesPedidos + "," + anoPedidos;
          selectMesesAnosPedidos.options[i + 1] = new Option(textoOpcaoSelect, valorOpcaoSelect);
        }
      }
    } else if (arrJSONMesesAnosPedidos.erro) {
      alert("Ocorreu um erro no processo de carga " + "dos meses e anos dos pedidos.\n(" + arrJSONMesesAnosPedidos.erro + ")");
    }
    req = null;
    esconderMensagemProgresso();
  }
}
```

Segue uma breve descrição das funcionalidades acrescentadas no arquivo AdvWorks.js.

- evento onload do objeto window: acrescenta código para manipular o evento onchange do objeto Select com id igual a selectEmpregados. Se o usuário selecionar um empregado diferente, então é executada uma chamada assíncrona ao servidor Web para obter a relação de meses e anos com as respectivas quantidades de pedidos atendidos pelo empregado selecionado, deixando o usuário informado do progresso e de como proceder;
- array meses: armazena os nomes dos meses do ano em idioma português brasileiro;
- preencherListaMesesAnosPedidos: método callback de uma chamada assíncrona ao servidor Web para receber a relação de meses e anos com as respectivas quantidades de pedidos atendidos pelo empregado selecionado em formato JSON e preencher o quadro de listagem apropriado com uso de DOM.

#### Finalização da aplicação de demonstração

Para finalizar a **aplicação Web AJAX** de demonstração, vamos criar uma página Web ASP.NET para gerar o código de uma tabela HTML com os pedidos de um dado empregado, num determinado mês e ano.

Adicione um Web Form nomeando-o PedidosPorEmpregadoMesAno.aspx selecionando a opção Place code in separate file. Apague todo o código HTML da página PedidosPorEmpregado.aspx, deixando somente a diretiva @Page e acrescentando o elemento <form runat="server"></form>, pois Web Server Controls somente podem ser hospedados em páginas ASPX que são Web Forms.

Acrescente um GridView e um Label ao Web Form ASPX e defina as propriedades como apresentado na Listagem 16.

**Listagem 16.** Arquivo PedidosPorEmpregadoMesAno.aspx

```
<%@ Page Language="C#" AutoEventWireup="true" CodeFile="PedidosPorEmpregadoMesAno.aspx.cs" Inherits="PedidosPorEmpregadoMesAno" EnableViewState="false" %>
  <form runat="server">
    <asp:gridview id="gvPedidosPorEmpregadoMesAno" runat="server" autogeneratecolumns="False" CssClass="dados">
      <Columns>
        <asp:BoundField DataField="Codigo" HeaderText="Código">
          <ItemStyle HorizontalAlign="Center" />
        </asp:BoundField>
        <asp:BoundField HtmlEncode="False" DataFormatString="{0:d}" DataField="DataPedido" HeaderText="Data do pedido">
          <ItemStyle HorizontalAlign="Center" />
        </asp:BoundField>
        <asp:BoundField HtmlEncode="False" DataFormatString="{0:C}" DataField="Subtotal" HeaderText="Subtotal">
          <ItemStyle HorizontalAlign="Right" />
        </asp:BoundField>
        <asp:BoundField HtmlEncode="False" DataFormatString="{0:C}" DataField="Taxa" HeaderText="Taxa">
          <ItemStyle HorizontalAlign="Right" />
        </asp:BoundField>
        <asp:BoundField HtmlEncode="False" DataFormatString="{0:C}" DataField="Frete" HeaderText="Frete">
          <ItemStyle HorizontalAlign="Right" />
        </asp:BoundField>
        <asp:BoundField HtmlEncode="False" DataFormatString="{0:C}" DataField="Total" HeaderText="Total">
          <ItemStyle HorizontalAlign="Right" />
        </asp:BoundField>
      </Columns>
      <AlternatingRowStyle CssClass="alt" />
    </asp:gridview>
    <asp:label id="lblErro" runat="server"></asp:label>
  </form>
```

Codifique o arquivo PedidosPorEmpregadoMesAno.aspx.cs como apresentado na Listagem 17.

**Listagem 17.** Arquivo code-behind PedidosPorEmpregadoMesAno.aspx.cs.

```
...
using System.Data.SqlClient;
using System.Web.UI.WebControls;
public partial class PedidosPorEmpregadoMesAno: System.Web.UI.Page {
  protected void Page_Load(object sender, EventArgs e) {
    Response.ContentType = "text/xml";
    int employeeID = (Request.Form["CodigoEmpregado"] == null) ? 0 : int.Parse(Request.Form["CodigoEmpregado"]);
    int mesPedidos = (Request.Form["MesPedidos"] == null) ? 0 : int.Parse(Request.Form["MesPedidos"]);
    int anoPedidos = (Request.Form["AnoPedidos"] == null) ? 0 : int.Parse(Request.Form["AnoPedidos"]);
    SqlConnection cnAdventureWorks = null;
    SqlDataReader drPedidosPorEmpregadoMesAno = null;
    try {
      cnAdventureWorks = new SqlConnection();
      cnAdventureWorks.ConnectionString = ConfigurationManager.ConnectionStrings["cnAdventureWorks"].ConnectionString;
      SqlCommand cmPedidosPorEmpregadoMesAno = new SqlCommand();
      cmPedidosPorEmpregadoMesAno.Connection = cnAdventureWorks;
      cmPedidosPorEmpregadoMesAno.CommandText = @"
        SELECT PurchaseOrderID AS Codigo
          , OrderDate AS DataPedido
          , SubTotal AS Subtotal
          , TaxAmt AS Taxa
          , Freight AS Frete
          , TotalDue AS Total
        FROM Purchasing.PurchaseOrderHeader AS PedidoMesAno
        WHERE EmployeeID = @EmployeeID
          AND MONTH(OrderDate) = @MesPedidos
          AND YEAR(OrderDate) = @AnoPedidos
        ORDER BY OrderDate";
      cmPedidosPorEmpregadoMesAno.Parameters.Add("@EmployeeID", SqlDbType.Int).Value = employeeID;
      cmPedidosPorEmpregadoMesAno.Parameters.Add("@MesPedidos", SqlDbType.Int).Value = mesPedidos;
      cmPedidosPorEmpregadoMesAno.Parameters.Add("@AnoPedidos", SqlDbType.Int).Value = anoPedidos;
      cnAdventureWorks.Open();
      drPedidosPorEmpregadoMesAno = cmPedidosPorEmpregadoMesAno.ExecuteReader();
      gvPedidosPorEmpregadoMesAno.DataSource = drPedidosPorEmpregadoMesAno;
      gvPedidosPorEmpregadoMesAno.DataBind();
    } catch (Exception ex) {
      lblErro.Text = ex.Message;
    } finally {
      if (drPedidosPorEmpregadoMesAno != null) {
        drPedidosPorEmpregadoMesAno.Close();
      }
      if (cnAdventureWorks != null) {
        cnAdventureWorks.Close();
      }
    }
  }
}
```

O código da Listagem 17 recebe os parâmetros com o código do empregado, o mês e o ano dos pedidos enviados pelo método HTTP POST. Depois, executa uma consulta no banco de dados AdventureWorks que retorna um SqlDataReader.

Esse objeto é passado para a propriedade DataSource do GridView para gerar o código XHTML de uma tabela formatando os dados. Caso ocorra algum erro de processamento, a exceção lançada é capturada e a mensagem de erro é colocada no Label.

Com uso das tecnologias do AJAX, parte deste código XHTML será embutido numa parte da página Pedidos.htm, conforme apresentado no código da Listagem 18 a seguir.

**Listagem 18.** Acrescentando código ao arquivo AvdWorks.js

```
window.onload = function () {...
  selectMesesAnosPedidos.onchange = function () {
    if (selectMesesAnosPedidos.selectedIndex == 0) {
      apresentarInfo(TIPO_INFO_SELECIONAR_MES_ANO_PEDIDOS);
    } else {
      var spanMesAnoPedidos = document.getElementById("spanMesAnoPedidos");
      var mesAnoPedidos, mesPedidos, anoPedidos;
      with(selectMesesAnosPedidos) {
        spanMesAnoPedidos.innerHTML = " de " + options[selectedIndex].text.toLowerCase();
        mesAnoPedidos = options[selectedIndex].value.split(",");
      }
      mesPedidos = parseInt(mesAnoPedidos[0]);
      anoPedidos = parseInt(mesAnoPedidos[1]);
      var parametrosEmpregadoMesAno = "CodigoEmpregado=" + codigoEmpregado + "&MesPedidos=" + mesPedidos + "&AnoPedidos=" + anoPedidos;
      apresentarMensagemProgresso("Carregando os pedidos do empregado no mês e ano...");
      enviarRequisicaoHTTP("PedidosPorEmpregadoMesAno.aspx", parametrosEmpregadoMesAno, "POST", apresentarTabelaPedidosEmpregadoMesAno);
    }
  }
}
};
};

function apresentarTabelaPedidosEmpregadoMesAno() {
  if (req.readyState == READY_STATE_COMPLETE) {
    var xhtml = req.responseText;
    var indiceInicial = xhtml.indexOf("<table>");
    if (indiceInicial >= 0) {
      var indiceFinal = xhtml.lastIndexOf("</table>") + 8;
      var xhtmlTabela = xhtml.substring(indiceInicial, indiceFinal);
      var divMesAnoPedidos = document.getElementById("divMesAnoPedidos");
      divMesAnoPedidos.innerHTML = xhtmlTabela;
    } else {
      var erro = req.responseXML.getElementsByTagName("span")[0].firstChild.nodeValue;
      alert("Ocorreu um erro no processo de carga " + "dos pedidos de um mês e ano.\n(" + erro + ")");
    }
    req = null;
    esconderMensagemProgresso();
  }
}
```

Segue uma breve descrição das funcionalidades acrescentadas no arquivo AdvWorks.js.

- evento onload do objeto window: acrescenta código para manipular o evento onchange do objeto Select com id igual a selectMesesAnosPedidos>. Se o usuário selecionar um par mês/ano diferente, então é executada uma chamada assíncrona ao servidor Web para obter a relação de pedidos do empregado no mês e ano selecionados;
- apresentarTabelaPedidosEmpregadoMesAno: método callback de uma chamada assíncrona ao servidor Web para receber a relação de pedidos do empregado no mês e ano selecionados em formato XHTML e atualizar a interface com a tabela gerada dinamicamente pelo GridView.

A Figura 3 apresenta a interface da página Web Pedidos.htm visualizada no Internet Explorer 7.0 após o usuário selecionar opções disponíveis nos quadros de seleção.

![Resultado de uma consulta na página Pedidos.htm no IE 7.0](https://www.devmedia.com.br/Imagens/msdnmagazine1/edicoes/42/net42-rogerio-ajax_arquivos/image006.jpg)**Figura 3.** Resultado de uma consulta na página Pedidos.htm no IE 7.0

### O que é o ASP.NET AJAX 1.0?

O ASP.NET AJAX 1.0 é um framework gratuito, fornecido pela Microsoft, que permite a criação rápida de uma nova geração de aplicações Web mais eficientes, mais interativas e altamente personalizadas que funciona em todos os browsers mais populares da atualidade.

Seguem algumas das características do ASP.NET AJAX:

- Corresponde a uma extensão do ASP.NET 2.0, tendo integração com o Visual Studio 2005;
- Permite a criação de interfaces Web ricas com componentes AJAX reutilizáveis;
- Fornece recursos para sofisticar as páginas ASP.NET 2.0 existentes usando poderosos controles AJAX com suporte para todos os principais browsers mais modernos;
- Possui recursos para acesso a serviços e dados remotos diretamente do browser sem a necessidade de escrever uma grande quantidade de scripts;
- Fornece os benefícios de um framework gratuito com suporte técnico fornecido pela Microsoft.

##### Conclusão

**O AJAX permite criar aplicações Web muito mais ricas, interativas e com respostas mais rápidas para os usuários**. Os recursos do AJAX e da Web 2.0 começaram a ser utilizados em diversos sites e corresponde a uma tendência real no desenvolvimento Web atualmente.

O objetivo deste primeiro artigo do mini-curso de ASP.NET AJAX foi apresentar e ilustrar as principais tecnologias que compõem o AJAX. A aplicação Web de demonstração mostrou como desenvolver toda a infra-estrutura de uma aplicação AJAX a partir do zero.

Desse modo, os desenvolvedores Web podem ter uma visão clara dos bastidores do AJAX e compreender melhor como utilizar frameworks AJAX disponíveis, como o Microsoft ASP.NET AJAX.

Apesar de se ter utilizado o ASP.NET 2.0 para gerar os dados XML e JSON dinamicamente do lado do servidor, qualquer outra tecnologia do lado do servidor poderia ter sido utilizada, como: PHP, Servlets/JSP/JSF, ASP legado, CGI, ISAPI, dentre outras.

Nos próximos artigos do mini-curso serão abordados os recursos do framework Microsoft ASP.NET AJAX que tornam o desenvolvimento de aplicações ASP.NET 2.0 com recursos de AJAX muito simples.

#### Links Úteis

- [Modelagem de dados: 1:N ou N:N?](https://www.devmedia.com.br/modelagem-de-dados-1-n-ou-n-n/38894):
  Você sabe quando usar um relacionamento do tipo 1:N ou N:N? Optar pelo tipo incorreto pode impactar diretamente no negócio.
- [C# Exceptions: Trabalhando com exceções em C#](https://www.devmedia.com.br/curso/csharp-exceptions-trabalhando-com-excecoes-em-csharp/2072):
  Neste curso você aprenderá a lidar com exceções em suas aplicações C#.

#### Saiba mais sobre AJAX ;)

- [Adoramos Ajax](https://www.devmedia.com.br/adoramos-ajax/37919):
  Neste DevCast veremos como a equipe de programação da DevMedia utilizou a técnica de Lazy Load, com jQuery, para otimizar o tempo de carregamento da página por meio de requisições Ajax.
- [PHP + Ajax + JavaScript](https://www.devmedia.com.br/php-ajax-javascript/34648):
  Hoje iremos propor o conserto de um pequeno bug em um aplicativo PHP e logo após iremos mostrar uma solução.

#### Confira também

[![Front-end e JavaScript](https://www.devmedia.com.br/arquivos/Salas/Linguagem/JavaScript/52/2332/thumb.jpg)Front-end e JavaScriptGuia](https://www.devmedia.com.br/guias/javascript)

[![Cursos de JavaScript](https://www.devmedia.com.br/arquivos/cursos/curso_primeiros-passos-com-javascript_2230.png)Cursos de JavaScriptCursos](https://www.devmedia.com.br/cursos/javascript)

[![Curso de Introdução ao JavaScript](https://www.devmedia.com.br/arquivos/cursos/curso_introducao-ao-javascript_2181.png)Curso de Introdução ao JavaScriptCurso](https://www.devmedia.com.br/curso/curso-de-javascript-completo/388)

###### Links:

- AJAX: The Official Microsoft ASP.NET AJAX Site ajax.asp.net
- Artigo “Ajax: A New Approach to Web Applications”, escrito por Jesse James Garrett www.adaptivepath.com/publications/essays/archives/000385.php
- Artigo “JavaScript Hijacking” www.net-security.org/dl/articles/JavaScript_Hijacking.pdf
- Artigo “JSON Hijacking and How ASP.NET AJAX 1.0 Avoids these Attacks” weblogs.asp.net/scottgu/archive/2007/04/04/json-hijacking-and-how-asp-net-ajax-1-0-mitigates-these-attacks.aspx
- Artigo “Tableless layout HOWTO” www.w3.org/2002/03/csslayout-howto
- Ecma International www.ecma-international.org
- Firefox 2.x www.mozilla.com
- Internet Explorer 7 www.microsoft.com/windows/downloads/ie
- Google Maps maps.google.com
- Google Suggest www.google.com/webhp?complete=1
- JSON (JavaScript Object Notation) www.json.org
- Netscape Browser 8.x (está em desenvolvimento a versão 9 para várias plataformas) browser.netscape.com
- Opera 9.x www.opera.com
- SQL Server 2005 Express Edition SP2 e o banco de dados AdventureWorks msdn.microsoft.com/vstudio/express/sql/download
- Visual Web Developer 2005 Express Edition SP1 msdn.microsoft.com/vstudio/express/downloads
- World Wide Web Consortium (W3C) www.w3.org