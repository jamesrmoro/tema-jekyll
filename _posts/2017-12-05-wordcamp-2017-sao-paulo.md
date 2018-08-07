---
layout: post
cover: 'assets/images/wordcamp-2017.jpg'
title:  WordCamp São Paulo 2017 | O maior evento oficial sobre WordPress
date:   2017-12-05 15:04:00
tags: wordpress
subclass: 'post tag-meta'
categories: 'jamesrmoro wordpress'
navigation: True
description: No dia 02 de dezembro a equipe da Soma Dev esteve presente no 6º encontro sobre Wordpress, o Wordcamp 2017.
logo: ''
---

No dia 02 de dezembro a equipe da <a href="https://www.facebook.com/agenciasomadev" title="Soma Dev" target="_blank">Soma Dev</a> esteve presente no 6º encontro sobre Wordpress, o <strong>Wordcamp 2017</strong>.

O evento aconteceu em São Paulo na Faculdade Impacta, e contou com diversas palestras e workshops. Foram abordados diversos assuntos interessantes.

<img src="assets/images/wordpress.gif" alt="">

##Sobre o evento e as programações

Neste artigo eu irei compartilhar com vocês alguns assuntos sobre este dia.

Palestras com <i>cases</i> reais foram apresentadas pelos palestrantes. Técnicas e ferramentas para otimização e desenvolvimento de websites rápidos, robustos e leves, prontos para receber grandes volumes de acessos foram assuntos debatidos na programação do evento.

O objetivo de palestras como essas, é que o nosso conhecimento recebe aquele <i>upgrade</i>, e assim podemos ter o compromisso com o cliente em entregar um projeto onde seu website terá os melhores <i>scores</i> de web pages analyzers, como PageSpeed, YSlow, etc.

##Ferramentas essenciais para desenvolvedores de plugins

Essa palestra foi bem interessante pois foi apresentado recursos para otimização no ambiente de desenvolvimento.

Para o desenvolvimento de plugins para WordPress, ou até mesmo websites e aplicativos, existem diversas ferramentas disponíveis hoje em dia que facilitam e muita na hora de desenvolver.

Ferramentas como o Vagrant, o Grunt e o PHP Code Sniffer, podem-lhe garantir e auxiliar que o projeto do cliente (e o código) fique totalmente organizado e bem estruturado.

Na <a href="https://www.facebook.com/agenciasomadev" title="Soma Dev" target="_blank">Soma Dev</a>, recentemente adotamos o ambiente de desenvolvimento com <a href="https://github.com/Varying-Vagrant-Vagrants" target="_blank">VVV</a> que nos possibilita subir rapidamente um servidor, sem nenhum problema com banco de dados, ou configurações extras, que geralmente dão problemas em máquinas locais.

A palestra foi ministrada por <a href="https://twitter.com/tiagoscd" target="_blank">@tiagoscd</a> e os slides podem ser visualizados <a href="https://www.slideshare.net/tiagohillebrandt/ferramentas-essenciais-para-desenvolvedores-de-plugins-wordpress" target="_blank">neste link</a>

##Automatizando tarefas no WordPress utilizando suas funções nativas de cron jobs.

Na palestra apresentado por <a href="https://twitter.com/vilourenco" target="_blank">@vilourenco</a>, foi mostrado o recurso de tarefas cron jobs no Wordpress.

Cron jobs compõem uma tecnologia responsável por executar tarefas agendadas em um servidor. Para você entender melhor, um exemplo bem simples é quando você agenda um post para ser publicado em determinada data no seu site/blog.

<img style="width:430px" src="assets/images/cron-jobs.gif" alt="">

No entanto cron jobs pode ir muito além, pois as utilidades são várias. Utilizar cron jobs exige um nível de conhecimento e programação elevados, pois a manipulação incorreta pode acarretar em mal funcionamento das funções básicas e na lentidão do sistema.

