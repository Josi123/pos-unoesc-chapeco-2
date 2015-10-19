#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Alessandro Biessek
### Artigo de revisão de CSS3

##### Funcionalidade: animation
##### O que é?
É uma propriedade que permite a criação de animações com css, dispensando em muitos casos a utilização de outra linguagem para animar estilos de elementos. 
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
//definir uma animação: (onde 'name' é o nome da animação)
@keyframes[name] {
	[keyframes-selector(from=0%,to=100%,0-100%)] {
		[css-styles]
	}
}

[classe,id,elemento] {
	animation: name duration timing-function delay iteration-count direction fill-mode play-state;
	// ou cada sub-propriedade:
	animation-name: name|none|initial|inherit;
	animation-duration: time|initial|inherit;
	animation-timing-function: linear|ease|ease-in|ease-out|cubic-bezier(n,n,n,n)|initial|inherit;
	animation-delay: time|initial|inherit;
	animation-iteration-count: number|infinite|initial|inherit;
	animation-direction: normal|reverse|alternate|alternate-reverse|initial|inherit;
	animation-fill-mode: none|forwards|backwards|both|initial|inherit;
	animation-play-state: paused|running|initial|inherit;
}
```
##### Exemplo de uso

```css

@keyframes diagonal-slide {
  from {
    left: 0;
    top: 0;
  }
  to {
    left: 100px;
    top: 100px;
  }
}

div {
  animation-name: diagonal-slide;
  animation-duration: 5s;
  animation-iteration-count: 10;
}

```
### Referencia:
[http://www.w3schools.com/cssref/css3_pr_animation.asp](http://www.w3schools.com/cssref/css3_pr_animation.asp)
[http://www.w3.org/TR/css3-animations/#animation](http://www.w3.org/TR/css3-animations/#animation)

##### Funcionalidade: calc()
##### O que é?
Função para realizar calculos aritméticos simples diretamente no css.
##### Onde usar:
Qualquer propriedade com valor numérico (<length>, <frequency>, <angle>, <time>, <number>, or <integer>).
##### Como usar:
```css
	[propriedade]: calc([expressão]) 
```
##### Exemplo de uso

```css
	div {
		width: calc(100% - 80px);
	}
```
### Referencia:
[https://developer.mozilla.org/en-US/docs/Web/CSS/calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)
[http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/](http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/)

##### Funcionalidade: gradients
##### O que é?
Permite que os designers web e desenvolvedores criarem transições mais agradaveis entre cores sem apelar para imagens.
##### Onde usar:
Qualquer propriedade com valor de cor.
##### Como usar:
```css
// gradiente linear:
[propriedade]: linear-gradient(direction<to bottom, to top, to right, to left, to bottom right, etc.>, color-stop1, color-stop2, ...);
```
##### Exemplo de uso

```css
	div {
		background: linear-gradient(to bottom, blue, white);
	}
```
### Referencia:
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients)
[http://www.w3schools.com/css/css3_gradients.asp](http://www.w3schools.com/css/css3_gradients.asp)

##### Funcionalidade: media queries
##### O que é?
Permite a criação de configurações de estilo diferentes e direcionadas para determinadas mídias(celular, tv, computador).
##### Onde usar:
Qualquer definição de classe.
##### Como usar:
```css
// Apenas encapsula uma definição de classe normal.
// tipo básico, pode ser adicionado mais expressões, utilizando media_features
@media [all | aural | braille | handheld | print | projection | screen | tty | tv | embossed]  { 
	[elemento| classe | id] { 
  		[atributo]: [valor]; 
	}	 
}
```
##### Exemplo de uso

```css
@media screen {
  .top-bar {
    display: none;
  }
}
```
### Referencia:
[https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)

##### Funcionalidade: columns
##### O que é?
O layout baseado em colunas já faz parte da estrutura do css. Anteriormente eram feitas gambiarras até do lado servidor para dividir o conteúdo em colunas.  Ainda não possui suporte total dos navegadores.
##### Onde usar:
Elementos de container.
##### Como usar:
```css
[seletor] {
	// shorthand
	columns: [auto|column-width column-count|initial|inherit];
	// ou definido as subpropriedades
	column-count: [number|auto|initial|inherit];
	column-fill: [balance|auto|initial|inherit];
	column-gap: [length|normal|initial|inherit];
	column-rule: [column-rule-width column-rule-style column-rule-color|initial|inherit];
	column-rule-color: [color|initial|inherit];
	column-rule-style: [none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit];
	column-rule-width: [medium|thin|thick|length|initial|inherit];
	column-span: [1|all|initial|inherit];
	column-width: [auto|length|initial|inherit];
}

