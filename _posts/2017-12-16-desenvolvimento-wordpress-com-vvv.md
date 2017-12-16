---
layout: post
cover: 'assets/images/minhas-metas-para-2018.jpg'
title:  Desenvolvimento Wordpress com VVV
date:   2017-10-15 10:18:00
tags: vagrant
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: Este é o meu planejamento para 2018. Um registro que vai além de uma promessa qualquer.
logo: ''
---

Para definir o meu ambiente de desenvolvimento próximo de um servidor, eu optei por usar o VVV. Abaixo irei explicar as vantagens de usar essa ferramenta nos dias de hoje. 

O VVV é uma predefinição da configuração Vagrant voltada para projetos em WordPress. Com essa ferramenta, é possível trabalhar com o desenvolvimento de um tema Wordpress, um plugin ou até mesmo para contribuir para o WordPress Core. 

A VVV também possui diversas ferramentas como WP-CLI , PHP Code Sniffer e Composer que auxiliam em nossos fluxos de trabalho de desenvolvimento.

##O cenário

O WordPress é executado no PHP, que é uma linguagem de codificação do lado do servidor, pelo que precisamos de um servidor para executar o WordPress.

Talvez você não ache necessário a migração para o VVV. Isso porque você já usa aplicativos como MAMP, WAMP ou XAMPP e que tem proporcionado um nível satisfação em seus desenvolvimentos. Mas que tal experimentar e deixar seu comentário aqui no post? Eu poderei lhe ajudar :)

##Mas por que optar por VVV?

Vamos imaginar o seguinte cenário: temos uma equipe de desenvolvedores que trabalha remotamente, e nossa equipe está distribuída em diversas regiões do Brasil. Cada desenvolvedor tem sua preferência - alguns usam o Windows, enquanto outros usam, Linux ou Mac. 

Para padronizar, adotamos Vagrant e VVV para que todos tenham o mesmo ambiente de desenvolvimento e tenham 100% de aproveitamento na experiência de uso de suas máquinas, sem nenhuma preocupação com incompatibilidade com pacotes e dependências. Que por hora funcionam, e outras não dependendo do sistema operacional que você escolheu.

##Quais as vantagens de usar VVV?

A capacidade de poder configurar sua máquina de trabalho em em qualquer lugar dentro de alguns minutos é fascinante. Uma das coisas que mais me chamou atenção quando optei por usar VVV foi exatamente o curto tempo em deixar tudo a funcionar.

As ferramentas de linha de comando são essenciais para automação do trabalho, como o <a href="http://wp-cli.org" target="_blank">WP-CLI</a> que é extramamente poderosa para automatizar tudo no seu WordPress

* Altamente portátil
* Altamente configurável
* Altamente automatizado

##O que vem no VVV?

<ol>
  <li><a href="http://www.ubuntu.com/">Ubuntu</a> 14.04 LTS (Trusty Tahr)</li>
  <li><a href="https://develop.svn.wordpress.org/trunk/">WordPress Develop</a></li>
  <li><a href="https://wordpress.org/">WordPress Stable</a></li>
  <li><a href="http://wp-cli.org/">WP-CLI</a> (master branch)</li>
  <li><a href="http://nginx.org/">nginx</a> (<a href="http://nginx.com/blog/nginx-1-6-1-7-released/">mainline</a> version)</li>
  <li><a href="https://mariadb.org/">MariaDB</a> 10.1</li>
  <li><a href="http://php-fpm.org/">php-fpm</a> 7.0.x</li>
  <li><a href="http://memcached.org/">memcached</a></li>
  <li>PHP <a href="https://pecl.php.net/package/memcache">memcache extension</a></li>
  <li>PHP <a href="https://pecl.php.net/package/xdebug/">xdebug extension</a></li>
  <li>PHP <a href="https://pecl.php.net/package/imagick/">imagick extension</a></li>
  <li><a href="https://phpunit.de/">PHPUnit</a></li>
  <li><a href="http://beyondgrep.com/">ack-grep</a></li>
  <li><a href="http://git-scm.com/">git</a></li>
  <li><a href="https://subversion.apache.org/">subversion</a></li>
  <li><a href="http://ngrep.sourceforge.net/usage.html">ngrep</a></li>
  <li><a href="http://dos2unix.sourceforge.net/">dos2unix</a></li>
  <li><a href="https://github.com/composer/composer">Composer</a></li>
  <li><a href="https://code.google.com/p/phpmemcacheadmin/">phpMemcachedAdmin</a></li>
  <li><a href="http://www.phpmyadmin.net/">phpMyAdmin</a> (multi-language)</li>
  <li><a href="https://github.com/rlerdorf/opcache-status">Opcache Status</a></li>
  <li><a href="https://github.com/jokkedk/webgrind">Webgrind</a></li>
  <li><a href="https://nodejs.org/">NodeJs</a></li>
  <li><a href="https://github.com/gruntjs/grunt-cli">grunt-cli</a></li>
  <li><a href="http://mailcatcher.me/">Mailcatcher</a></li>
