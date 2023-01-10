#cálculos dinâmicos de posicionamento de elementos no CSS, como altura e largura.

Nosso site deve estar preparado para dispositivos com diversos tamanhos de tela. Um grande problema enfrentado ao desenvolver um site harmonioso é justamente calcular a proporção s dimensões dos elementos em diferentes dispositivos.

Clicaremos sobre a imagem de utensílios de barbeiro com o botão direito do mouse, então selecionaremos a opção "Inspecionar" para acessarmos a ferramenta do desenvolvedor.

Em nosso CSS, verificaremos que o tamanho da imagem é de 120px, mas como podemos fazer com que esse tamanho seja proporcional? Basta mudar para percentual, isto é, 20% de largura tendo a tela como referência.

Para que a imagem sempre ocupe a medida correta em outros dispositivos, utilizamos a propriedade calc. O calculo que desejamos realizar é escrito entre parênteses, em que inserimos o primeiro valor, o tipo de operção e o resultado esperado.
```scss
.utensilios {
    width: calc(40% - 26px);
    float: left;
    Margin: 0 20px 20px 

}
```
Dessa forma, foi calculado precisamente 350px de largura para este elemento. É possível encadear quantas operações quisermos, no mesmo modelo de sintaxe.

```scss
.utensilios {
    width: calc(40% - (26px * 4);
    float: left;
    Margin: 0 20px 20px 
}
```
A propriedade calc nos dá o poder de fazer com o que cremos valores proporcionais específicos.

