# Descrição Simples

> The command line interface (CLI)[^2] is a simple text input system for entering anything from single-word commands to complicated scripts. Most operating systems have a CLI that provides a direct way of accessing and controlling the computer.

## 3.2 Applications

> "_The kernel[^1] of the operating system is like an air traffic controller at an airport, and the applications are the airplanes under its control. **The kernel decides which program gets which blocks of memory**, it starts and kills applications, and it handles displaying text or graphics on a monitor._"

> "_When we, as users, think of applications, we tend to think of word processors, web browsers, and email clients, however, there are a large variety of application types. The kernel doesn’t differentiate between a user-facing application, a network service that talks to a remote computer, or an internal task. From this, we get an abstraction called a process[^3]. A process is just one task that is loaded and tracked by the kernel. An application may even need multiple processes to function, so the kernel takes care of running the processes, starting and stopping them as requested, and handing out system resources._"

---

### 3.2.1 Categorias de Software no Linux

O **Linux Software** normalmente cai em uma das três categorias:

1. **Aplicação de Servidor (Server Application):** É um programa projetado para executar em segundo plano (*background*), sem a necessidade de interação direta com periféricos locais (como monitor, teclado ou mouse) da máquina hospedeira.
   * **Propósito Principal:** Processar e servir informações para outros computadores ou sistemas na rede, conhecidos como **Clients** (Clientes).
   * **Processamento Assíncrono/Background:** Em alguns cenários, essas aplicações não se comunicam diretamente com outros computadores. Em vez disso, atuam em segundo plano como serviços de suporte, consumindo, processando e armazenando dados de forma automatizada (como *background jobs*).

2. **Aplicações Desktop:** Referem-se a softwares instalados localmente no sistema operacional do usuário, como navegadores web, editores de texto e players de música, com os quais há interação direta.
   * **Propósito Principal:** Atuar como a interface final que consome dados de *Server Applications*. É o ponto de chegada do fluxo de dados, renderizando páginas web, processando downloads ou exibindo informações ao usuário.
   * **Arquitetura (Client/Server):** Funciona essencialmente como o **Cliente (*Client*)** — a entidade final e visual na arquitetura cliente/servidor, responsável por solicitar e apresentar os dados.

3. **Ferramentas (Tools):** Definida como uma categoria abrangente de programas focados em utilitários, scripts e comandos que tornam o gerenciamento, a automação e o manuseio do computador mais fáceis para o usuário ou administrador.

---

## 3.2.2 Serviços de Infraestrutura de Rede

### 3.2.2.1 Web Server (Servidores Web)

Um dos primeiros usos do Linux foi para **servidores web**, que hospedam conteúdos de páginas web visualizadas por navegadores através dos protocolos **HTTP** ou **HTTPS**[^4] (sua versão criptografada).

#### Tipos de Páginas Web
* **Estáticas:** O servidor envia o arquivo exatamente como ele está salvo no disco.
* **Dinâmicas:** A requisição é enviada pelo servidor para uma aplicação que gera o conteúdo em tempo real (ex: **WordPress**, onde os usuários criam conteúdo pelo navegador e o sistema gera um site dinâmico funcional).

#### Principais Servidores Web
* **Apache (Apache HTTPD):** É o servidor dominante historicamente. Mantido pela *Apache Software Foundation*, o `httpd` é o daemon[^5] (programa de servidor) que processa as requisições.
* **NGINX:** Focado em alta performance e concorrência, utiliza kernels UNIX mais modernos e realiza um subconjunto menor e mais otimizado de funções que o Apache.

> 💡 Juntos, **Apache e NGINX movem mais de 65% de todos os sites da internet**.

*🧠 **Definição Mental:** **Web Server = O Garçom de Páginas.** O navegador (cliente) pede um prato (URL/página) e o servidor web vai até a cozinha (disco/banco de dados) para entregar o arquivo pronto na mesa do usuário.*

---

### 3.2.2.2 Private Cloud Servers (Servidores de Nuvem Privada)

Com a migração de dados para a nuvem por indivíduos e empresas, cresceu a demanda por softwares de **nuvem privada** que possam ser implantados, hospedados e gerenciados internamente na infraestrutura da própria organização.

#### Principais Projetos
* **ownCloud:** Lançado em 2010 por Frank Karlitschek para armazenar, sincronizar e compartilhar dados. Possui uma versão de código aberto (licença GNU AGPLv3) e uma versão comercial para empresas.
* **Nextcloud:** Criado em 2016 por Karlitschek como um *fork*[^6] (bifurcação) do ownCloud. É totalmente gratuito (GNU AGPLv3) e focado em um processo de desenvolvimento aberto, transparente e com mais recursos nativos de colaboração.

#### Objetivos Comuns
* Foco estrito em segurança, privacidade e conformidade regulatória (como LGPD/GDPR).
* Atendem desde usuários domésticos até grandes corporações.

