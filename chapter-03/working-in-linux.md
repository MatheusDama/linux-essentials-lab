
# Descrição Simples

>The command line interface (CLI) is a simple text input system for entering anything from single-word commands to complicated scripts. Most operating systems have a CLI that provides a direct way of accessing and controlling the computer.

### 3.2 Applications

> "_The The **kernel**[^1] of the operating system is like an air traffic controller at an airport, and the applications are the airplanes under its control. **The kernel decides which program gets which blocks of memory**, it starts and kills applications, and it handles displaying text or graphics on a monitor.  of the operating system is like an air traffic controller at an airport, and the applications are the airplanes under its control. The **kernel** decides which program gets which blocks of memory, it starts and kills applications, and it handles displaying text or graphics on a monitor._"

> "_When we, as users, think of applications, we tend to think of word processors, web browsers, and email clients, however, there are a large variety of application types. The kernel doesn’t differentiate between a user-facing application, a network service that talks to a remote computer, or an internal task. From this, we get an abstraction called a process. A process is just one task that is loaded and tracked by the kernel. An application may even need multiple processes to function, so the kernel takes care of running the processes, starting and stopping them as requested, and handing out system resources._"

### 3.2.1

**Linux Software** normalmente caêm em uma das três categorias:

Uma **Aplicação de Servidor** (Server Application) é um programa projetado para executar em segundo plano, sem a necessidade de interação direta com periféricos locais (como monitor, teclado ou mouse) da máquina hospedeira. 

* **Propósito Principal:** Processar e servir informações para outros computadores ou sistemas na rede, conhecidos como **Clients** (Clientes).
* **Processamento Assíncrono/Background:** Em alguns cenários, essas aplicações não se comunicam diretamente com outros computadores. Em vez disso, atuam em segundo plano como serviços de suporte, consumindo, processando e armazenando dados de forma automatizada (como *background jobs*).

A **Aplicações Desktop** referem-se a softwares instalados localmente no sistema operacional do usuário, como navegadores web, editores de texto e players de música, com os quais há interação direta.

* **Propósito Principal:** Atuar como a interface final que consome dados de *Server Applications* (Aplicações de Servidor). É o ponto de chegada do fluxo de dados, renderizando páginas web, processando downloads ou exibindo informações ao usuário.
* **Arquitetura (Client/Server):** Funciona essencialmente como o **Cliente (*Client*)** — a entidade final e visual na arquitetura cliente/servidor, responsável por solicitar e apresentar os dados.

Definida como **Ferramenta** (_Tools_) tem-se como uma categoria vaga de programas que fazem o manuseio do computador mais fácil

### 3.2.2.1 **Web Server** (Servidores Web)

### Resumo: Servidores Web no Linux

Um dos primeiros usos do Linux foi para **servidores web**, que hospedam conteúdos de páginas web visualizadas por navegadores através dos protocolos **HTTP** ou **HTTPS** (sua versão criptografada).

#### Tipos de Páginas Web
* **Estáticas:** O servidor envia o arquivo exatamente como ele está salvo no disco.
* **Dinâmicas:** A requisição é enviada pelo servidor para uma aplicação que gera o conteúdo em tempo real (ex: **WordPress**, onde os usuários criam conteúdo pelo navegador e o sistema gera um site dinâmico funcional).

#### Principais Servidores Web
* **Apache (Apache HTTPD):** É o servidor dominante hoje. Mantido pela *Apache Software Foundation*, o `httpd` é o daemon (programa de servidor) que processa as requisições.
* **NGINX:** Focado em alta performance, utiliza kernels UNIX mais modernos e realiza um subconjunto menor de funções que o Apache.

> 💡 Juntos, **Apache e NGINX movem mais de 65% de todos os sites da internet**.

### 3.2.2.2 **Private Clound Servers** (Servidores Nuvem Privados)

### Resumo: Nuvem Privada (ownCloud e Nextcloud)

Com a migração de dados para a nuvem por indivíduos e empresas, cresceu a demanda por softwares de **nuvem privada** que possam ser implantados e gerenciados internamente. 

#### Principais Projetos
* **ownCloud:** Lançado em 2010 por Frank Karlitschek para armazenar, sincronizar e compartilhar dados. Possui uma versão de código aberto (licença GNU AGPLv3) e uma versão comercial para empresas.
* **Nextcloud:** Criado em 2016 por Karlitschek como um *fork* (bifurcação) do ownCloud. É totalmente gratuito (GNU AGPLv3) e focado em um processo de desenvolvimento aberto e transparente.

#### Objetivos Comuns
* Foco em segurança, privacidade e conformidade regulatória.
* Atendem desde pequenas a grandes organizações.

> 📊 Embora existam outras alternativas no mercado, o **ownCloud e o Nextcloud são os maiores projetos desse ecossistema**, tanto em volume de implantação quanto em número de membros na comunidade.

### 3.2.2.4 **Email Servers**

### Resumo: Servidores de e-mail (MTA, MDA, POP)

--EXPLICAR--

#### Projetos difundidos na comunidade

* **Mail Trasfer Agent(MTA):** O mais conhecido MTA (transferência por mensagem eletronica para outros sistemas) é o **Sendmail** e **Postfix**.
* **Mail Delivert Agent(MDA)**

### --- DEFINIÇÕES MENTAIS ---

> [^1] **Kernel**
