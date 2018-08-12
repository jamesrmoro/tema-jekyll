---
layout: post
cover: 'assets/images/como-usar-greensock.jpg'
title:  O que é GreenSock?
date:   2018-08-10 10:18:00
tags: dicas
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: GreenSock Animations Platform – GSAP foi desenvolvida com Javascript puro e é livre e de código aberto.
logo: ''
---

 Com [GreenSock Animations Platform](https://greensock.com "GreenSock Animations Platform"){:target="_blank"} você consegue criar todas as animações que são possíveis com CSS Animations. Além disso é possível controlar estados, interações de usuário, sequências, pausas, repetições, etc. 

 O melhor de tudo isso é que GSAP ainda oferece suporte a navegadores antigos e não possui dependências com outras bibliotecas como jQuery, por exemplo. Como essa biblioteca não possui dependências, temos uma garantia de performance incrível.

##Sobre as animações do passado

Nos anos 90 até meados dos anos 2000, as animações que existiam na web boa parte era feita em Flash. No entanto, quando Steve Jobs anunciou, em 2010, que o iOS não suportaria Flash, as animações começaram a desaparecer da web. Logo, tudo se tornou mais estático. Acontece que sem as animações, o mundo digital deixa de ser interessante e intuitivo. Por isso então surgiu o CSS Animations.

##Algumas coisas sobre GreenSock

**TweenLite:** O TweenLite é uma ferramenta de animação extremamente rápida, leve e flexível que serve de base para GSAP. Uma ocorrência de TweenLite manipula interpolação de uma ou mais propriedades de qualquer objeto (ou matriz de objetos) ao longo do tempo. O TweenLite pode ser usado sozinho para realizar a maioria das tarefas de animação com tamanho mínimo de arquivo ou pode ser usado em conjunto com ferramentas avançadas de sequenciamento, como TimelineLite ou TimelineMax, para simplificar tarefas complexas.

**Exemplo TweenLite:**
<div class="cp_embed_wrapper"><iframe id="cp_embed_FcfKd" src="//codepen.io/anon/embed/FcfKd?height=300&amp;theme-id=6453&amp;slug-hash=FcfKd&amp;default-tab=js&amp;user=anon" scrolling="no" frameborder="0" height="300" allowtransparency="true" allowfullscreen="true" allowpaymentrequest="true" name="CodePen Embed" title="CodePen Embed 3" class="cp_embed_iframe " style="width: 100%; overflow: hidden;"></iframe></div>

**TweenMax:** O TweenMax estende o TweenLite, adicionando muitos recursos úteis (mas não essenciais, mas isso tudo TweenLite pode fazer além de não-essenciais, como repetição, yoyo, repeatDelay, etc Ele inclui muitos plugins comuns também como CSSPlugin de modo que você não precisa carregar tantos arquivos. O foco está em ser completo, em vez de leve.

**Exemplo TweenMax:**
<div class="cp_embed_wrapper"><iframe id="cp_embed_uyfDH" src="//codepen.io/anon/embed/uyfDH?height=300&amp;theme-id=6453&amp;slug-hash=uyfDH&amp;default-tab=js&amp;user=anon" scrolling="no" frameborder="0" height="300" allowtransparency="true" allowfullscreen="true" allowpaymentrequest="true" name="CodePen Embed" title="CodePen Embed 2" class="cp_embed_iframe " style="width: 100%; overflow: hidden;"></iframe></div>

**TimiLineLite:** Este recurso permite que você crie uma timeline com todas as animações que você criou, desta forma você poderá controlar como se estivesse num rolo de filme.


**Exemplo TimiLineLite:**
<div class="cp_embed_wrapper"><iframe id="cp_embed_cmKgh" src="//codepen.io/GreenSock/embed/cmKgh?height=523&amp;theme-id=3984&amp;slug-hash=cmKgh&amp;default-tab=result&amp;user=GreenSock" scrolling="no" frameborder="0" height="523" allowtransparency="true" allowfullscreen="true" allowpaymentrequest="true" name="CodePen Embed" title="CodePen Embed 1" class="cp_embed_iframe " style="width: 100%; overflow: hidden;"></iframe></div>

**TimiLineMax:** Versão extendida do TimiLineLite, mas com mais recursos. Com ele você pode usar repetição, repeatDelay, yoyo, currentLabel(), dentre outras coisas, recursos úteis mas não excenciais.

**Exemplo TimiLineMax:**
<div class="cp_embed_wrapper"><iframe id="cp_embed_FnsqC" src="//codepen.io/GreenSock/embed/FnsqC?height=371&amp;theme-id=3984&amp;slug-hash=FnsqC&amp;default-tab=result&amp;user=GreenSock" scrolling="no" frameborder="0" height="371" allowtransparency="true" allowfullscreen="true" allowpaymentrequest="true" name="CodePen Embed" title="CodePen Embed 2" class="cp_embed_iframe " style="width: 100%; overflow: hidden;"></iframe></div>

##Exemplo:

<p data-height="410" data-theme-id="0" data-slug-hash="jEEoyw" data-default-tab="html,result" data-user="GreenSock" data-pen-title="DrawSVGPlugin Animation" data-preview="true" class="codepen">See the Pen <a href="https://codepen.io/GreenSock/pen/jEEoyw/">DrawSVGPlugin Animation</a> by GreenSock (<a href="https://codepen.io/GreenSock">@GreenSock</a>) on <a href="https://codepen.io">CodePen</a>.</p>
<script async src="https://static.codepen.io/assets/embed/ei.js"></script>

##Dica

Neste artigo eu quero deixar este [link com uma lista de cursos](https://webdesign.tutsplus.com/pt/articles/popular-courses-on-css-animation--cms-27166 "link com uma lista de cursos"){:target="_blank"} para você se aprimorar na área de Front-End. São diversos cursos que você pode fazer e todos são voltados a animações. 

##Conclusão

Nos começo da internet, as animações ficaram conhecidas por tdos aqueles efeitos estranhos e complexos que pareciam ótimos, mas que demoram muito para carregar uma página e eram difíceis de usar. Mas agora com a possibilidade do framework GreenSock, as animações em elementos HTML ficará mais fácil.