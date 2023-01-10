- [Curso Alura html5-css3-avancando-css](https://cursos.alura.com.br/course/html5-css3-avancando-css)
# "algumas anotações minhas sobre o curso para estudos." 
## Pseudo-elementos do css3:


Evoluiremos ainda mais em nosso entendimento do CSS, e um dos tópicos do nosso estudo serão os já referidos pseudo-elementos, que não existem no código HTML e são criados via CSS.

### Utilizaremos o título "Nosso estabelecimento" para entendermos as possibilidades do CSS. Se quisermos negritar apenas a primeira letra desse título? Com os conhecimentos que temos até agora, isso seria possível?

Não, pois estudamos seletores avançados de classe, identificadores, mas nada que possibilitasse a marcação de uma única letra. Contudo, essa é uma ação possível graças às atualizações e melhorias no CSS. Na tag titulo-principal, utilizaremos o pseudo-elemento first-letter para definir o peso da fonte.
```scss
.titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
}
```
```scss
.titulo-principal:first-letter {
    font-weight: bold;
}
```
Ao carregarmos a página, teremos a primeira letra do título "Nosso estabelecimento" em negrito, isto é, a letra "N". Outra opção interessante, muito comum no mercado editorial, é configurar a primeira linha para itálico. Para tanto, ajustamos para que todos os parágrafos (p) terão a primeira linha (first-line) no estilo italic.
```scss
p:first-line {
    font-style: italic;
}
```
Conheceremos ainda outros dois pseudo-elementos do CSS: after e before. Esses dois elementos criam espaço para que o CSS atue antes ou depois de um determinado conteúdo. Continuaremos utilizando o título para entender como a sintaxe se dá:

```scss 
.titulo-principal:before {
    content: "[";
}
```

```scss 
.titulo-principal:after {
    content:"]"
}
```
Dessa maneira, ao recarregarmos a página o título estará envolvido por colchetes: "[Nosso estabelecimento]". É interessante mencionar que esse conteúdo - os colchetes - não são selecionáveis pelo mouse, trata-se apenas de uma informação visual e não um conteúdo manipulável. Utilizaremos os caracteres unicode para inserir estrelas na lista da sessão "Benefícios", que trabalhávamos na aula anterior.

Procuraremos no Google por "unicode star" e copiaremos o conteúdo da estrela que acharmos visualmente mais interessante. Em nosso CSS, trabalharemos na classe itens, utilizaremos o pseudo-elemento before para que antes do conteúdo da lista, haja uma estrela.

```scss
 itens:before {
    content: ""
}
```
Ao carregarmos a página, teremos as estrelas marcadas em cada item da lista. Novamente trata-se de um elemento não selecionável, apenas conteúdo de exibição.


#Com os seletores avançados do CSS, podemos selecionar os filhos diretos de <main>, para tanto, utilizaremos o sinal >, e todo os outros parágrafos serão ignorados, afinal são filhos diretos da <section> e não de <main>.
```scss
main > p {
    background: red; 
}
```
Mas como selecionar o primeiro parágrafo que sucede uma imagem, por exemplo? Conseguimos selecionar o primeiro filho com o seletor que acabamos de conhecer, mas neste caso estamos falando do primeiro irmão que vem depois de um elemento.

Neste caso, usamos img como elemento âncora e para o primeiro irmão usamos o sinal de "+"

```scss
img + p { 
    background: blue;
}
```
Para selecionar todos os parágrafos localizados depois de uma imagem usamos o seletor "~"
```scss
img ~ p {
    background: yellow
} 
```
É importante lembrar que um seletor pode sobrescrever o outro, pois todos possuem a mesma força. Os seletores avançados nos ajudam a criar estilos mais complexos e utilizar o CSS de uma maneira incrível, com uma autonomia maior do HTML.

No CSS podemos, inclusive, excluir itens específicos. Se quisermos excluir todos os parágrafos que não compõe missao, escreveremos:
```scss
.principal p:not(#missao) {
    background: orange;
}
```
A exclusão é um elemento poderoso no CSS, principalmente quando realizamos manutenção em algum código que já existe e que não devemos modificar tanto o HTML.

[Proxima pagina- Calculos basicos em css](https://github.com/livehass/html5-css3/blob/main/calculosbasicoscss.md)
