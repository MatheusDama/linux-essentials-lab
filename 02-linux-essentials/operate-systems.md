### 2.1 **Sistema Operacional :** Um Programa que roda em um sistema de computador e controla os componentes de ***hardware*** e ***Software*** que fazem um sistema computacional funcional.

> Computer users today have a choice mainly between three major operating systems: Microsoft Windows, Apple macOS, and Linux.
>
> Of the three major operating systems listed only Microsoft Windows is unique in its underlying code. Apple’s macOS is a fully-qualified UNIX distribution based on BSD Unix (an operating system distributed until 1995), complemented by a large amount of proprietary code. It runs on hardware specifically optimized to work with Apple software. Linux can be any one of hundreds of distribution packages designed or optimized for whatever task is required. Only Microsoft Windows is based on a proprietary code base that isn’t either UNIX- or Linux-based.
>
> A user can easily interact with any of these systems by pointing and clicking their way through everyday productivity tasks that all behave similarly regardless of the underlying operating system. Except for Windows, which is mostly administered via the GUI, most system administration tasks are performed using typed commands in a terminal. An administrator that is familiar with UNIX can typically perform tasks on a Linux system and vice versa. Many Linux command line functions also have Microsoft equivalents that administrators use to do their work efficiently.

---

### 2.1.1 **Pontos de Decisão**

Role(função) - A função que específica de qualquer máquina
* Rodando aplicativos de produtividade ou navegação web? ***family desktop*** é para você
* A máquina será acessada remotamente por muitos usuários ou providênciando serviços para um usuário remoto? ** *server* **

Sendo o ** *Server* ** situado como um suporte interno, a qual divide-se entre vários usuários para os ademais necessidades de uma empresa, seu CLI é geralmente usado para configurações ou solução de problemas(troubleshooting). Geralmente rodando em **CLI**, retirando todas as propriedades de um **GUI**, para que economize em recursos para o propósitos reais desse computador: 

#### Function (propósito)

|---|

### Life Cycle (Ciclo de Vida)

>The service lifetime and risk tolerance of the server also needs to be determined. Operating systems and software upgrades come on a periodic basis, called a release cycle. Vendors only support older versions of software for a certain period of time before not offering any updates; this is called a maintenance cycle or life cycle.
>
>In an enterprise server environment, maintenance and release cycles are critical considerations because it is time-consuming and expensive to do major upgrades. Instead, the server hardware itself is often replaced because increased performance is worth the extra expense, and the resources involved are often many times more costly than the hardware.

### Estabilidade
* ***realese*** de programas podem ser definidos como ***beta*** ou ***stable*** dependendo do seu *release cycle*. - quando se tem muintas novas funções, sabe-se que nem tudo foi testado, referindo-se assim como ** *beta* **, e assim que testado em campo, definida como ** *stable* **.

* ...

### 2.4 Linux

* **distibution**: A _distribuição_ Linux é composta por um **bundle**(pacote) de programas, que tipicamente são compostas pelo
>A Linux distribution is a bundle of software, typically comprised of the Linux kernel, utilities, management tools, and even some application software in a package which also >includes the means to update core software and install additional applications.

Assim sendo, as _distribution_ tem a responsabilidade de configurar o armazenamento, construir o **kernel** e instalar o drive de hardware, também instalndo aplicativos e utilitários que o façam totalmente funcional no sistema do computador. > The organizations that create distributions also include tools to manage the system, a package manager to add and remove software, as well as update programs to provide security and functionality patches.

#### Life Cycle 

>Linux distributions can be broadly classed in two main categories: enthusiast and enterprise. An enthusiast distribution such as openSUSE’s Tumbleweed has a fast update cycle, is not supported for enterprise and may not contain (or drop) features or software in the next version that are in the current one. Red Hat’s Fedora project uses a similar method of development and release cycle, as does Ubuntu Desktop.

.Enterprise distributions are almost the exact opposite, in that they take care to be stable and consistent, and offer enterprise-grade support for extended periods, anywhere from 5-13 years in the case of SUSE. Enterprise distributions are fewer by far, being offered mainly by Red Hat, Canonical and SUSE

