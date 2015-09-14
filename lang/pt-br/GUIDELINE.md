
#HTML5 Mobile

Diogo Beato - Engenheiro de Software

Atualmente compondo o time da Bluesoft, atuando em soluções de arquitetura e desenvolvimento do modulo financeiro do BluesoftERP.

**Perguntas para entender o público**
* Quem já trabalha na área?
* Quem trabalha com mobile?

## Pessoas e dispositivos móveis
Cada vez mais pessoas estão conectadas à internet através dos dispositivos mobile e cada vez é maior a variedade desses dispositivos, smartphones, tablets: Android, iOS, Windows Phone, FirefoxOS e outros.

Convencido desse nicho e querendo levar seu produto para todas essas plataformas você decide ataca-lo

## primeira decisao, web ou app?
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

mobile especifico x web responsivo
pro usuario é irrelevante, é uma decisao mais tecnica.

porém uma coisa importante é ter em mente as diferenças de usabilidade de mobile pra desktop.
mobile nao tem title. Não tem mouse:hover
Recomendação do google é utilizar design responsivo ao invés de um site especifico. 
Inclusive recentemente o google alterou seu algoritimo de indexação nas buscas pra aumentar drasticamente a relevancia dos sites que são user friendly a dispositivos mobiles.

Então, nos dias de hoje sempre que vc for desenvolver um site ou uma applicação web, comece pelos principios do mobile first.

Certo, mas o que isso quer dizer, como isso funciona na prática.
Mostrar ferramentas de desenvolvimento do google chrome, 
mostrar o livereload e principais frameworks para facilitar no desenvolvimento(bootstrap, foundation, etc)

O diferencial do html5
pergunta: Alguem sabe dizer qual é o maior diferencial que o html5 trouxe?
Antigamente, quando queriamos desenvolver um software que precissasse de acesso direto ao hardware (Vai usar a camera, vai usar a GPU para Aceleração Grafica, vai fazer um player de audio), não tinha nem o que pensar, tem que ser nativo (Java, C++, C#, Ruby, etc). 

O grande diferencia do HTML5 é exatamente isso, atravéz da sua API a gente começa a ter acesso a funcionalidades de alguns hardwares que antes só podiam estar presentes na web utilizando plugins como flash ou java applets.
Hoje com um browser e conhecimento de javascript vc consegue fazer vários experimentos legais utilizando o hardware do seu computador sem precisar de plugins.

Muito lindo na teoria, mas "show me the code".
mostrar APIs de camera, som, canvas, GPS, etc.

Mas a sua ideia não é web, vc quer lançar um applicativo mesmo, quer que as pessoas façam download do seu applicativo na apple store, na play store.

Os principais players do mercado mobile hoje em dia são o Android, iPhone e Windows Phone(nem tanto).

Android utiliza java como linguagem base, o iPhone utiliza ObjectiveC/Swift e o Windows Phone utiliza C#.

O que torna algumas vezes inviável manter um time especialista em cada plataforma. 

Que é o nosso caso na Bluesoft e em muitas outras empresas.
Nossos principais produtos são feitos com Java, Groovy e Ruby. Então, como podemos resolver isso?

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
