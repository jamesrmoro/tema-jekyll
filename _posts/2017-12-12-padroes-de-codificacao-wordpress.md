---
layout: post
cover: 'assets/images/wordcamp-2017.jpg'
title:  Padrões de Codificação WordPress
date:   2017-12-12 12:04:00
tags: wordpress
subclass: 'post tag-meta'
categories: 'wordpress'
navigation: True
description: No dia 02 de dezembro a equipe da Soma Dev esteve presente no 6º encontro sobre Wordpress, o Wordcamp 2017.
logo: ''
---

##Aspas simples e duplas 
Use aspas simples e duplas quando apropriado. Se você não estiver tratando nada na string, use use aspas simples. Você nunca deve escapar aspas HTML numa string, porque você apenas precisa alternar entre os tipos de aspas, assim:

<pre class="language-markup"><code class="language-markup">    
<script type="text/plain">echo '<a href="/link/estatico" title="Yeah yeah!">Nome do link</a>';
echo "<a href='$link' title='$titulodolink'>$nomedolink</a>";
</script>
</code></pre>

##Indentação

Sua indentação deve sempre refletir uma estrutura lógica. Use tabs reais e não espaços, pois isso permite maior flexibilidade entre clientes.

Exceção: se você tem um bloco de código que seja mais legível se estiver alinhado, use espaços:

<pre class="language-markup"><code class="language-markup">[tab]$foo   = 'algumvalor';
[tab]$foo2  = 'algumvalor2';
[tab]$foo3  = 'algumvalor3';
[tab]$foo4  = 'algumvalor4'
</code></pre>

Regra de ouro: tabs devem ser usadas no início das linhas e espaços devem ser usados no meio das linhas.

##Estilo das Chaves

Chaves devem ser usadas em multiplos blocos:

<pre class="language-markup"><code class="language-markup">if ( condicao ) {
    acao1();
    acao2();
} elseif ( condicao2 && condicao3 ) {
    acao3();
    acao4();
} else {
   acaopadrao();
}
</code></pre>

No mais, se você tiver um bloco muito grande, considere quebrá-lo em dois ou mais blocos ou funções.

Caso seja realmente necessária a existência desse longo bloco, por favor ponha um pequeno comentário no final para que as pessoas percebam de relance o que aquela chave de fechamento está fechando -- normalmente isso é apropriado para blocos lógicos, maiores que cerca de 35 linhas, mas qualquer código que não seja intuitivamente óbvio pode ser comentado.

Blocos de uma linha apenas pode omitir as chaves para ficarem mais concisos:

<pre class="language-markup"><code class="language-markup">if ( condicao )
    acao1();
elseif ( condicao2 )
    acao2();
else
    acao3();
</code></pre>

Se qualquer um dos blocos relacionados tiver mais de uma linha então todos os blocos relacionados devem possuir chaves :

<pre class="markdown"><code class="language-markup">if ( condicao ) {
    acao1();
} elseif ( condicao2 ) {
    acao2a();
    acao2b();
}
</code></pre>

Loops devem sempre conter chaves para melhorar a legibilidade, e permitir poucas linhas de edição para posteriores correções ou adição de novas funcionalidades:

<pre class="markdown"><code class="language-markup">foreach ( $itens as $item ) {
    processar_item( $item );
}
</code></pre>

##include_once vs. require_once 
Aprenda a diferença entre <a href="http://us3.php.net/manual/en/function.include-once.php" target="_blank">include_once</a> e <a href="http://us3.php.net/manual/en/function.require-once.php">require_once</a>, e use o mais apropriado. Para citar a <a href="http://us3.php.net/manual/en/function.include.php">php página do manual php sobre o include():</a> "Os dois construtores são identicos em todos os aspectos exceto em como eles tratam as falhas. include() produz um Alerta (Warning) enquanto o require() resulta num Erro Fatal (Fatal Error)." Erros Fatais interrompem a execução do script.