* Sendo esses dois parágrafos a definição pura de _testing_ e _stable_ releases.

> Application software may be written such that it only supports a specific release of a distribution, requiring users to remain on an older, less secure operating system than they might like. Therefore, some Linux releases are considered to have long-term support (LTS) of 5 years or more while others are only supported for two years or less.

#### Stability 

* **Community-oriented beta release** =

> openSUSE and its enterprise counterpart SLES (SUSE Linux Enterprise Server) are similar, in that the community edition is used as a testing ground for the features and functions that will eventually be migrated into the enterprise version. Previously somewhat dissimilar, later versions of the openSUSE and SLES distribution codebases are nearly identical, allowing for easier migration of features and code from one to the other.

#### Interface 
* **Terminal application**(shell):
* **shell**:
* **CLI**:

> the CLI, is a text-based interface to the computer, where the user types in a command and the computer then executes it. The CLI environment is provided by an application on the computer known as a terminal. ‌⁠​⁠​ The terminal accepts what the user types and passes to a shell. The shell interprets what the user has typed into instructions that can be executed by the operating system. If output is produced by the command, then this text is displayed in the terminal. If problems with the command are encountered, then an error message is displayed.

> During login there may be some text displayed called the **message of the day** (MOTD). This is an opportunity for the systems administrator to pass information to users, or just make a silly joke. Following the MOTD is the command prompt, in the example above, the user has entered the w command which shows who is logged in. As new commands are entered and processed, the window scrolls up and older text is lost across the top. The terminal itself is responsible for keeping any history, such as to allow the user to scroll up and see previously entered commands. As far as Linux is concerned, what is on the screen is all that there is. There’s nothing to move around.

## Key Terms:



Android
    A Linux distribution that provides a platform for mobile users but lacks the traditional GNU/Linux packages to make it compatible with desktop Linux distributions.
    Section 2.4.1 
CentOS
    A Linux distribution that is compatible with Red Hat Enterprise Linux but does not offer the paid support that Red Hat does.
    Section 2.4.1 
Debian
    An operating system that uses the Linux kernel. It that promotes the use of open source software and adherence to standards.
    Section 2.4.1 
Linux Mint
    A Linux distribution that is a derivative of Ubuntu and still relies upon the Ubuntu repositories.
    Section 2.4.1 
Raspberry Pi
    A hardware platform used in training for programmers and hardware designers at all levels. Its low cost and ease of use have made it popular with educators.
    Section 2.4.1 
Raspbian
    A specialized Linux distribution optimized to run on Raspberry Pi hardware.
    Section 2.4.1 
Red Hat
    A Linux distribution that introduced Red Hat Package Manager (RPM). The developer formed a company by the same name which specializes in open source software.
    Section 2.4.1 
SUSE
    One of the first comprehensive Linux distributions. It is derived from Slackware which offers many similarities with Red Hat Enterprise Linux.
    Section 2.4.1 
Scientific Linux
    A specific use distribution based on Red Hat. It was designed to enable scientific computing.
    Section 2.4.1 
Ubuntu
    The most popular Debian derived distribution. It has several different variants for desktop, server, and various specialized applications as well as an LTS version.
    Section 2.4.1 
beta
    A software release that has many new features that haven’t been tested.
    Section 2.1.1 
command line interface (CLI)
    A text based interface in which the user enters commands. Feedback, output and programs are presented in text format only.
    Section 2.1.1 
desktop configuration
    Desktop are preferred if the user interacts with the system directly. Desktop system primarily run a GUI for the ease of use of its user.2.1.1
    Section 2.1.1 
graphical user interface (GUI)
    A visual user interface that allows the user to interact with the system using windows, icons, a cursor, etc.
    Section 2.1.1 
long-term support (LTS)
    Associated with the life cycle of distributions, this feature states that software is supported for 5 years or more.
    Section 2.4 
maintenance cycles
    The period of time vendors support older versions of software before not offering any updates.
    Section 2.1.1 
openSUSE
    A Linux distribution that is a completely open, free version of SUSE Linux Enterprise with multiple desktop packages similar to CentOS and Linux Mint.
    Section 2.4.1 
stable
    A software release whose updates have been tested in the field.
    Section 2.1.1 


