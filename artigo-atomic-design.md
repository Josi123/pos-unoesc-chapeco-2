Atomic Design

Alessandro Biessek (Unoesc Chapecó)
{alessandrobiessek@gmail.com}

Resumo:

Atomic design é uma metodologia composta por cinco estágios que juntos, coperam para a criação de layouts através de sistemas de interface modulares. Tendo como objetivo o estabelecimento de padrões para criação de sistemas de design, aumento de produtividade, redução de erros e retrabalho.

1) O que é?

Uma metodologia criada e conceituada por Brad Frost para mudança no paradigma na criação de páginas web. Basicamente, a ideia é que pode-se partir de algo abstrato para criar algo concreto.
Para justificar o nome de Design Atomico baseia-se na ideia de que as interfaces são compostas de diversos elementos, assim como a matéria. Então, como a matéria pode ser quebrada em átomos, a interface também pode ser decomposta em pequenos blocos.

2) Como funciona

Iniciando dos "átomos" da web que seriam as tags html que como elementos isolados não possuem significado algum, por exemplo, *labels*, *inputs*. Quando agrupados formam moléculas e cooperam para fazer algo juntos, um exemplo básico seria a combinação dos "átomos" `<label>` e `<input>` numa molécula `<form>`. Apartir daí, tais "moléculas" podem ser combinadas para formar organismos, que já seria algo mais complexo e concreto em relação às moléculas. Nesta analogia química os organismos por sua vez dão forma ao todo. Para manter a eficiência da metodologia, a etapa final ainda se concentra em dois pontos, o template e a página em sí. O template é um modelo de página que combina diversos organismos e são concretos, pois dão um contexto às moléculas antes apenas agrupadas. Finalizando a evolução do abstrato ao concreto, temos a página que é efetivamente uma instância de um template, concreta e contextualizada.

3) Para que usar

O Atomic Design propõe uma forma mais limpa e clara de se organizar projetos web, que atualmente são feitos de diversas formas, sem um determinado padrão. Além disso possibilita que se caminhe da concepção abstrata até a concretização da ideia de forma organizada e linear, onde se entende cada parte de uma página, cada "organismo" e sua determinada função. Como é pensado de forma modular é muito mais fácil tratar um "organismo" defeituoso por exemplo, ou mesmo aperfeiçoá-lo sem interferir no todo de forma abrupta. 

4) Onde usar?

Pode ser utilizado na criação de componentes, frameworks e sistemas web.
O conceito é bem simples, principalmente pela analogia com a química, mas muito amplo e efetivo.Particularmente, acredito que se assemelha a conceitos básicos de engenharia de software, metodologias ágeis e dessa forma pode ser aplicado em todo desenvolvimento de software, componentes, frameworks, independente da plataforma, basta extrair a ideia básica, e pode-se obter muitos benefícios.


5) Exemplos:

5.1 Átomos:
São os elementos mais simples que sozinhos não teriam significado importante.
```html
<!--Um simples label-->
<label>Apenas um label</label>

<!--Um simples input-->
<input type="button" name="Button" value="Button">
```
5.2 Moléculas:
São combinações de átomos, dando algum sentido à eles.
```html
<form>
	<label>Apenas um label</label>
	<<input type="text" name="busca" value="busca" placeholder="busca">
	<input type="button" name="Button" value="Button">
</form>
```
5.3 Organismos:
São combinações de moléculas, isto já é algo concreto.
```html
<!--Combina as moléculas de busca e navegação-->
<header>
	<img src="logo.png">
	<<nav>
		<ul>
			<li><a href="" title=""></a></li>
			<li><a href="" title=""></a></li>
			<li><a href="" title=""></a></li>
		</ul>
	</nav>
	<div>
		<label>Busca no site</label>
		<input type="button" name="Button" value="Button">
	</div>
</header>
```
5.4 Templates:
Onde a analogia com a química acaba :/ 
Um modelo de página concreta.

![Template](img_artigo/template.jpg)

5.4 Páginas:

Uma página pronta, a visão de algo tangível.

![Página](img_artigo/pagina.jpg)


6) Referências

http://bradfrost.com/blog/post/atomic-web-design/
http://habaneroconsulting.com/insights/what-is-atomic-design#.ViRBJfmrTIU
http://tableless.com.br/o-que-e-design-atomic/