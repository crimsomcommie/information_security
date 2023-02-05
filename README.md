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
Damos nossas fotos (Facebook, Instagram, Google Photos), nossos interesses (Pesquisas Google, Bing), localização
(Google Maps, Uber) nome, celular e até mesmo CPF e moradia. Apesar de ser necessário compartilhar algumas dessas
informações em alguns momentos, é preciso frisar que nem sempre é necessário compartilhar essas informações e,
quando for, por vezes é possível dar informações falsas.

Para fotos, podemos não fazes backups automáticos para a cloud ou compartilhá-las no Instagram, Facebook e WhatsApp
(mesmo que sejam por mensagens diretas). Se for desejável o backup de fotos que se deseja manter anônima, é possível
passa-las para um ou mais computadores, de forma a se manter anonimato. É possível também agrupar um conjunto de fotos em 
um arquivo protegido com senha (e.g. um arquivo `.zip`) e colocar o arquivo em nuvem ou computador pessoal.

Para localização, mantenha o GPS desligado e não dê acesso à apps que não necessitam de GPS, como Instagram. Se for
procurar um local ou uma rota para chegar em um lugar específico, utilize serviços como [DuckDuckGo](https://duckduckgo.com/) 
ao invés do Google. Por vezes é possível também colocar em aplicativos como Uber como ponto final algum lugar perto do que realmente
deseja ir (e.g. colocar o endereço de uma loja que fica perto de onde você realmente vai).

Ao se compartilhar nome e CPF, veja se é realmente necessário de se utilizar seu nome e CPF real. Caso não seja, 
utilize um nome falso qualquer e use um [gerador de CPF](https://www.4devs.com.br/gerador_de_cpf). É possível também criar
endereços de [email temporários](https://temp-mail.org/pt/) ([segunda opção](https://www.guerrillamail.com/pt/)) para sites que cobram email. Se for necessário informar a moradia,
pesquise o endereço de uma loja qualquer (preferencialmente uma longe de você) e use-a.


### Sistema de Criação de Senhas
É importante utilizar senhas fortes e ter múltiplas senhas para sites diferentes. Procure não utilizar em senhas informações pessoais, como nome de mãe, filho, data de aniversário, comida favorita, etc. Algumas dicas para se utilizar senhas fortes são:
- Evite utilizar palavras reais;
- Não coloque seu usuário na senha;
- Utilize pelo menos 8 caracteres (senhas maiores são desejáveis);
- utilize letras maiúsculas, minúsculas, números e símbolos especiais (e.g. `@`, `$`);

Note que senhas longas por si só não lhe dão segurança. Senhas que são frases longas, mesmo que sem sentido(ou seja, uma sequência de palavras), podem ser facilmente descobertas por técnicas básicas de descobrimento de senha; alguns sites também podem não guardar a senha inteira(e.g. Hotmail até 2012), fazendo uma longa sequencia de palavras ser inútil.

O uso de sistemas de gerenciamento de senhas é recomendável pois eles podem criar e salvar senhas fortes facilmente (Para computadores (Windows, Linux Mac): (KeePassXC)[https://keepassxc.org/docs/KeePassXC_GettingStarted.html]; Celulares: LessPass ((Android)[https://play.google.com/store/apps/details?id=com.lesspass.android&hl=en&gl=US], (iOS)[https://apps.apple.com/us/app/lesspass/id1531215924])). Lembre de utilizar uma senha forte para acessar seu gerenciador de senhas. 

Navegadores como Chrome e Firefox já sugerem senhas ao entrar em páginas de sign up e salvar seus dados de log-in, porém um gerenciador externo é preferível. Ver [Navegadores](##Navegadores-Padrões) para decidir qual navegador utilizar.

Caso opte por não utilizar um gerenciador, verifique se sua senha é forte antes de usar (aqui)[https://passwordsecurity.info/].

Lembre de nunca copiar e colar (ctr+c, ctr+v) sua senha em qualquer computador!


#### Verificação em Duas Etapas
Diversos sites atualmente possuem verificação por duas etapas, isso é, para realizar login em um máquina desconhecida, é necessário que o usuário aceite o login por outro meio. A forma de se aceitar varia, podendo ser inserindo um código enviado por email ou SMS na tela de login, ou aceitando o dispositivo novo em outro já conhecido. Recomenda-se sempre utilizar a verificação em duas etapas, pois ela fortalece a segurança contra indivíduos desconhecidos que tenham conseguido sua senha de um site ou aplicativo.


### Utilização de Emails
É recomendável utilizar múltiplos emails com diferentes objetivos. Não apenas você pode ser monitorado e identificado através do uso de seu email, suponha que um site com seu email pessoal seja hackeado e sua senha nesse site descoberto. Caso utilize o mesmo email e senha em outros sites, quem tiver descoberto a senha agora tem acesso à sua conta de diferentes sites (e no pior dos casos de seu email principal). Use, por exemplo, em conjunto de seu email pessoal um email para compras (e.g. `jo.soares@gmail.com`), redes sociais (`bruno.mars@gmail.com`), etc.

Nota sobre GMail: como o GMail está atrelado a uma conta do Google, se você logar no seu gmail suas pesquisas serão, por padrão, salvas pela google, independentemente de qual máquina você estiver utilizando para fazer a pesquisa.


### Fotos e Geolocalização
Fotos contém diversas meta-informações (informações sobre a foto) entre elas: modelo da câmera, coordenadas GPS de onde foi a foto foi tirada, nome do proprietário, comentários, áudio incorporado, data em que foto foi tirada, descrição, palavras-chave. Isso significa que uma mera foto pode dar informações de onde você está e quem você é mesmo sem nada de relevante aparecer na imagem. Limpar esses dados é relativamente simples. No Windows, ao clicar em `Propriedades` -> `Detalhes` -> `Remove Propriedades e Informações Pessoais` é possível remover esses meta-dados.

Pode-se também utilizar [serviços onlines](https://www.imgonline.com.ua/eng/delete-exif.php) para deletar esses meta-dados ou aplicativos na app/play store.


## Navegando de Forma Anônima

### Search Engines

### Navegadores Padrões

### Tor


## Trocando Mensagens de Forma Anônima

### Criptografia

### O que é Peer 2 Peer

### Aplicativos Seguros


## Ações Avançadas de Segurança

### Criando um Proxy


## Resources 
(Password security and a comparison of Password Managers)[https://ss64.com/docs/security.html]
(Validador de força de senha)[https://passwordsecurity.info/]
(Have I been pwned)[https://haveibeenpwned.com/]