Você sabia que um tema comprado pode haver recursos de cron jobs que podem deixar seu site lento? Se você quer saber como resolver isso, deixe seu comentário neste artigo :)

##Guia de Segurança para Wordpress

Segurança é um negócio sério.

O conteúdo que o cliente disponibiliza em seu site e as informações são a maior riqueza da empresa. Por isso é sempre importante manter essas informações seguras.

<img src="assets/images/seguranca-web.gif" alt="">

Nós nos preocupamos com a segurança de nossos websites, e observamos a quantidade de ambientes vulneráveis à disposição de qualquer pessoa com algum conhecimento para explorá-los.

Para garantir que esses sites desenvolvidos não fiquem vulneráveis, nós da <strong>Soma Dev</strong> sempre seguimos algumas ações, como:

1. Realizar backups regulares dos dados;
2. Manter o WordPress, plugins e temas sempre atualizados;
3. Implementar a autenticação de dois fatores;
4. Proteger o banco de dados da instalação;
5. Certificar que o debug está protegido;
6. Blindar o arquivo wp-config.php;
7. Definir as permissões corretas para arquivos e pastas;
8. Definir regras no servidor em uso;
9. Excluir arquivos desnecessários do core;
10. Evitar SPAM e tentativas de postagens externas;
11. Não permitir a listagem dos nomes de usuários;
12. Se proteger de ataques de XSS;
13. Manter boas práticas de segurança.

##Criando um ambiente de alta disponibilidade para Wordpress com Kubernetes

<img src="assets/images/kubernetes.gif" alt="">

No workshop do <a href="https://twitter.com/rafaelangeline" target="_blank">@RafaelAngeline</a> foi mostrado como utilizar Kubernetes para o gerenciamento de containers Docker. O propósito dessa ferramenta é hospedar seus aplicativos WordPress com segurança e deixá-lo totalmente escalável.

O <a href="https://kubernetes.io" target="_blank">Kubernetes</a> oferece suporte a load balancer, que é um distribuidor de carga. Assim, você pode trabalhar com a recuperação de falhas em sua aplicação.

Dessa maneira, o Kubernetes tem como principal objetivo facilitar a implantação de aplicativos baseados em microservices. Ele foi baseado na experiência do Google de muitos anos de trabalho com containers, adaptando-o para se trabalhar com Docker.

##Os Progressive Web Apps – PWA (aplicativos web progressivos)

Essa palestra foi realizada por Ricardo Lima, onde foi falado sobre as experiências Web por meio da PWA (Aplicativos Web Progressivos).

A ideia é que você tenha aplicações web rodando em seu dispositivo móvel como se fosse aqueles app baixados. O objetivo disso é que você não tenha que instalar o app de um estacionamento por exemplo quando for ao Shopping. 


<img style="width: 390px" src="assets/images/push-demo-mobile.gif" alt="">

Com PWA, você faz muitas coisas sem ter que realizar uma instalação em seu aparelho móvel. Recebe notificações pushs, ícone na tela inicial, carregamento em tela inteira, funciona offline e é carregado instantaneamente.

E mesmo em conexões instáveis, não tem a necessidade de ser instalado a partir de uma loja de aplicativos como a Google Play.

Sendo assim, pudemos observar que é possível transformar qualquer site WordPress em um PWA.

Com isso, nós melhoramos consideravelmente a experiência do usuário, e aumentamos a visibilidade nos mecanismos de busca e reduzindo uso de recursos do servidor.

##Conclusão

Um evento como este nos proporciona o encontro de diversos profissionais, pois o Wordcamp busca reunir desenvolvedores, designers, publicitários, jornalistas, blogueiros e usuários casuais para debater os avanços, a usabilidade, as ferramentas, plugins e o código do WordPress.

Outras palestras muito interessantes foram ministradas por profissionais da área. E isso trouxe bastante valor para nós que trabalhamos diariamente com tecnologia.

E que venha o <strong>#Wordcamp2018</strong> :)

