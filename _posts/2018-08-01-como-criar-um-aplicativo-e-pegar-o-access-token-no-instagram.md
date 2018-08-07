---
layout: post
cover: 'assets/images/token-instagram.jpg'
title:  Como criar um Aplicativo e pegar o Access Token no Instagram 
date:   2018-08-01 08:00:00
tags: instagram
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: Exibindo fotos do Instagram no seu website
logo: ''
---

A maioria dos widgets para sites/blogs que mostram fotos recentes de um perfil no Instagram, precisam de autorização do usuário para que funcionem.

Recentemente, eu precisei criar uma galeria de imagens com as fotos do Instagram. O resultado você pode  [ver aqui](https://jamesrmoro.github.io/galeria-api "Galeria Instagram"){:target="_blank"}

Devido as últimas alterações da API do Instagram, alguns usuários podem ter problemas com o atual código token. Então esse artigo é para explicar como gerar o *Access Token* na sua conta do Instagram.

##Criando o aplicativo

Para criar um aplicativo no Instagram, entre [nessa página](https://www.instagram.com/developer/clients/manage/ "Developer Instagram"){:target="_blank"}.

Se você não tem nenhum aplicativo criado na sua conta do Instagram, ele irá pedir pra cadastrar a URL do seu site, seu telefone e porque você quer criar um aplicativo. 

Preencha esses campos e depois de confirmar, na nova página que abrir terá o botão **Register a new client**. Clique nesse botão.

Na próxima página você precisa preencher as informações do seu aplicativo.

<img src="assets/images/api-instagram.png" alt="Api Instagram">

1. Na aba **Details**, preencha o nome do aplicativo, a descrição, nome do seu site/blog, a URL dele, e **no campo Valid redirect URLs preencha com http://seudominio.com.br**

2. Na aba **Security**, deixe desmarcado a opção **Disable implicit OAuth**.
Então preencha o campo **Type the words above** e depois clique no botão **Register**.

É importante deixar desmarcado a opção **Disable implicit OAuth** antes de clicar no botão **Register**. Do contrário, a URL **http://seusite.com.br** não será aceita.

<img src="assets/images/integracao-instagram.png" alt="Integração Instagram">

3. Na próxima página você terá seu aplicativo criado com o código Client ID. Esse código será necessário para gerar o access token.

<img src="assets/images/instagram-token.png" alt="Pegar Access Token no Instagram">

##Gerando o Access Token

Agora que você já tem seu aplicativo criado, vamos gerar o código access token. Você vai precisar do código **Client ID** do seu aplicativo.

Pra gerar o access token use a URL abaixo, substituindo **YOUR_CLIENT_ID** pelo código Client ID do seu aplicativo.

https://instagram.com/oauth/authorize/?client_id=**YOUR_CLIENT_ID**&redirect_uri=http://seusite.com.br&response_type=token

Então cole essa URL no seu navegador e visite ela (como se estivesse abrindo um site/blog).
Quando fizer isso vai abrir uma página do instagram pedindo pra você autorizar seu perfil para esse aplicativo.

Só clicar no botão **Authorize**.

<img src="assets/images/instagram-acesso-api.png" alt="Gerar accesso Token">

Após clicar no botão vai retornar uma página no seu próprio computador, com erro.

**Ignore o conteúdo da página que retornar, o importante é a URL na barra de endereços do seu navegador.**

Vai retornar algo como **http://seusite.com.br/#access_token=CODIGO_TOKEN_AQUI**

Então é copiar o **código token** da URL e colar no widget do seu site/blog.
