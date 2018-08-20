---
layout: post
cover: 'assets/images/history-api-javascript.jpg'
title:  Navegação com tabs mudando a url
date:   2018-08-18 20:28:00
tags: javascript
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: Veja como mudar a url do browser sem dar refresh usando a função pushState do objeto History do javascript.
logo: ''
---

Recentemente eu precisei criei uma navegação semelhante a imagem abaixo.

<img style="max-width: 100%" src="assets/images/navegacao.gif" alt="Navegação">

No entanto, eu precisava atualizar a url com a slug assim que o usuário clicasse em uma aba. Isso era necessário porque para cada aba teria uma sessão de produtos que iria compor uma página exclusiva.

Isso foi feito porque o usuário poderia compartilhar a url assim que ele clicasse na aba de categoria do produto. 

Assim, ao compartilhar a url, ele acessaria a página de categoria criada daquele produto. 

A ideia era não ter somente os produtos na Home do site, mas também em páginas isoladas, então foi criado as sessões de categorias paras estes produtos.

Optei por criar desta forma para que estes conteúdos pudessem ser indexados pelos mecanismos de busca.

Abaixo você pode ver o resultado final.

<script src="https://gist.github.com/jamesrmoro/68dbcfd693dc9f22ceab776b3c6ba256.js"></script>

Este exemplo foi criado usando <code>window.history.pushState</code>. Assim é possível manipular o histórico do navegador por meio desta API.