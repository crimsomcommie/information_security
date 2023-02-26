# Segurança da Informação
Este documento tem como objetivo demonstrar formas de se comunicar e navegar pela internet de forma anônima
bem como explicar conceitos básicos de segurança. Vale notar que há uma troca entre conveniência e segurança,
sendo as ações mais convenientes normalmente as menos seguras. Apesar disso, algumas ações e hábitos
extremamente simples podem trazer um grande aumento segurança digital.
O texto é dividido da seguinte forma:

Primeiro explicamos ações básicas para se manter anônimo em sites, como não compartilhar informações
pessoais, criação de emails e como criar e utilizar boas senhas. Explicamos também algumas das formas
que empresas coletam dados pessoais.

Na segunda seção, explicamos sobre como navegar na internet de forma anônima, discutimos sobre navegadores
e introduzimos o Tor.

Na terceira seção damos noções mais avançadas de segurança, explicamos proxies e como podemos criar um para 
nos manter em anonimato.


## Ações Básicas de Anonimato
Nessa seção iremos explicar como tomar ações básicas para se manter anônimo. Explicaremos também
diferentes formas que empresas podem rastrear e coletar dados de alguém.

### Escondendo Informações pessoais
Ao utilizar diversos serviços de grandes aplicações normalmente damos uma variedade de informações pessoais.
Damos nossas fotos (Facebook, Instagram, Google Photos), nossos interesses (Pesquisas Google, Bing), localização (Google Maps, Uber) nome, celular e até mesmo CPF e moradia. Apesar de ser necessário compartilhar algumas dessas informações em alguns momentos, é preciso frisar que nem sempre é necessário compartilhar essas informações e, quando for, por vezes é possível dar informações falsas.

Para fotos, podemos não fazes backups automáticos para a cloud ou compartilhá-las no Instagram, Facebook e WhatsApp (mesmo que sejam por mensagens diretas). Se for desejável o backup de fotos que se deseja manter anônima, é possível passa-las para um ou mais computadores, de forma a se manter anonimato. É possível também agrupar um conjunto de fotos em  um arquivo protegido com senha (e.g. um arquivo `.zip`) e colocar o arquivo em nuvem ou computador pessoal.

