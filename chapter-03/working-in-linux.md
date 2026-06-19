
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

* T
  

### --- DEFINIÇÕES MENTAIS ---

> [^1] **Kernel**