> 📊 Embora existam outras alternativas no mercado, o **ownCloud e o Nextcloud são os maiores projetos desse ecossistema**, tanto em volume de implantação quanto em número de membros na comunidade.

*🧠 **Definição Mental:** **Nuvem Privada = O seu próprio Google Drive/Dropbox.** Em vez de confiar seus arquivos sensíveis a servidores de terceiros, você instala o Nextcloud em um servidor Linux próprio e mantém controle absoluto sobre o armazenamento dos dados.*

---

### 3.2.2.4 Email Servers (Servidores de E-mail)

A arquitetura de e-mail no Linux funciona como um sistema de correios tradicional digital, sendo dividida em componentes especializados que se comunicam para garantir o envio, transporte e recebimento das mensagens.


#### Projetos Difundidos na Comunidade

* **Mail Transfer Agent (MTA):** Responsável por transportar o e-mail de um servidor para outro através da internet usando o protocolo **SMTP**[^7]. Os MTAs mais conhecidos e consolidados no ecossistema Linux são o **Sendmail** e o **Postfix**.
* **Mail Delivery Agent (MDA) / Local Delivery Agent (LDA):** Responsável por receber a mensagem entregue pelo MTA no destino final e armazená-la com segurança na caixa de entrada específica do usuário no disco. Ele atua na ponta final da corrente de transmissão do servidor.
* **POP/IMAP Server:** Protocolos utilizados para permitir que um software de e-mail local do usuário (o cliente, como Outlook ou Thunderbird) se conecte ao servidor remoto para ler as mensagens armazenadas pelo MDA.
  * **POP3**[^8]: Baixa os e-mails do servidor para o computador local e, geralmente, remove-os do servidor remoto.
  * **IMAP**[^9]: Sincroniza e lê os e-mails diretamente no servidor, permitindo que as mensagens fiquem disponíveis em múltiplos dispositivos simultaneamente. Os servidores mais populares de POP/IMAP no Linux são o **Dovecot** e o **Courier**.

*🧠 **Definição Mental:** **Email Architecture = O Fluxo Postal.** O **MTA** é o caminhão dos correios que leva a carta entre cidades; o **MDA** é o carteiro que coloca a carta na sua caixa de correio física; e o **POP/IMAP** é você abrindo a portinha da caixa para pegar ou ler as cartas usando o seu celular/computador.*

---

### 3.2.2.5 File Sharing (Compartilhamento de Arquivos)

O Linux atua como um hub centralizado para fornecer ou consumir arquivos em redes heterogêneas, utilizando protocolos especializados para cada sistema operacional:

* **Samba:** O líder absoluto para redes baseadas em **Windows**. Ele faz com que uma máquina Linux se comporte como um servidor Windows, implementando papéis de servidor (compartilhamento de arquivos) e cliente, permitindo também a integração em domínios Active Directory.
* **Netatalk:** Projeto open-source que permite ao Linux atuar nativamente como um servidor de arquivos para ecossistemas **Apple Macintosh**.
* **Network File System (NFS):** O protocolo de compartilhamento nativo para ecossistemas **UNIX/Linux**. Por operar integrado diretamente ao kernel[^1], um sistema de arquivos remoto pode ser montado[^10] de forma transparente, comportando-se exatamente como se fosse um disco rígido local para as aplicações.

*🧠 **Definição Mental:** **File Sharing = O Armário Compartilhado Multiplataforma.** O Linux consegue falar com qualquer sistema na rede: ele usa o **Samba** para se disfarçar de Windows, o **Netatalk** para falar com Macs e o **NFS** para conversar nativamente com outros Linux de forma ultrarrápida.*

---

### 3.4.1 Debian Package Management (Manejamentos de Pacotes Debian)

Em distribuições derivadas do _debian_ como Ubuntu e Mint, usam o _Debian Package management system_. Sendo que no coração do **DPKG (Debian package management)** é destribuido como arquivo com terminações `.deb`.

A ferramenta de baixo-nível para lidar com esses arquivos é o comando `dpkg`. Podendo esse programa ser um pouco sorrateiro para novos usuário Linux, o **Advanced Package Tool (apt)**, `apt-get` (um programa front-end comparado a ferramenta `dpkg`), fazendo o manejamento de pacotes fácil. 

---

## 3.4 Package Management (Gerenciamento de Pacotes)

### 3.4.2 RPM Package Management

O gerenciamento de programas e a padronização de software no Linux são regulados e facilitados através de ecossistemas de pacotes dedicados:

