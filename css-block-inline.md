# Comportamento padrão dos elementos

Todo elemento HTML possui uma maneira natural de se comportar, ou seja, mesmo sem aplicar estilizações à tag. O parágrafo `<p></p>`, por exemplo, possui margem tanto na parte superior quanto na parte inferior de 1rem. Isso também ocorre com o comportamento do display de cada elemento; cada uma das tags tem um certo comportamento natural de display.

Para seguir com total entendimento do Flexbox, vamos entender o comportamento natural das tags no display. Alguns elementos possuem o display `block`, outros possuem o display `inline`. O que estamos vendo são comportamentos naturais, ou ‘default’, dos elementos, porém, podemos alterar quaisquer comportamentos com CSS.

## O que são elementos com display block?

Esses elementos têm o comportamento de ocupar toda a extensão, em largura, de quem os envolve. Se declararmos três parágrafos, eles ficarão um embaixo do outro, pois são elementos com display block.

### Tags que possuem naturalmente display block

- `<address>`
- `<article>`
- `<aside>`
- `<blockquote>`
- `<canvas>`
- `<dd>`
- `<div>`
- `<dl>`
- `<dt>`
- `<fieldset>`
- `<figcaption>`
- `<figure>`
- `<footer>`
- `<form>`
- `<h1>` - `<h6>`
- `<header>`
- `<hr>`
- `<li>`
- `<main>`
- `<nav>`
- `<noscript>`
- `<ol>`
- `<output>`
- `<p>`
- `<pre>`
- `<section>`
- `<table>`
- `<tfoot>`
- `<ul>`
- `<video>`

## O que são elementos inline?

Os inline são elementos que irão ocupar apenas o necessário do seu conteúdo, como, por exemplo, a tag `span`. Nesse caso, se colocarmos três tags `span` juntas, cada uma irá ficar ao lado da outra.

### Tags que possuem naturalmente display inline

- `<a>`
- `<abbr>`
- `<acronym>`
- `<b>`
- `<bdo>`
- `<big>`
- `<br>`
- `<button>`
- `<cite>`
- `<code>`
- `<dfn>`
- `<em>`
- `<i>`
- `<img>`
- `<input>`
- `<kbd>`
- `<label>`
- `<map>`
- `<object>`
- `<q>`
- `<samp>`
- `<script>`
- `<select>`
- `<small>`
- `<span>`
- `<strong>`
- `<sub>`
- `<sup>`
- `<textarea>`
- `<time>`
- `<tt>`
- `<var>`
