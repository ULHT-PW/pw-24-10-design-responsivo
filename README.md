# pw-24-10-design-responsivo
Universidade Lusófona
**Programação Web**

# Ficha 10: Design responsivo com CSS grid, flex e media queries

### Objetivo:
* Familiarizar-se com a propriedade display:flex e display:grid para renderizar elementos e criar layouts 
* familiarizar-se com o design responsivo com media-queries
* Irá aplicar estas técnicas nas aplicações que desenvolveu (Bandas, Artigos e Curso). 

### Antes de iniciar a ficha:
* veja o video-tutorial [Construindo um layout com CSS grid](https://educast.fccn.pt/vod/clips/1qib570kz7/streaming.html?locale=pt)
* veja o video-tutorial [Criando um layout responsivo com media query](https://educast.fccn.pt/vod/clips/23dbqe9keb/streaming.html?locale=pt)
* veja os slides [Propriedades display flex e grid](https://moodle.ensinolusofona.pt/pluginfile.php/615262/course/section/443400/pw-24-11-css-propriedades-display-flex-grid.pptx?time=1715594981506) 
* veja os slides [Design responsivo](https://moodle.ensinolusofona.pt/pluginfile.php/615262/course/section/443400/pw-24-11-css-propriedades-display-flex-grid.pptx?time=1715594981506)

# Estilização do layout base
* estilize o layout base da sua aplicação com a propriedade CSS display:grid, flex, e usando media queries, garantindo que fica bem renderizado quando visualiza no telemóvel.

# Estilização das páginas das aplicações
* estilize o layout das páginas das aplicações, usando a propriedade CSS display:flex.
* em especial, quando lista vários elementos, liste-as usando flex, com flex-directon: column, de modo a que fiquem uns por baixo dos outros.
* Quando lista elementos, inclua uma fotografia


## Seletores CSS
* Para cada um dos selectores class, id, atributo, pseudo-classe e pseudo-elemento, deverá ter pelo menos 3 regras de cada (3 classes, 3 ids, etc) que apliquem estilos em sítios diferentes. 
* Utilize pelo menos três combinadores de selectores (descendentes, filhos `>`, adjacentes `~`, imediatamente adjacentes `+`, agrupados `,`). 
* De seguida dão-se algumas sugestões de elementos a estilizar.
 
## Estilização de elementos

#### Fonte
Escolha uma [fonte Google](https://fonts.google.com/) a seu gosto para as páginas da sua aplicação:
* no site, escolha uma fonte que goste
* clique em *add font*
* selecione *get embeded code*
* copie o código da página (três elementos link, como apresentados em baixo para a fonte Montserrat) e insira-os no elemento `<head>` do seu layout.html.
```css
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
```
* insira no seu ficheiro css, uma regra com um selector universal e a declaração `font-family: "Montserrat", sans-serif;` de modo a que a fonte seja usada em todo o lado* Configure a cor de background do seu website, assim como de alguns elementos HTML5 usando seletores adequados. 

#### Menu
* Para o texto do menu, utilize os selectores de pseudo-classe `link`, `visited`, `hover`, `active` para configurar os links utilizando apenas as cores da palete, assim como os selectores `before` e `after` no menu quando passar com o rato por cima.
* Inclua, antes de cada palavra do menu, um icon adequado, usando ícones de Font Awesome. Para tal:
   * visite o [link](https://fontawesome.com/start)
   * registe-se para obter uma chave (por exemplo, `5d1319edfb`), 
   * no elemento head do layout.html, insira um elemento script   
`    <script src="https://kit.fontawesome.com/5d1319edfb.js" crossorigin="anonymous"></script>`
   * utilize [icons](https://fontawesome.com/search?q=music&o=r) a seu gosto. Para um icon à sua escolha (que não seja Pro, exclusivos para subscrições pagas) use no seu HTML o elemento que o identifica, por exemplo<br>`<i class="fa-solid fa-music"></i>`
 

#### Elementos com fundos
 * crie alguns elementos com um padrao ue goste, por exemplo em https://pixabay.com/pt/
* para tal, especifique o background tendo no url o link para a imagem

#### Letras
* adicione, à classe Musica, o campo letra, um TextField. Não se esqueça de especificar os atributos default, null e blank:<br> `letra = models.TextField(default='', null=True, blank=True)`
* garanta que no formulário para inserir uma música aparece o campo letra.
* Insira a letra de pelo menos uma música por disco.
* evidencie, na lista de músicas de um disco, a música que tem letra, usando por exemplo um icon de Font Awesome.
* Na página da música, se existir, insira a letra.

#### Biografia
* adicione, à classe Musica, o campo biografia, um TextField.
* garanta que no formulário para inserir uma música aparece o campo biografia.
* Insira para cada banda uma biografia, peça ao chatGPT uma curta de 4-5 linhas.
* Na página da banda, insira a biografia.
* use selectores pseudo-elementos de first-letter e first-line para estilizar o texto da biografia.

### Fotografia da banda
* estilize as molduras (border) das imagens usando seletores, sem recorrer a classes.
* utilize mais do que uma cor para cada lado, ou só uma borda de cor de um dos lados.

### Formulários
* no forms.py, defina `help_texts` para todos os campos do formulário de nova banda, textos explicativos adicionais para os campos dos seus modelos.
* Exemplo: 
        help_texts = {
            'biografia': 'Insira uma breve biografia de 4-5 linhas.'
        }
* este texto é exibido junto ao campo biografia, no formulário, dentro de um elemento com o atributo `class="helptext"`.
* estilize-os usando CSS (por exemplo, use letras mais pequenas com a propriedade `font-size` e numa cor mais clara).


# Página HTML5 & CSS

* Crie uma nova página HTML `html5-css.html`.
* Insira um elemento `h3` com o título "Seletores CSS" onde deverá incluir:
    1. uma frase introdutória sobre CSS 
    2. uma tabela onde tem, na primeira coluna, todos os tipos de seletores CSS, um por linha. Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google), e na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou, colocando um link. 
* Insira um elemento `h3` com o título "Combinadores de seletores" onde deverá incluir:
    * uma tabela com todos os combinadores de seletores apresentados na aula, um por linha.
    * Na segunda coluna deverá indicar se o usou ou não nalguma página, recorrendo a um icon adequado (use os icones Google)
    * na terceira coluna deverá incluir um breve comentário a explicar como este funciona e onde o utilizou.


# Submissão
* submeta o link para a sua aplicação
