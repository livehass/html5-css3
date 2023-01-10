# gerar opacidade em nossos elementos:
A opacidade é uma camada a mais posta sobre a imagem, como um insulfilme para a janela de carro, que oferece níveis diferentes de proteção contra o Sol.

Utilizaremos a imagem da sessão "Benefícios" para compreendermos o funcionamento da ferramenta de opacidade no HTML. Em index.css , utilizaremos a propriedade opacity que pode ter valores entre 0 a 1, sendo que 0 o elemento estará totalmente oculto. Se quisermos exibir a imagem com opacidade de 30%, ajustaremos o valor da propriedade para 0.3.
```scss
.imagem-beneficios {
    width: 60%
    opacity: 0.3;
}
```
Esse recurso é interessante quando montamos composições visuais com elementos sobrepostos, ou para sugerir interações com o mouse ao utilizarmos o hover. Quando o mouse estiver posicionado sobre a imagem teremos 1 de opacidade.

.imagem-beneficios:hover {
    opacity: 1;
}
Temos ainda o recurso transition, em que podemos estabelecer uma transição da opacidade em determinados milissegundos.
```scss
.imagem-beneficios {
    width: 60%
    opacity: 0.3;
    transition: 400ms;
}
```
Em nosso site, faremos com o que o comportamento padrão da imagem seja de opacidade 1, e no momento em que mouse estiver sobre ela a opacidade será de 0.3, o que irá gerar um belo efeito visual.

Atualmente, podemos utilizar opacidade em todos os elementos e em cores, vamos entender melhor como isso ocorre.

A cor de titulo-principal possui a cor padrão #00000, preto. Como podemos fazer com que essa cor que está em hexadecimal? se torne RGB? Isto é, a mesma cor escrita em outra linguagem? Do seguinte modo:
```scss
.titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
    color: rgb(0,0,0);
}
```
Com CSS 3, podemos utilizar mais uma camada - a de opacidade, chamada alfa - nas cores em RGB. Para tanto, utilizamos o rgbae então definir os valores que quisermos.
```scss
.titulo-principal {
    text-align: center;
    font-size: 2em;
    margin: 0 0 1em;
    clear: left;
    color: rgba(0,0,0,0.3);
}
```
Esse recurso pode ser utilizado em todas as cores: de fundo, texto, borda e assim por diante.