Para localização, mantenha o GPS desligado e não dê acesso à apps que não necessitam de GPS, como Instagram. Se for procurar um local ou uma rota para chegar em um lugar específico, utilize serviços como [Searx](https://searx.thegpm.org/) ao invés do Google. Por vezes é possível também colocar em aplicativos como Uber como ponto final algum lugar perto do que realmente deseja ir (e.g. colocar o endereço de uma loja que fica perto de onde você realmente vai).

Ao se compartilhar nome e CPF, veja se é realmente necessário de se utilizar seu nome e CPF real. Caso não seja, utilize um nome falso qualquer e use um [gerador de CPF](https://www.4devs.com.br/gerador_de_cpf). É possível também criar endereços de [email temporários](https://temp-mail.org/pt/) ([segunda opção](https://www.guerrillamail.com/pt/)) para sites que cobram email. Se for necessário informar a moradia,
pesquise o endereço de uma loja qualquer (preferencialmente uma longe de você) e use-a.


### Sistema de Criação de Senhas
É importante utilizar senhas fortes e ter múltiplas senhas para sites diferentes. Procure não utilizar em senhas informações pessoais, como nome de mãe, filho, data de aniversário, comida favorita, etc. Algumas dicas para se utilizar senhas fortes são:
- Evite utilizar palavras reais;
- Não coloque seu usuário na senha;
- Utilize pelo menos 8 caracteres (senhas maiores são desejáveis);
- utilize letras maiúsculas, minúsculas, números e símbolos especiais (e.g. `@`, `$`);

Note que senhas longas por si só não lhe dão segurança. Senhas que são frases longas, mesmo que sem sentido(ou seja, uma sequência de palavras), podem ser facilmente descobertas por técnicas básicas de descobrimento de senha; alguns sites também podem não guardar a senha inteira(e.g. Hotmail até 2012), fazendo uma longa sequencia de palavras ser inútil.

O uso de sistemas de gerenciamento de senhas é recomendável pois eles podem criar e salvar senhas fortes facilmente (Para computadores (Windows, Linux Mac): [KeePassXC](https://keepassxc.org/docs/KeePassXC_GettingStarted.html); Celulares: LessPass ([Android](https://play.google.com/store/apps/details?id=com.lesspass.android&hl=en&gl=US), [iOS](https://apps.apple.com/us/app/lesspass/id1531215924))). Lembre de utilizar uma senha forte para acessar seu gerenciador de senhas. 

Navegadores como Chrome e Firefox já sugerem senhas ao entrar em páginas de sign up e salvar seus dados de log-in, porém um gerenciador externo é preferível. Ver [Navegadores](##Navegadores-Padrões) para decidir qual navegador utilizar.

Caso opte por não utilizar um gerenciador, verifique se sua senha é forte antes de usar [aqui](https://passwordsecurity.info/).

Lembre de nunca copiar e colar (ctr+c, ctr+v) sua senha em qualquer computador!


#### Verificação em Duas Etapas
Diversos sites atualmente possuem verificação por duas etapas, isso é, para realizar login em um máquina desconhecida, é necessário que o usuário aceite o login por outro meio. A forma de se aceitar varia, podendo ser inserindo um código enviado por email ou SMS na tela de login, ou aceitando o dispositivo novo em outro já conhecido. Recomenda-se sempre utilizar a verificação em duas etapas, pois ela fortalece a segurança contra indivíduos desconhecidos que tenham conseguido sua senha de um site ou aplicativo.


### Utilização de Emails
É recomendável utilizar múltiplos emails com diferentes objetivos. Não apenas você pode ser monitorado e identificado através do uso de seu email, suponha que um site com seu email pessoal seja hackeado e sua senha nesse site descoberto. Caso utilize o mesmo email e senha em outros sites, quem tiver descoberto a senha agora tem acesso à sua conta de diferentes sites (e no pior dos casos de seu email principal). Use, por exemplo, em conjunto de seu email pessoal um email para compras (e.g. `jo.soares@gmail.com`), redes sociais (`bruno.mars@gmail.com`), etc.

Nota sobre GMail: como o GMail está atrelado a uma conta do Google, se você logar no seu gmail suas pesquisas serão, por padrão, salvas pela google, independentemente de qual máquina você estiver utilizando para fazer a pesquisa.


### Fotos e Capturas de Tela
Imagens contém diversas meta-informações (informações sobre a imagem), valendo para fotos, capturas de tela e imagens feitas por aplicativos (e.g. Photoshot) entre elas: modelo da câmera, coordenadas GPS de onde foi a imagem foi tirada, nome do proprietário, comentários, áudio incorporado, data, descrição, palavras-chave. Isso significa que uma mera imagem pode dar informações de onde você está e quem você é mesmo sem nada de relevante aparecer na imagem. Limpar esses dados é relativamente simples. No Windows, ao clicar em `Propriedades` -> `Detalhes` -> `Remove Propriedades e Informações Pessoais` é possível remover esses meta-dados.

Pode-se também utilizar [serviços onlines](https://www.imgonline.com.ua/eng/delete-exif.php) para deletar esses meta-dados ou aplicativos na app/play store.


### Windows e outros Sistemas Operacionais
O Windows coleta e compartilha seus dados desde o momento em que ele é ligado. Informações como o que se é digitado, histórico de pesquisa no Bing e Edge, quais aplicativos estão sendo utilizados em que horários, especificações do computador (memória, CPU, etc), dados da rede entre muitos outros são enviados para a Microsoft e para terceiros. 

Não existe uma opção real para evitar essa coleta de dados realizada pela Microsoft além de se parar de utilizar o Windows, utilizar versões mais antigas (e.g. Windows XP) ou então tentam baixar versões hackeadas do Windows que clamam terem retirado a telemetria do sistema operacional.

Quem não necessitar de aplicativos exclusivos de Windows para trabalhar pode tentar migrar para uma distribuição linux, como [Ubuntu](https://ubuntu.com/) ou [Linux Mint](https://linuxmint.com/), que fornecem total controle ao usuário sobre o sistema operacional.


## Navegando de Forma Anônima
Para navegar de forma anônima precisamos de um navegador e mecanismo de busca voltados para segurança e privacidade. Nesta seção iremos comentar sobre os sistemas mais utilizados e as melhores opições visando o anonimato.

### Search Engines
Google e Bing são os mecanismos de busca mais utilizados. Por serem de grandes empresas, os dados de usuário podem ser compartilhados com governos e vendidos para terceiros. Esses mecanismos também podem rastrear o usuário em diferentes máquinas, seja por ter uma conta atrelada o por padrões de uso. O DuckDuckGo é uma pseudo-alternativa popular, porém este contém acordos com a Microsoft de forma a permitir rastreadores na busca. É importante notar também que o DuckDuckGo, por trás dos panos, utiliza o Bing como motor de busca para obter seus resultados.

Uma real alternativa visando a segurança é o [Searx](https://searx.thegpm.org/). Ao invés de coletar resultados de pesquisa de uma fonte única, como o Google, o Searx agrega resultados de vários motores de busca diferentes, selecionados pelo usuário, e os apresenta em uma única página. O Searx não salva histórico de pesquisa e não repassa ou mesmo vende os dados de uso para terceiros. Seu código também é aberto, ou seja, qualquer um pode contribuir com o projeto e verificar o código que está rodando.


### Navegadores Padrões
Por padrão, os navegadores mais comuns permitem o fácil rastreamento de seus usuários, seja por propagandas ou outros rastreadores. É recomendável utilizar o UBlock ([Firefox](https://addons.mozilla.org/pt-BR/firefox/addon/ublock-origin/), [Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm?hl=pt-BR)) para bloquear anúncios e rastreadores. Estes também podem proteger o usuário avisando sobre sites possivelmente nocivos. Estes bloqueadores funcionam de forma que URLs com objetivo de expor propagandas ou rastrear o usuário são barradas antes que o navegador possa acessá-las.

O Chromium e seus derivados (Chrome, Edge, Opera, etc) limitam o uso de bloqueadores de propagandas e rastreamento (lembrando que os programadores do Chromium são da Google, empresa que mais lucra com anúncios e rastreamento de usuário). Portanto, é recomendado utilizar o Firefox, que oferece suporte pleno à tecnologias de bloqueio de anúncios.

Também é possível de se rastrear alguém utilizando JavaScript, uma linguagem de programação utilizada por sites para trazer interatividade. Desligando o interpretador de JavaScript de seu navegador pode-se obter ainda mais anonimato, porém algumas páginas da web podem parar de funcionar por depender fortemente da linguagem. Desligando o JavaScript também é possível burlar alguns dos detectores de bloqueadores de anúncios de funcionar.


### Tor
O [Tor](https://www.torproject.org/download/) (The Onion Router) é um navegador de internet anônimo que permite que os usuários naveguem na web de forma privada e segura. O Tor funciona criptografando os dados do usuário e encaminhando-os através de uma série de roteadores (ou nós) distribuídos pelo mundo (é feita uma analogia onde cada roteador é uma camada de uma cebola, ou `onion`), antes de chegar ao seu destino final na web. Isso torna muito difícil para qualquer pessoa rastrear a origem ou o destino da comunicação. 

Além de proteger a privacidade e segurança dos usuários, o Tor também permite que eles acessem conteúdo da web que possa estar bloqueado em sua localização geográfica e acessar URLs `.onion`. URLs `.onion` são acessíveis por meio da rede Tor, sendo acessíveis por navegadores comuns apenas através de extensões que permitam se comunicar com a rede Onion.

O uso do Tor torna mais difícil rastrear a atividade de um usuário na Internet. O uso pretendido do Tor é proteger a privacidade pessoal de seus usuários, bem como sua liberdade e capacidade de se comunicar confidencialmente por meio de endereços IP anônimos usando os nós de saída do Tor.

É importante notar que mesmo com o Tor ainda é possível ser rastreado, seja por acessar sites não seguros ou fora da rede Tor que utilizam JavaScript, ou caso o nó de saída utilizado esteja compromissado. É importante notar que o Tor não esconde seu uso, isso é, o provedor de um site sabe quando um usuário está se conectando utilizando o Tor, apesar de não saber quem é este é. Alguns sites chegam a bloquear o acesso de usuários utilizando o Tor.


## Trocando Mensagens de Forma Anônima
Todos os aplicativos de mensagens mais utilizados criptografam suas mensagens para evitar que elas sejam lidas por terceiros. O problema destes aplicativos é que informações de um usuário para outro são guardados em servidores centralizados e essas informações podem ser compartilhadas ou vazadas para terceiros. Algumas das informações armazenadas são dados de quando uma mensagem foi enviada, seu IP, número de telefone, nome, dentre outros. Essas informações podem revelar com quem se está conversando, onde se está, dentre outros. É recomendável utilizar programas de mensagem que coletam o mínimo de informações possíveis de seus usuários como Signal([Google Play](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms), [App Store](https://apps.apple.com/us/app/signal-private-messenger/id874139669)) e Tox ([Google Play](https://play.google.com/store/apps/details?id=ltd.evilcorp.atox)).


### Criptografia
A criptografia é uma técnica usada para proteger informações confidenciais, tornando-as inacessíveis para terceiros que não possuem a chave para decifrá-las. Ela é usada para garantir a segurança e a privacidade das comunicações e das transações eletrônicas.

A criptografia pode ser aplicada de várias maneiras, mas geralmente envolve o processo de codificar uma mensagem ou dados com uma chave, transformando-os em um formato ilegível e, em seguida, enviar essa mensagem ou dados para o destinatário. O destinatário, por sua vez, usa a chave correspondente para decodificar a mensagem ou dados e recuperar a informação original.

Os algoritmos atuais são robustos o suficiente de forma que as mensagens criptografadas dos aplicativos de mensagens não podem ser descobertas nem mesmo pelas próprias empresas dos aplicativos caso elas não tenham a chave utilizada para decodificar a mensagem. 


### O que é Peer 2 Peer
Peer-to-peer (P2P) é um modelo de comunicação de rede em que os computadores ou dispositivos conectados em uma rede compartilham diretamente recursos, como arquivos, aplicativos, dados ou processamento, sem estes passarem por de um servidor central.

No modelo tradicional de cliente-servidor, um servidor centralizado é usado para gerenciar a rede e distribuir recursos. Isso significa que um cliente precisa se comunicar com o servidor para obter recursos ou informações. No modelo P2P, cada nó na rede tem a capacidade de compartilhar e acessar recursos diretamente de outros nós na rede, sem a necessidade de um servidor central.

A comunicação P2P geralmente ocorre em redes descentralizadas, em que não há um único ponto de controle ou autoridade, evitando que uma entidade central tenha todos os dados de seus usuários. O Signal utiliza de comunicação P2P para chamadas de voz e de vídeo entre pessoas que tenham seus contatos, porém as mensagens passam por um servidor central. O Tox não contém ums servidor central e portanto não guarda dados de seus usuários.


## Engenharia Social e Segurança
Engenharia social é uma técnica de manipulação psicológica que é usada para obter informações confidenciais ou fazer com que as pessoas tomem decisões indevidas. É uma forma de exploração que se aproveita das vulnerabilidades humanas, como a confiança, a boa fé e a ignorância, para obter informações ou realizar ações maliciosas. Essa é a principal forma de ataque para se obter informações de terceiros e como a maioria dos hacks a grandes empresas acontecem, por ser mais fácil e eficaz enganar alguém do que quebrar a proteção digital atual.

A engenharia social pode ser realizada através de vários meios, como e-mails, mensagens instantâneas, telefonemas, publicidade enganosa e outros. Por exemplo, um atacante pode se fazer passar por alguém de confiança, como um funcionário de uma empresa ou um amigo, e pedir informações confidenciais ou fazer com que a pessoa clique em um link malicioso.

Por isso, é importante estar ciente das técnicas de engenharia social e estar preparado para reconhecê-las e proteger-se contra elas. É recomendável não compartilhar informações confidenciais com desconhecidos e ser cauteloso ao clicar em links suspeitos. Além disso, é importante manter software de segurança atualizado e ter cuidado com mensagens suspeitas que possam ser parte de uma tentativa de engenharia social.

Também é importante não ter informações confidenciais não criptografadas (sejam documentos digitais ou documentos físicos, como textos em folhas de papel), de forma que mesmo tendo acesso à informação outros não consigam ter acesso aos dados reais. Por exemplo, não há motivos para um atacante tentar hackear um celular ou email se ele puder obter uma informação confidencial através de roubo ou furto de um caderno ou celular.


## Proteção Física
É importante notar que a segurança digital anda de mãos dadas com a segurança física e pessoal. De nada adianta utilizar uma senha forte se ela estiver escrita em um caderno que poderia ser facilmente roubado por terceiros. Nada impede também de uma pessoa mal intencionada de se utilizar de violência para obter informações confidenciais diretamente de uma pessoa. Portanto, além de adotar medidas de segurança digital é importante se proteger também no mundo físico em que vivemos para mantermos nossas informações pessoais sigilosas.


## Resources 
[Password security and a comparison of Password Managers](https://ss64.com/docs/security.html)

[Validador de força de senha](https://passwordsecurity.info/)

[Have I been pwned](https://haveibeenpwned.com/)

[Gerador de CPF](https://www.4devs.com.br/gerador_de_cpf)

[Gerador de emails Temporários](https://temp-mail.org/pt/) ([segunda opção](https://www.guerrillamail.com/pt/))

### Apps
[Signal](https://signal.org/pt_BR/)

[Tox](https://tox.chat/)

[KeePassXC](https://keepassxc.org/docs/KeePassXC_GettingStarted.html)

LessPass ([Android](https://play.google.com/store/apps/details?id=com.lesspass.android&hl=en&gl=US), [iOS](https://apps.apple.com/us/app/lesspass/id1531215924))

[Tor](https://www.torproject.org/download/)


### Motores de Busca
[Searx](https://searx.thegpm.org/)


### Sistemas Operacionais
[Ubuntu](https://ubuntu.com/) 

[Linux Mint](https://linuxmint.com/)
