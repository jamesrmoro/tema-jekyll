---
layout: post
cover: 'assets/images/testes-automatizados-com-javascript.jpg'
title:  Testes automatizados com Javascript
date:   2018-08-04 12:00:00
tags: estudos
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: A automação de testes existe para reduzir ao máximo o envolvimento humano em atividades manuais repetitivas.
logo: ''
---

Javascript é usado em mais de 93% dos sites hoje em dia. Muitas interações com a web são fornecidas via Javascript, o que faz toda mágica front-end acontecer. 

###O que é Jasmine?

Jasmine é um framework de desenvolvimento orientado por comportamento (BDD) para testes de Javascript. Ele não depende de nenhum outro framework de Javascript, nem mesmo requer um DOM (Document Object Model). E possui uma sintaxe óbvia e limpa para escrever testes facilmente.

###Estrutura dos testes

Os testes são estruturados da seguinte maneira:

* Suite: Agrupa um conjunto de testes
* Spec: Descreve um caso de teste
* Expectation: Descreve um retorno esperado dentro de um teste

###O que é o Travis CI

O Travis CI é um serviço web de Integração Contínua na nuvem integrado com o GitHub. Ele é gratuito para repositórios públicos(travis-ci.org) e pago para repositórios privados(travis-ci.com).

O CI significa *Continuous integration* (integração contínua), ou seja isto se refere a uma série de testes que você pode escrever para garantir que os seus códigos e afins funcionem da maneira esperada através de testes unitários.

Com apenas um arquivo chamado .travis.yml contendo algumas informações sobre o projeto, podemos produzir builds automatizados com todas as mudanças, para o branch master ou outro, e até mesmo através de pull request.

**Pré Requisitos**

* Conta no GitHub;
* Conta no Heroku;
* Para o Travis você poderá usar a mesma conta do GitHub;
* Git, NodeJS e Bower instalado;
* Um editor de texto: Sublime Text, Atom ou qualquer outro de sua preferência.

A **integração contínua** é uma prática de desenvolvimento de software de DevOps em que os desenvolvedores, com frequência, juntam suas alterações de código em um repositório central.

Os testes ajudarão sua equipe a ser mais produtiva ao liberar os desenvolvedores de tarefas manuais e encorajar comportamentos que ajudam a reduzir o número de erros e bugs implantados para os clientes.

###Conclusão

Com testes mais frequentes, sua equipe pode descobrir e investigar bugs mais cedo, antes que no futuro os problemas cresçam demais.

Os testes são uma parte muito importante do desenvolvimento de software. Isso pode tornar as coisas mais fáceis quando configuradas corretamente. 

Espero que depois de ler este post, você tenha ficado curioso em colocar isso em prática. Me acompanhe no Youtube que eu irei te mostrar na prática como isso funciona, assim você tera uma boa idéia de como integrar o teste de unidade em seus projetos JS :)