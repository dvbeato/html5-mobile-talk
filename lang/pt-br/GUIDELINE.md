
#HTML5 Mobile

Diogo Beato - Engenheiro de Software

Atualmente compondo o time da Bluesoft, atuando em soluções de arquitetura e desenvolvimento do modulo financeiro do BluesoftERP.

**Perguntas para entender o público**
* Quem já trabalha na área?
* Quem trabalha com mobile?

## Pessoas e dispositivos móveis
Cada vez mais pessoas estão conectadas à internet através dos dispositivos mobile e cada vez é maior a variedade desses dispositivos, smartphones, tablets: Android, iOS, Windows Phone, FirefoxOS e outros.

Convencido desse nicho e querendo levar seu produto para todas essas plataformas você decide ataca-lo

## Web x Applicativo
**Tudo depende da expectativa do seu usuario.**

**Estrategia na decisão:** 
O Instagram começou com apenas um app iPhone, pois era um applicativo novo, não tinha usuários então não tinha expectativas. Agora imagina vc ter um portal na web e lançar um app soh para iphone? Você pode deixar a maioria dos seus usuários frustrados.
Outro exemplo é um site pornô. É muito dificil alguém querer instalar um applicativo porno no celular, mais facil acessar o website pelo smartphone e não deixar rastros.

## Web first
Seguir pela Web é mais seguro, todos dispositivos suportam a web.
Algum tempo atras apostar em apps iphone era certeiro, depois veio o android e tomou boa parte dos usuários
e a galera teve que correr atras. 

**Fazer pesquisa de usuários Android x iPhone x Web**

Quem sempre pensou primeiro na web não teve essas dores de cabeça.

## Mobile especifico x Web responsivo
Para o usuario é irrelevante, o que ele quer é ter a devida experiencia no devido dispositivo.

É muito importante ter em mente as diferenças de usabilidade de mobile pra desktop.
* Mobile não tem title. 
* Mobile não tem mouse:hover

E ninguém quer usar um site no notebook como se fosse um applicativo mobile gigante.

Algumas empresas ainda utilizam site especifico para mobile:
Facebook por exemplo, quando você acessa a página atravéz de um browser mobile, ele re-direciona para https://m.facebook.com/?_rdr
O twitter também utiliza um site especifico para mobile, https://mobile.twitter.com/

Porém a recomendação do google é fazer o site responsivo ao invés de um site especifico. 

## Web Responsivo
Na maioria das vezes que você procurar por site responsivo ou responsive web, os principais topicos abordados vão ser as media queries do CSS e como utiliza-las para adaptar o design do seu site conforme o tamanho da página.
Porém tem várias outras considerações a serem levadas em conta do que somente o tamanho do design. Temos que nos preocupar com a conexão, tamanho das imagens e no fluxo do uso do applicativo tabém, o Menu por exemplo é um componente que sempre sofre alterações na hora de tornar o site responsivo.

Recentemente o google alterou seu algorítimo de indexação nas buscas pra aumentar drasticamente a relevancia dos sites que são user friendly a dispositivos mobiles.

Então, nos dias de hoje sempre que vc for desenvolver um site ou uma applicação web, comece pelos principios do mobile first.

