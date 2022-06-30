# Módulo 2 - Fundamentos web com HTML e CSS

As anotações aqui apresentadas foram desenvolvidas com base no Bootcamp "Geração Tech Unimed-BH", da plataforma de estudos **[DIO](https://web.dio.me/home)**.

## Curso 2 - Introdução à criação de websites com HTML5 e CSS3

//Primeiros passos para começar a programar

**Mentor: Lucas Vilaboim**

---

[2.1 Introdução ao curso de HTML](#21-introdução-ao-curso-de-html)

[2.2 Entendendo o que é semântica](#22-entendendo-o-que-é-semântica)

[2.3 Como usar textos e links em HTML](#23-como-usar-textos-e-links-em-html)

[2.4 Como inserir imagens em seu site](#24-como-inserir-imagens-em-seu-site)

[2.5 Como organizar listas com HTML](#25-como-organizar-listas-com-html)

[2.6 Introdução e concenitos básicos do CSS3](#26-introdução-e-conceitos-básicos-do-css3)

[2.7 Estilizando elementos, textos e listas](#27-estilizando-elementos-textos-e-listas)

[2.8 Dimensão e alinhamento](#28-dimensão-e-alinhamento)

---

### 2.1 Introdução ao curso de HTML

#### 2.1.1 Estrutura básica

Objetivos:

* História e Estrutura básica de HTML;
* Semântica de HTML;
* Principais elementos HTML.

O HTML foi criado em 1991, por Tim Bernes-Lee, que trabalhava em uma empresa e precisava compartilhar documentos com seus colegas. O processo de criação dessa linguagem (não de programação, mas sim de marcação) não foi rápido. O desenvolvimento começou a ser esboçado em 1980 e só foi “concluído”.

* Desde 1991 sugiram 5 versões do HTML, e a última (HTML5) foi lançada em 2014.

Para entender o HTML, precisamos entender o que é elemento, a base da linguagem. Tudo dentro de um documento HTML é o elemento.

![Estrutura HTML](./2.1.1_imagem1-estrutura.png "Estrutura HTML")

Um elemento HTML:

* Começa com uma tag de abertura, que diz qual o tipo do elemento em questão (no exemplo acima, \<h1>);
* A tag pode ter um atributo, que pode mudar uma funcionalidade, aparência ou dizer alguma cosa ao navegador;
* Depois vem o conteúdo do elemento (no exemplo acima, “Título”)
* Por fim, vem a tag de fechamento \</h1>

A estrutura básica de um documento HTML é pequena, consiste de:

```html
<!DOCTYPE html>
<html>
 <head> <!-- são informações que um navegador necessita -->
 <meta> 
 <title> </title> <!-- título na aba do navegador -->
 </head>
 
 <body>
 </body>
</html>
```

\<html>

A tag html é a raiz do seu documento, todos os elementos HTML devem estar dentro dela. E nela nós informamos ao navegador qual é o idioma desse nosso documento, através do atributo lang, para o português brasileiro usamos pt-BR.

\<head>

A tag head contém elementos que serão lidos pelo navegador, como os metadados - um exemplo é o charset, que é a codificação de caracteres e a mais comum é a UTF-8, o JavaScript com a tag script, o CSS através das tags style e link - veremos a diferença quando falarmos sobre CSS - e o título da página com a tag title.

\<body>

E dentro da tag body colocamos todo o conteúdo visível ao usuário: textos, imagens, vídeos.

---

### 2.2 Entendendo o que é semântica

#### 2.2.1 Semântica

Durante muitos anos, o elemento padrão no HTML foi a div, segundo a qual todo o conteúdo era construído.

Em 2014, com a quinta versão do HTML, houve várias mudanças importantes, a fim de melhorar performance e acessibilidade. No curso, o foco está na semântica.

A semântica permite descrever mais precisamente o conteúdo. Um bloco de texto não é apenas uma div, é um article e tem mais significado assim.

Há vários elementos para ressignificar as divs:

* \<section>

Representa uma seção genérica de conteúdo.

* \<header>

É o cabeçalho da página ou de uma seção da página. Normalmente contém logotipos, menus ou campos de busca.

* \<article>

Representa um conteúdo independente e de maior relevância dentro de uma página, como um post de blog, uma notícia em uma barra lateral ou um bloco de comentários. Um article pode conter outros elementos.

* \<aside>

É uma seção que engloba conteúdos relacionados ao conteúdo principal, como artigos relacionados, biografia do autor e publicidade. Normalmente são representadas como barras laterais.

* \<footer>

Esse elemento representa o rodapé do conteúdo ou de parte dele, pois ele é aceito dentro de vários elementos, como article e section e até do body.

* \<h1>-\<h6>
Eles não foram criados na versão 5 do HTML e nem são específicos para semântica, mas servem para esse propósito. São utilizados para marcar a importância dos títulos, sendo \<h1> o mais importante e <\h6> o menos.

>Uma dica: use apenas um \<h1> por página, pois ele representa o objetivo da sua página.

---

### 2.3 Como usar textos e links em HTML

#### 2.3.1 Tags para textos

Já falamos anteriormente sobre os elementos h1-h6, essenciais para indicar visualmente a importância e localização de seções de texto na página, mas para textos maiores e mais densos, p é o elemento usado.

O \<p> representa um parágrafo, mas não suporta apenas texto, podemos adicionar imagens, código, vídeos e vários outros tipos de conteúdo dentro dele.

#### 2.3.2 Tags para links

Um outro elemento interessante e extremamente necessário na web é o \<a>, que significa anchor/âncora. Representa um hyperlink, interliga vários conteúdos e páginas na web.

O elemento a tem vários atributos, mas vamos focar em dois:

* O **href** representa o hyperlink para onde sua âncora aponta, pode ser uma página do seu ou de outro site, um e-mail e até mesmo um telefone, os dois últimos precisam dos prefixos mailto: e tel:, respectivamente.
* O **target** neste momento vai servir para nos ajudar a abrir nossos links em outra aba do navegador usando o valor **_blank**.

Uma âncora pode ser uma imagem ou um texto, basta colocar o elemento entre as tags de abertura e fechamento, da seguinte forma:

```html
    <p>
        Lorem ipsum dolor sit amet,<a href="seu link” target="_blank">consectetur adipiscing\</a>  
    </p>

```

---

### 2.4 Como inserir imagens em seu site

#### 2.4.1 Tag img

O elemento \<img> não possui tag de fechamento.

É bem simples e tem apenas 2 atributos próprios:
**src**, que representa a origem (fonte) da imagem e **alt**, o texto alternativo à imagem caso não seja possível exibi-la.

* O atributo alt não é obrigatório, mas é altamente recomendado.

```html
<img>
<img src=”url da imagem”>
<img alt=”descrição da imagem”>
```

>Dica: para fazer refência a uma imagem que está na mesma pasta que o código HTML use: \<img src="./nome-da-imagem.jpg">

---

### 2.5 Como organizar listas com HTML

#### 2.5.1 Tags li, ul e ol

Listas servem para agrupar coleções de itens.

\<ul> representa uma lista em que a ordem dos itens não é importante (uma lista desordenada).

* Item 1
* Item 2

\<ol> representa uma lista em que a ordem dos itens é importante (uma lista ordenada).

1. Item 1
2. Item 2

\<li> é um item dentro de uma lista.

---

### 2.6 Introdução e conceitos básicos do CSS3

#### 2.6.1 Introdução ao CSS3

Objetivos:

* O que são seletores;
* Conceitos básicos;
* Principais seletores CSS.

A linguagem de estilo que conhecemos por CSS foi criada em 1996. A sintaxe é simples e pode ser resumida com a frase: “Você cria regras de estilo para elemento ou grupos de elementos”.
Uma regra CSS é formada por um seletor (ou grupo de seletores, que são os elementos HTML.

![Estrutura CSS](./2.6.1_imagem1-estrutura.png "Estrutura CSS")

As declarações ficam contidas em um par de chaves, e são formadas por uma propriedade e um valor. No exemplo acima, a cor dos elementos foi mudada para azul e o tamanho da fonte, para 14 pixels.

O seletor nesse primeiro exemplo é um seletor de tipo, pois ele representa um elemento HTML.

Com **IDs** e **Classes** é possível representar qualquer tipo de elemento, mas há algumas diferenças entre eles:

* ID: é representado pelo símbolo # (hash) seguido de um nome.
  * Cada ID é único e é uma boa prática não usar IDs em excesso.
* Classe: a classe é representada de forma parecida do ID, mas é precedida por um ponto em vez do #.

E a diferença mais importante entre eles é a forma como devem ser usados: o ID só pode ser usado uma vez em uma página HTML enquanto a classe não tem restrições.

#### 2.6.2 Conceitos básicos

O navegador representa cada elemento HTML  como uma caixa retangular, a partir de um box-model. Com o CSS é possível alterar a aparência dessa caixa (largura, altura, cor de fundo, etc.).

A caixa é composta por 4 áreas: o conteúdo, o padding, a borda e a margem.

* As **margens (margin)** são espaçamentos entre elementos;
* As **bordas (border)**;
* O **padding** é um espaçamento entre as bordas e o conteúdo, a diferença para as margens é que declarações de imagem de fundo funcionam nele;
* O **conteúdo (content)** é o que o seu bloco representa, um texto, uma imagem, um vídeo;

---

### 2.7 Estilizando elementos, textos e listas

#### 2.7.1 Estilizando elementos

Padding e Margin
Anteriormente usamos o padding e o margin da forma mais básica, com apenas um valor, mas, se quisermos atribuir tamanhos diferentes para cada lado do box nós podemos, e vamos ver três formas de fazer isso.

* A primeira, é colocando um valor para as partes superior e inferior (10px) e depois para os lados esquerdo e direito (5px).

```css
padding: 10px 5px;
```

* A segunda forma é dando valores para cada lado do box.

```css
padding: 15px 10px 5px 0px;
```

Uma boa dica também é que quando o valor for 0 não precisamos não precisamos colocar a unidade.

* A terceira forma é com as propriedades específicas para cada lado, até agora tínhamos visto atalhos para essas propriedades.

```css
padding-top: 15px;
padding-right: 10px;
padding-bottom: 5px;
padding-left: 0;
```

Essa opção é mais usada quando temos o mesmo valor para 3 lados, e o quarto precisa ter um valor diferente.

**Background** é um atalho para várias propriedades, e uma boa opção de leitura é a documentação do **[MDN](https://developer.mozilla.org/pt-BR/)** (Mozilla Development Network).

A primeira forma de especificar a cor de fundo é pelo nome da cor em inglês, a segunda é pelo código hexadecimal e a terceira é usando apenas o atalho background.

**Border** é uma propriedade que pode ter 3 valores: a largura, a cor e o estilo, mas existem algumas particularidades nisso.

A largura pode ser usada com várias unidades, como px, em e mm.

A cor pode ser atribuída pelo nome ou por um código hexadecimal, assim como o background.

O estilo é representado por palavras-chave, vamos ver algumas delas:

* solid: mostra uma borda simples e reta;
* dotted: são bolinhas com um pequeno espaçamento entre elas;
* dashed: forma uma linha tracejada.

Existem propriedades específicas para cada aspecto de uma borda, border-width para a largura, border-color para a cor e border-style para o estilo.

É possível juntar os lados com os aspectos de uma borda e criar uma regra mais específica ainda.

**Border-radius** é a última propriedade, e permite arredondar os cantos de um elemento. É possível usar várias unidades, mas as mais comuns são os pixels e a porcentagem.

Colocando apenas um valor, todos os cantos do elemento são modificados, mas seguindo aquela mesma ordem do padding e margin (topo, direita, inferior e esquerda) é possível alterar cada canto separadamente.

#### 2.7.2 Estilizando textos

**font-family** altera a fonte dos textos.

Dê preferência às fontes seguras, chamadas de web safe fonts. Elas recebem esse nome pois são encontradas em quases todos os sistemas e podem ser usadas sem preocupação.

**font-size** muda o tamanho do texto.

**font-style** é usado para mudar o estilo do texto, deixando ou não em itálico.

**font-weight** é usado para mudar o peso do texto, deixando ou não em bold.

**text-transform** muda o texto entre maiúsculas e minúsculas.

* uppercase: todas maiúsculas;
* louwercase: todas minúsculas;
* capitalize: primeira letra de todas as palavras maiúscula.
text-decoration acrescenta linhas ao texto.
* underline: abaixo;
* overline: acima;
* line-trough: no meio.

#### 2.7.3 Estilizando listas

Existem listas ordenada e não ordenadas, como visto no curso de HTML5.
Para alterar o estilo dos marcadores dessas listas, utiliza-se:

```css
list-style-type
```

---

### 2.8 Dimensão e Alinhamento

#### 2.8.1 Propriedades de dimensões e alinhamento

* Width (largura)
* Height (altura)

* Max-width (largura máxima)
* Max-height (altura máxima)

* **Margin** estabelece o espaçamento entre o box model e os elementos externos.

* Text align é a propriedade de alinhamento de texto.

### Referências

---

As anotações aqui apresentadas foram desenvolvidas com base no Bootcamp "Geração Tech Unimed-BH", da plataforma de estudos **[DIO](https://web.dio.me/home)**.

---