* **Padrão de Mercado:** O projeto *Linux Standards Base (LSB)*[^14] define por consenso um conjunto de normas para aumentar a compatibilidade entre distribuições Linux. De acordo com o LSB, o sistema padrão oficial para o gerenciamento de pacotes é o **RPM** (utilizando arquivos com a extensão `.rpm`).
* **Distribuições que Utilizam:** É a base estrutural de distribuições derivadas da Red Hat (como **CentOS** e **Fedora**), mas também adotada por ecossistemas não derivados como **SUSE**, **openSUSE** e historicamente ligada a estruturas de compatibilidade como o **Arch**.
* **Rastreamento de Dependências:** Assim como o sistema Debian, o RPM rastreia dependências[^15] entre os pacotes. Isso garante de forma automatizada que, ao instalar um programa, todos os outros pacotes necessários para o seu funcionamento também sejam instalados, mantendo atualizações e remoções consistentes sem quebrar o sistema.
* **Ferramentas de Back-end vs Front-end:** * **Back-end (`rpm`):** A ferramenta base de baixo nível é o comando `rpm`. Ele é capaz de instalar, atualizar, consultar e remover pacotes diretamente, mas não resolve dependências sozinho.
  * **Front-end (`yum` / `up2date` / `dnf`):** Utilitários de alto nível de linha de comando que funcionam como fachadas automatizadas. Ferramentas como o `yum`[^16] e o moderno `dnf`[^17] resolvem de forma autônoma os problemas de dependências, buscando e baixando os pacotes complementares necessários da internet.

*🧠 **Definição Mental:** **Gerenciamento RPM = A App Store dos Servidores Red Hat.** O arquivo `.rpm` é como um instalador fechado (`.exe` ou `.msi` do Windows). O comando **`rpm`** é o instalador cru que descompacta os arquivos, enquanto o **`yum`/`dnf`** é o assistente inteligente que avisa: *"Para instalar esse programa, eu preciso baixar esses outros 3 antes automaticamente para você"*, evitando que você precise caçar os arquivos manualmente.*

---

### 3.5 Development Language (Linguagem de Desenvolvimento)


### Glossário Teórico e Notas de Rodapé

* **NOTA GERAL:**
* Ou o programa _back-end_ ou aplicação interagem ambas com o programa _front-end_, ou é "chamada" por um programa intermediário entre esses dois. Programas _back-end_ não irão interagir diretamente com o usuário.

[^1]: **Kernel:** O núcleo principal do sistema operacional. É a camada de software mais baixa que faz a ponte de comunicação direta entre o hardware do computador (processador, memória, discos) e os programas/aplicações que você executa.
[^2]: **CLI (Command Line Interface):** Interface de Linha de Comando. Um meio de interagir com o computador onde o usuário digita comandos de texto em vez de clicar em ícones visuais.
[^3]: **Processo:** Uma instância de um programa de computador que está sendo executada pelo Kernel. Ele possui seu próprio espaço de memória alocado e recursos atribuídos.
[^4]: **HTTP/HTTPS (Hypertext Transfer Protocol Secure):** Protocolos base da web para transferência de dados. O 'S' no final indica que os dados transmitidos são criptografados através de TLS/SSL para impedir interceptações de terceiros.
[^5]: **Daemon:** Um tipo de programa de sistema no Linux que roda silenciosamente em segundo plano (background) de forma persistente para atender a requisições de serviços (como o Apache respondendo a requisições de páginas web).
[^6]: **Fork (Bifurcação de Código):** Quando desenvolvedores pegam uma cópia de um código-fonte de um software de código aberto existente e iniciam um desenvolvimento independente a partir dele, criando um novo projeto com rumos diferentes (como o Nextcloud fez a partir do ownCloud).
[^7]: **SMTP (Simple Mail Transfer Protocol):** O protocolo padrão utilizado para o envio e transporte de mensagens de e-mail entre servidores através da internet.
[^8]: **POP3 (Post Office Protocol v3):** Protocolo clássico de recebimento de e-mails focado em baixar as mensagens do servidor para o armazenamento local do dispositivo do cliente, liberando espaço no servidor.
[^9]: **IMAP (Internet Message Access Protocol):** Protocolo moderno de recebimento de e-mails que mantém as mensagens guardadas no servidor central e apenas reflete a visualização delas nos dispositivos do usuário, permitindo sincronização em tempo real entre webmail, celular e computador.
[^10]: **Montar (Mounting):** O processo no Linux de anexar um sistema de arquivos externo ou remoto (como uma pasta compartilhada em outro servidor via NFS) a um diretório específico da árvore de arquivos local, tornando-o acessível.
[^11]: **BIND (Berkeley Internet Name Domain):** O software de servidor DNS mais utilizado na Internet, cujo nome do processo em execução no sistema operacional é tradicionalmente chamado de `named` ou `bind`.
[^12]: **OpenLDAP:** Uma implementação livre e de código aberto do protocolo LDAP, amplamente utilizada para gerenciar serviços de diretório centralizados em servidores Linux.
[^13]: **ISC DHCP Server:** Servidor DHCP open-source de referência mantido pela Internet Systems Consortium, utilizado para distribuição automatizada de parâmetros de rede em larga escala.