Algumas ferramentas que podem facilitar a nossa vida na hora de criar aplicativos responsivos.
* Chrome Developer.
* [Bootstrap](http://getbootstrap.com/).
* [Modernizr](https://modernizr.com/)
* [Grunt](http://gruntjs.com/)

## O diferencial do HTML5
**pergunta: Alguem sabe dizer qual é o maior diferencial que o html5 trouxe?**

Antigamente, quando queriamos desenvolver um software que precissasse de acesso direto ao hardware (utilizar a camera, a GPU para Aceleração Grafica, ou um player de audio), não tinha nem o que pensar, tinha que ser feito com linguagens como (Java, C++, C#, Ruby, etc). E se quisessemos levar esses aplicativos para a web, só era possivel através de tecnologias como Java Applet, Flash e outros do genero.

O grande diferencia do HTML5 é exatamente isso, ele traz uma serie de APIs novas que a gente começa a ter acesso a funcionalidades de alguns hardwares.
Hoje com um browser e conhecimento de javascript vc consegue fazer vários experimentos legais utilizando o hardware do seu computador sem precisar de plugins.

**show me the code**.
snippets com APIs de camera, som, canvas, GPS, etc.

## Applicativos Híbridos.
Mas a sua ideia não é web, você quer lançar um applicativo mesmo, você quer criar um aplicativo para os principais players do mercado mobile que hoje em dia são: Android, iPhone e Windows Phone.

**Então o que você precisa saber?**
* precisa saber Java para criar o App para Android
* precisa saber ObjectiveC ou Swift para criar o App para iPhone
* precisa saber C# para criar o App para Windows Phone.

E depois que você lançar e começar a ganhar dinheiro, provavelmente vai ter que ter um time que domine todas essas linguagens ou um time especialista pra cada plataforma. 

Na maioria das vezes é inviável manter um time especialista em cada plataforma. 

Você precisa gerenciar as versões muito bem.
Por que vc não pode corrigir bugs apenas em uma das plataformas, tem que corrigir em todas. Não pode lançar a nova funcionalidade só pra uma versão, tem que lançar pra todas. Ou seja, vc está multiplicando seu Trabalho.

Na Bluesoft, nossos principais produtos são feitos com Java, Groovy e Ruby. Então, como podemos resolver isso?

**Criação do PhoneGap e Cordova**
Imagine se pudessemos criar o app uma vez só e que conseguisse compilar pra todas essas plataformas. E melhor, se pudessmos utilizar uma tecnologia que fosse comum a todos os times.

Foi pensando nisso que o pessoal da Nitobi Software criou o phoneGap. 
Uma plataforma que permite desenvolver applicativos mobile utilizando html5, css3 e java.

Em 2011 a Adobe comprou o código fonte do Nitobi e logo em seguida doou para a Apache Foundation, deixando o projeto open source. A ideia da adobe era atrair a força da comunidade Apache para contribuir no projeto.
Atualmente o código fonte mantido pela apache foudation é o projeto Cordova que é a engine que faz o middleware entre a API do html5 com o código nativo de cada plataforma. 
O Phone Gap ainda eh mantido pela adobe, mas agora o projeto utiliza o Cordova como core engine e foca no desenvolvimento de novas APIs e Ferramentas que rodem em cima do Cordova.

Caramba, maravilha. Mas como isso funciona?
Internamente o projeto é um componente de WebView interno do aparelho que renderiza o HTML e o CSS para o usuario e utiliza o java para fazer a lógica e acessar funções de hardware do aparelho.

Apesar do HTML5 prover nativamente algumas funcionalidades para acesso a hardwares como GPS, Camera e acelerometro, nem todos os browsers mobile dao suporte a essas APIs, particularmente versões antigas do android. Então o Cordova inclui essas funções  dentro da webview de cada aparelho.

Compatibilidade entre os browsers.
Pelo fato do Cordova utilizar a webview do aparelho para renderizar a interface, vcs ja devem imaginar que cada vendor utiliza sua engine de browser. 
Por exemplo: 
No android a webview utiliza a engine do chrome.
No iphone a webview utiliza a engine do safari.
No windows Phone utiliza a engine do IE.
Então na hora de desenvolver é sempre bom utilizar tecnologias como o modernizr e algum css reset pra garantir que vai estar compativel com todos os browers, o que ja deve ser um problema comum de resolver para uma equipe de desenvolvimento web. 
Esses são os chamados aplicativos hibridos, pq sao aplicativos web que utilizam tecnologia nativa.

Nativo x Hibrido
Outro ponto eh que o Cordova adiciona uma camada extra entre o código do desenvolvedor e código nativo, o que certamente torna as aplicações menos performática do que as aplicações nativas. Então, dependendo do tipo de aplicação que vc quiser fazer, isso pode ser um problema e talvez a melhor opção seja utilizar código nativo mesmo.

impacto de performance entre acesso ao hardware atraves de codigo nativo x api html5, 
mas nem sempre são relevantes.
Desktop Nativo e Applicativo Web

Principais ferramentas e frameworks que auxiliam no desenvolvimento de applicativos hibridos
Ionic, Meteor, Angular, Backbone, jQuery Mobile
Backend as a service Parse e Firebase

Offiline first

That's all folks