</ol>

##Como instalar

Agora que você já tem uma ideia aproximada sobre os benefícios desta ferramenta, irei mostrar como configurar O VVV e colocá-lo em funcionamento.

Neste tutorial eu irei ensinar você a configurar no Linux Mint, distro que escolhi definitivamente para realizar meus trabalhos de desenvolvimento.

##Etapa 1: Instalar o VirtualBox

Em primeiro lugar, vamos ter que instalar uma Máquina Virtual (VM) para hospedar nossos ambientes de desenvolvimento criados através do Vagrant. Neste tutorial, optei por usar o VirtualBox - é grátis. Um instalador está disponível para cada plataforma - Windows, OSX e algumas distribuições Linux - na página de download.

imagem aqui

O VirtualBox pode demorar um pouco para ser instalado, após concluído, podemos instalar o Vagrant.

##Etapa 2: Instalar Vagrant

Um instalador Vagrant está disponível para Mac, Windows e Linux no site. Então realize o download do software de acordo com sua plataforma e siga as etapas. 

##Etapa 3: Instalar Plugins Vagrant

##Criando um novo site WordPress

Com o VV é possível tornar uma instalação de um novo site do WordPress com um simples comando:

<code>vv create</code>

Uma vez executado, ele irá solicitar algumas perguntas ao longo do caminho para configurar o novo site, que são:

###1. Nomeando o Diretório do site

Para usuários MAMP, é semelhante a criar uma nova pasta dentro da raiz do documento MAMP em <code>/MAMP/htdocs/</code> . Esta é a pasta onde estã todos os arquivos do site. 

Nesta etapa, insira o nome do diretório sem espaços, de preferência em minúsculas, por exemplo:

###2. Nomeando o Domínio
Defina o domínio para o nosso novo site. Um domínio para um site local geralmente termina com <code>.dev</code> ou <code>.local</code> . Nesse caso, vamos dar o nome de <code>wordpress.dev</code>

###3. Defina a versão do WordPress
Aqui vamos instalar o WordPress 4.9.1, que é a última versão até o momento que este artigo foi escrito. A lista completa de versões do WordPress pode ser encontrada na página <a href="https://wordpress.org/download/release-archive" target="_blank">Release Archive</a>.

###4. Ativar Multisite
Ele nos pergunta se queremos ativar o modo Multisite WordPress. Nós selecionamos <code>n</code>

###5. Recursos de conteúdo WP
O diretório de wp-content do WordPress geralmente armazenada uma série de subdiretórios, como os diretórios de temas, plugins e uploads. Às vezes podemos criar algumas pastas extras para armazenar alguns arquivos. Se você tiver um conteúdo predefinido hospedado em um repositório Git, você pode inserir a URL e deixar VV clonar o repositório.

Por enquanto, deixamos-o vazio.