```
##### Exemplo de uso

```css
div {
   -webkit-column-width: 100px; /* Chrome, Safari, Opera */
    column-width: 100px;
}
```
### Referencia:
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)

##### Funcionalidade: web fonts
##### O que é?
Regra que permite a utilização de fontes que não estejam instaladas na máquina do usuário.
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
@font-face {
    font-family: [name]; // nome da fonte
    src: url([url_arquivo_fonte]); //url para o arquivo da fonte.
    font-stretch: [normal|condensed|ultra-condensed|extra-condensed|semi-condensed|expanded|
				   semi-expanded|extra-expanded|ultra-expanded];
	font-style:	 [normal|italic|oblique];
	font-weight: [normal|bold|100|200|300|400|500|600|700|800|900];
	unicode-range:	[unicode-range] // quais caracteres UNICODE a font suporta. 
}
```
##### Exemplo de uso

```css
@font-face {
    font-family: fonteLegal;
    src: url(fonte_legal.ttf);
    font-weight: bold;
}
```
### Referencia:
[http://www.w3schools.com/css/css3_fonts.asp](http://www.w3schools.com/css/css3_fonts.asp)

##### Funcionalidade: 3D Transforms
##### O que é?
Permite estilizar elementos usando transformações 3D.
##### Onde usar:
Todos os elementos html. 
##### Como usar:
```css
seletor {
	// rotação
    -webkit-transform: [rotateX([angulo_rotacao]) | rotateY([angulo_rotacao]) | rotateZ([angulo_rotacao])]; /* Chrome, Safari, Opera */
    transform: [rotateX([angulo_rotacao]) | rotateY([angulo_rotacao]) | rotateZ([angulo_rotacao])] ;

    // transformação em perspectiva
    -webkit-perspective: [length|none];
    perspective: [length|none];


}
```
##### Exemplo de uso

```css
div {
	// rotação
    -webkit-transform: rotateY(130deg); /* Safari */
    transform: rotateY(130deg);

    // perspectiva
    -webkit-perspective: 500px; /* Chrome, Safari, Opera */
    perspective: 500px;
}
```
### Referencia:
[http://www.w3schools.com/css/css3_3dtransforms.asp](http://www.w3schools.com/css/css3_3dtransforms.asp)

##### Funcionalidade: text-overflow
##### O que é?
Especifica como um conteúdo que exceda seu espaço deve ser exibido(cortado, com reticências.)
##### Onde usar:
Todos os elementos html. 
##### Como usar:
```css
seletor {
    text-overflow: [clip|ellipsis|string|initial|inherit];
}
```
##### Exemplo de uso

```css
// o texto presente nesta div mostrará reticencias no final se o tamanho do conteúdo for maior que seu tamanho.
div {
     text-overflow: ellipsis; 
}
```
### Referencia:
[http://www.w3schools.com/cssref/css3_pr_text-overflow.asp](http://www.w3schools.com/cssref/css3_pr_text-overflow.asp)

##### Funcionalidade: RGBA
##### O que é?
Capacidade de adicionar o canal alfa à uma cor, anteriormente RGB. Simplifica o controle de opacidade de elementos.
##### Onde usar:
QUalquer propriedade de cor. 
##### Como usar:
```css
seletor {
    [propriedade_cor]: rgba([red,green,blue,alpha]);
}
```
##### Exemplo de uso

```css
// o texto presente nesta div mostrará reticencias no final se o tamanho do conteúdo for maior que seu tamanho.
div {
     background-color: rgba(255,255,255,0.5); // alpha|opacidade de 50%.
}
```
### Referencia:
[http://tableless.com.br/css3-breve-introducao-a-rgba/](http://tableless.com.br/css3-breve-introducao-a-rgba/)

##### Funcionalidade: novos seletores por atributo
##### O que é?
Além de outros seletores adicionados, este possibilita selecionar elementos baseado nos seus atributos. 
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
	[elemento][attr^=val] // todos os elementos com atributo 'attr' e valor iniciando em 'val'
	[elemento][attr$=val] // todos os elementos com atributo 'attr' e valor terminando em 'val'
	[elemento][attr*=val] // todos os elementos com atributo 'attr' e valor contendo em 'val'
```
##### Exemplo de uso

```css
	//selecionando todas as imagens com a extensão jpg.
	img[src$=".jpg"]  {
		...
	}
```
### Referencia:
[http://www.w3schools.com/cssref/css_selectors.asp](http://www.w3schools.com/cssref/css_selectors.asp)
