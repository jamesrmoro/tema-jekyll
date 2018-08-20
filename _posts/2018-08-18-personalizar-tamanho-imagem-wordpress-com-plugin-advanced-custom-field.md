---
layout: post
cover: 'assets/images/plugin-advanced-custom-field.jpg'
title:  Personalizar tamanho de imagem WordPress com o plugin Advanced Custom Field
date:   2018-08-18 20:28:00
tags: wordpress
subclass: 'post tag-meta'
categories: 'jamesrmoro'
navigation: True
description: Veja como configurar um campo personalizado quando precisar usar imagens em seu projeto WordPress
logo: ''
---

Com o plugin [Advanced Custom Fields – ACF](https://wordpress.org/plugins/advanced-custom-fields "Advanced Custom Fields – ACF"){:target="_blank"}, você cria campos personalizados em seus posts. 

É possível criar outros campos em outros lugares, como custom posts, páginas e até no perfil do usuário. Tudo isso para facilitar a inserção de informações onde você quiser.

Hoje vou mostrar como é fácil trabalhar com este plugin quando precisar usar em imagens.

##Tipos de campos adicionais que você pode configurar

Com esta configuração você pode definir o tipo de retorno dos dados.

- Você pode escolher entre Objeto (array de dados);
- URL da imagem (string);
- ID da imagem (int);

**Dica:** você pode debugar as variáveis para ver tudo o que ela retorna, utilizando a função <code>var_dump()</code> do php.

##Exemplo de uso básico (valor retornado do tipo Objeto)

Com este exemplo abaixo, podemos exibir a imagem por meio do retorno de um Objeto. Este retorno é ideal quando você precisa pegar os atributos da imagem, como o campo "alt".

<pre style='color:#000000;background:#ffffff;'><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>=</span><span style='color:#000000; background:#ffffe8; '> get_field</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0000e6; background:#ffffe8; '>'imagem-exemplo'</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#800000; background:#ffffe8; font-weight:bold; '>if</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>!</span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>empty</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>:</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span>

	<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>img</span><span style='color:#274796; '> </span><span style='color:#074726; '>src</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>echo</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#808030; background:#ffffe8; '>[</span><span style='color:#0000e6; background:#ffffe8; '>'url'</span><span style='color:#808030; background:#ffffe8; '>]</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#0000e6; '>"</span><span style='color:#274796; '> </span><span style='color:#074726; '>alt</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>echo</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#808030; background:#ffffe8; '>[</span><span style='color:#0000e6; background:#ffffe8; '>'alt'</span><span style='color:#808030; background:#ffffe8; '>]</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#0000e6; '>"</span><span style='color:#274796; '> </span><span style='color:#a65700; '>/></span>

<span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>endif</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span>
</pre>

##Exemplo de uso básico (valor retornado do tipo ID)

No exemplo abaixo, podemos observar o uso da opção com o retorno ID. O código final é uma tag img com a url do tamanho do crop que você colocou na variável size.

<pre style='color:#000000;background:#ffffff;'><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>=</span><span style='color:#000000; background:#ffffe8; '> get_field</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0000e6; background:#ffffe8; '>'imagem-exemplo'</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#797997; background:#ffffe8; '>$size</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>=</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#0000e6; background:#ffffe8; '>'full'</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#696969; background:#ffffe8; '>// (thumbnail, medium, large, full, ou um tamanho customizado criado em seu tema)</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#800000; background:#ffffe8; font-weight:bold; '>if</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800080; background:#ffffe8; '>{</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '>	</span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>echo</span><span style='color:#000000; background:#ffffe8; '> wp_get_attachment_image</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#808030; background:#ffffe8; '>,</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$size</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#800080; background:#ffffe8; '>}</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#5f5035; background:#ffffe8; '>?></span>
</pre>

##Exemplo de uso personalizado (valor retornado do tipo Objeti)

No exemplo abaixo, podemos observar o uso da opção com o retorno de Objeto, mas desta vez vamos pegar o tamanho da imagem que foi feito crop.

O tamanho do crop da imagem foi dado o nome de slider. O código abaixo vai retornar a url com crop na tag img.

<pre style='color:#000000;background:#ffffff;'><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span>
<span style='color:#000000; background:#ffffe8; '>&#xa0;&#xa0;&#xa0;&#xa0;</span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>=</span><span style='color:#000000; background:#ffffe8; '> get_field</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0000e6; background:#ffffe8; '>'imagem'</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '></span>
<span style='color:#5f5035; background:#ffffe8; '>?></span>

<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>img</span><span style='color:#274796; '> </span><span style='color:#074726; '>src</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>echo</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#797997; background:#ffffe8; '>$image</span><span style='color:#808030; background:#ffffe8; '>[</span><span style='color:#0000e6; background:#ffffe8; '>'sizes'</span><span style='color:#808030; background:#ffffe8; '>]</span><span style='color:#808030; background:#ffffe8; '>[</span><span style='color:#0000e6; background:#ffffe8; '>'slider'</span><span style='color:#808030; background:#ffffe8; '>]</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#0000e6; '>"</span><span style='color:#a65700; '>></span>
</pre>

##Exemplo de uso básico (valor retornado do tipo URL)

No último exemplo abaixo, podemos observar o retorno por meio da URL. Este exemplo é útil quando você precisa exibir apenas o campo, sem parâmetros nenhum!

<pre style='color:#000000;background:#ffffff;'><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>if</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#000000; background:#ffffe8; '> get_field</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0000e6; background:#ffffe8; '>'imagem-exemplo'</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>:</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span>

	<span style='color:#a65700; '>&lt;</span><span style='color:#800000; font-weight:bold; '>img</span><span style='color:#274796; '> </span><span style='color:#074726; '>src</span><span style='color:#808030; '>=</span><span style='color:#0000e6; '>"</span><span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> the_field</span><span style='color:#808030; background:#ffffe8; '>(</span><span style='color:#0000e6; background:#ffffe8; '>'image'</span><span style='color:#808030; background:#ffffe8; '>)</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span><span style='color:#0000e6; '>"</span><span style='color:#274796; '> </span><span style='color:#a65700; '>/></span>

<span style='color:#5f5035; background:#ffffe8; '>&lt;?php</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#800000; background:#ffffe8; font-weight:bold; '>endif</span><span style='color:#800080; background:#ffffe8; '>;</span><span style='color:#000000; background:#ffffe8; '> </span><span style='color:#5f5035; background:#ffffe8; '>?></span>
</pre>

##Conclusão

Mais do que um criador de campos personalizados para coleta de dados, o plugin **Advanced Custom Fields** trabalha com os mais diversos tipos de campos ou fields – texto, área de texto, arquivos, imagens, listas, checkbox, user, Google Maps, Tabs, dentre muitos (muitos) outros.