###6. Importar SQL
Nesta instalação não iremos importar nenhum banco de dados SQL. Então também deixaremos este prompt vazio. Mas, se você tiver um, especifique o caminho do diretório onde o arquivo SQL se encontra, por exemplo: <code>/Sites/db/wp.sql</code>.

###7. Temas e complementos padrão
O WordPress vem com os temas padrão (por exemplo, TwentyFifteen, TwentySixteen, etc.) e plugins ( Akismet e Hello Dolly ) que, muitas vezes, não usaremos. Nesta etapa, podemos passar para o prompt para dizer ao VV para removê-los completamente.

###8. Conteúdo Dummy
Podemos dizer ao VV para instalar o conteúdo da amostra do <a href="https://github.com/poststatus/wptest" target="_blank">WPTest</a> . É um extenso conjunto de conteúdos que inclui posts, páginas e comentários. Este conteúdo será útil para encontrar quaisquer desalinhamentos, problemas de compatibilidade ou erros em nossos temas e plugins. Por isso, digite <code>s</code>

###9. WP_DEBUG
Nós definitivamente habilitaremos o <code>WP_DEBUG</code> para permitir que o WordPress imprima quaisquer erros de PHP durante o desenvolvimento. Por isso, digite <code>s</code> no prompt.

###10. Confirmação
Finalmente, confirme que todas as configurações definidas estão corretas antes do VV prosseguir com a instalação. Se tudo estiver bem, digite <code>s</code> para prosseguir. Caso contrário, digite <code>n</code> para interromper a operação e você pode repetir o <code>vv create</code> desde o início.

Uma vez feito, o VV mostrará o site, bem como os dados de acesso para efetuar o login.

###Painel do Vagrant
O Painel do Vagrant é acessível em <code>vvv.dev</code>

##Vagrant Manager
Outro utilitário que você pode instalar é o <a href="http://vagrantmanager.com/images" target="_blank">Vagrant Manager</a>.

Vagrant Manager é semelhante ao MAMP e WAMP onde, neste caso, nos permite executar, interromper e recarregar Vagrant em poucos cliques. 

Uma vez que o Vagrant Manager está instalado e em execução, você pode encontrar uma lista das configurações do Vagrant que estão atualmente ativas.

##phpMyAdmin
Vagrant também vem com o phpMyAdmin incorporado, acessível em <a href="vvv.dev/database-admin" target="_blank">vvv.dev/database-admin/</a>. No entanto, para aqueles que não são fãs do phpMyAdmin por não possuir uma interface desejável, e ainda ser lenta em processar consultas em um banco de dados enorme, é sugerido usar uma aplicação como Sequel Pro ou SQL Workbench. 

Primeiro temos que conectar o aplicativo ao MySQL.

##Conectando-se ao MySQL com a aplicação nativa
Aqui estou usando SQL Workbench no Linux Mint. No entanto, as credenciais necessárias para se conectar ao MySQL são aplicáveis ​​independentemente dos aplicativos que você está usando. Eles são os mesmos.

* <strong>MySQL Host:</strong> 127.0.0.1
* <strong>Nome de usuário MySQL:</strong> root
* <strong>Senha do MySQL:</strong> root
* <strong>SSH Host:</strong> wordpress.dev (também aplicável com qualquer domínio registrado em VVV)
* <strong>Usuário SSH:</strong> vagrant
* <strong>Senha SSH:</strong> vagrant

##Qual o próximo passo?
Como mencionado, o VVV vem com um pacote de ferramentas, incluindo PHP CodeSniffer, que permite que você execute auditoria de código em seus projetos de acordo com os Padrões de Codificação do WordPress. Eu esrevi um artigo sobre isso e pode ser lido neste link. 

No entanto, uma vez que o PHP CodeSniffer é algo além do escopo deste tutorial, coloquei algumas referências abaixo para ajudá-lo.

* The WordPress Coding Standard Series
* PHP CodeSniffer Official Wiki