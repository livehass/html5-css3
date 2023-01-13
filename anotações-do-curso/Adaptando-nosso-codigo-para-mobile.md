# as adaptações necessárias para que o site seja visualizado corretamente em dispositivos móveis. Hoje em dia, a maior parte do fluxo de usuários na internet é proveniente de celulares, portanto um site não responsivo a tal necessidade é um problema.

Para testarmos a usabilidade do site, abriremos a ferramenta do desenvolvedor por meio do atalho "Ctrl + Shift + I" . No painel de ferramentas, teremos um ícone que representa tablets e celulares, a "Toggle device toolbar" , que também pode ser acessada pelo atalho "Ctrl + Shift + M".

![exemplo de como fica](https://caelum-online-public.s3.amazonaws.com/1310-html5-css3-parte4/06/6_1_1_ferramenta+do+de.png)

No momento em que habilitamos essa opção, nosso site passa a se comportar como se estivesse sendo visualizado via celular: o conteúdo é compartimentando em 940px, o mínimo para esse tipo de plataforma. Atualmente, temos alguns problemas nesse tipo de visualização: a logo marcar está pequena,o menu está pouco legível assim como o conteúdo da lista de benefícios.

![exemplo de como fica](https://caelum-online-public.s3.amazonaws.com/1310-html5-css3-parte4/06/6_1_2_mobile.png)

Primeriamente, precisamos compreender quantos pixels existem na tela para trabalhamos em uma melhor exibição. Atualmente, nossa tela se adapte ao tamanho disponibilizado pelo navegador, sendo o mínimo 940px. No caso de celulares o panorama é diferente: mesmo que a resolução do dispositivo seja de 2000px de largura, a quantidade de pixels existentes na tela sempre será diferente. Esses valores são chamados de DPI, isto é, a densidade de pixels por polegada.

Geralmente, os celulares possuem 320px de largura de tela,alguns maiores oscilam entre 350px e 480px. Portanto se o mínimo é 940px, teremos um valor discrepante. Uma informação crucial é saber quantos pixels possui a tela do usuário.

Trabalharemos com uma nova tag <meta>, mas dessa vez com propriedade e valor name="viewport" embutidas. Queremos, ainda, saber a largura do dispositivo, e para isso usaremos a propriedade content com o valor width=device-width.
```scss
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width">
    <title>Barbearia Alura</title>
    <link rel="stylesheet" href="style-home.css">
    <link href="https://fonts.googleapis.com/css?family=Montserrat&display=swap" rel="stylesheet">
</head>
```
Ao reabrirmos o navegador, veremos que o site se comporta de maneira diferente. A forma como os elementos etão distribuídos em relação ao fundo, o conteúdo é de 940px, mas a visualização mobile é de 375px, que corresponde a um IphoneX. Na pare superior da tela ainda podemos rotacionar a tela para horizontal e ver como a página se comporta.

![exemplo de como fica](https://caelum-online-public.s3.amazonaws.com/1310-html5-css3-parte4/06/6_1_3_fundo+novo.png)

Precisaremos, então, adaptar o CSS para que ele funcione nessa tela. Precisamos entregar para telas até 450px um estilo diferente, e faremos isso por meio de media queries. Perguntaremos ao navegador qual é o tamanho da tela em questão e, se for aquele que desejamos, entregaremos o estilo correto.

Para realizar isso, utilizaremos o @media, com o valor do tipo de tela screen e a pesquisa. Todas as telas que tenham até 450, terão esse estilo diferente, reescrito. Para exempliciar, colocaremos no background um estilo da cor vermelha.
```scss
@media screen and (max-width: 480px) {
    body {
        background: red;
    }
}
```
![exemplo de como fica](https://caelum-online-public.s3.amazonaws.com/1310-html5-css3-parte4/06/6_1_4_tela+vermelha.png)

