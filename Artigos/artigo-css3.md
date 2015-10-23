------ INICIO do artigo ------ 
#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Guilherme Mendes Senger
### Artigo de revisão de CSS3
##### Funcionalidade: transform
##### O que é?
As transformações em CSS3 permitem alterar a posição, girar, torcer/inclinar e aumentar ou diminuir os elementos, permitindo assim mudar sua forma, tamanho e posição, suportando 2D e 3D.
##### Onde usar:
Em qualquer elemento do tipo transformable, cujo layout é controlado pelo CSS box model.
##### Como usar:
As transformações 2D são:
```css
/* translate: move o elemento no eixo X (à direita) e Y (abaixo) em pixels */
seletor {
  transform: translate(x,y);
}
/* rotate: gira o elemento em X graus em sentido horário (positivo) ou anti-horário (negativo) */
seletor {
  transform: rotate(angle);
}
/* scale: aumenta ou diminui o tamanho original do elemento no número de vezes informado para a largura e 
altura */
seletor {
  transform: scale(x,y);
}
/* skewX: torce ou inclina o elemento no eixo X, conforme o ângulo informado */
seletor {
  transform: skewX(angle);
}
/* skewY: torce ou inclina o elemento no eixo Y, conforme o ângulo informado */
seletor {
  transform: skewY(angle);
}
/* skew: torce ou inclina o elemento no eixo X e Y, conforme os ângulos informados */
seletor {
  transform: skew(x-angle,y-angle);
}
/* matrix: combina todos os métodos anteriores em um só, passando 6 parâmetros representando uma matriz que 
será utilizada para transformar o elemento */
seletor {
  transform: matrix(n,n,n,n,n,n);
}
```

As transformações 3D são:

```css
/* rotateX: gira o elemento no eixo X, conforme o ângulo informado */
seletor {
  transform: rotateX(angle);
}
/* rotateY: gira o elemento no eixo Y, conforme o ângulo informado */
seletor {
  transform: rotateY(angle);
}
/* rotateZ: gira o elemento no eixo Z, conforme o ângulo informado */
seletor {
  transform: rotateZ(angle);
}
```

##### Exemplo de uso
O exemplo abaixo combina as duas funcionalidades vistas até agora, exibindo um elemento div vermelho de 100 x 100 px, adicionando um efeito de transição nas propriedades with e height com duração de 2 segundos e uma transformação com duração de 2 segundos.

```css
div {
  width: 100px;
  height: 100px;
  background: red;
  transition: width 2s, height 2s, transform 2s;
}
```

O efeito inicia ao passar o mouse sobre o elemento, conforme o exemplo abaixo, aumentando, girando e inclinando a imagem:
```css
div:hover {
  width: 300px;
  height: 300px;
  transform: rotate(180deg) skewX(-5deg);
}
```






##### Funcionalidade: resize
##### O que é?
Permite ao usuário redimensionar um elemento HTML.
##### Onde usar:
Qualquer elemento.
##### Como usar:
```css
seletor {
  resize: none|both|horizontal|vertical|initial|inherit;
}
```

##### Exemplo de uso
Permite ao usuário aumentar ou reduzir a altura do elemento div.

```css
div {
  resize: vertical;
}
```




##### Funcionalidade: backgrounds
##### O que é?
Conjunto de propriedades para configurar o fundo de um elemento, sendo possível adicionar múltiplas imagens:
background-image - imagem ou imagens a serem exibidas.
background-position - posição da imagem no fundo.
background-repeat - define se a imagem será repetida até preencher o espaço.
background-size- tamanho da imagem a ser exibida.
background-origin - define a origem da posição da imagem.
background-clip - define a área de desenho da imagem.
##### Onde usar:
Em qualquer elemento que seja deseja exibir uma imagem de fundo.
##### Como usar:
```css
seletor {
  background-image: url|none|initial|inherit;
  background-size: auto|length|cover|contain|initial|inherit;
  background-origin: padding-box|border-box|content-box|initial|inherit;
  background-clip: border-box|padding-box|content-box|initial|inherit;     
}
```

##### Exemplo de uso
A imagem cobrirá toda a janela do browser, centralizada e mantendo a proporção original, sem barras de rolagem.

```css
html {
  background: url(img_flower.jpg) no-repeat center center fixed;
  background-size: cover;
}
```




##### Funcionalidade: border images
##### O que é?
Utilizar uma imagem como borda de um elemento, definindo como a imagem será cortada e se as seções do meio da borda deverão esticar a imagem ou repeti-la. A imagem sempre será cortada em nove pedaços: quatro cantos, quatro lados e um centro.
##### Onde usar:
Em qualquer elemento que suporte a propriedade border.
##### Como usar:
```css
seletor {
  border: border-width border-style border-color|initial|inherit;
  border-image: source slice width outset repeat|initial|inherit;
}
```

##### Exemplo de uso
A imagem será cortada em pedaços de 30 pixels, que serão ajustados automaticamente para preencher toda a extensão da borda do elemento.

```css
#borderimg { 
  border: 10px solid transparent;
  padding: 15px;
  border-image: url(border.png) 30 round;
}
```


##### Funcionalidade: Text Shadow
##### O que é?
A propriedade text-shadow destina-se a definir sombras em textos.
##### Onde usar:
Em qualquer elemento que possui o atributo text.
##### Como usar:
```css
seletor { propriedade: offsetX offsetY raioBlur cor [,offsetX offsetY raioBlur cor];}
```
Os valores de raioBlur e cor são opcionais.

##### Exemplo de uso
A sintaxe geral para aplicar sombreamento em textos é mostrada a seguir.

```css
seletor { 
      text-shadow: 0 0 0 0 none;
}
```



##### Funcionalidade: Cores RGBA
##### O que é?
A propriedade RGBA destina-se a definir cores e transparência com uso de valores RGB (sistema de cores formado por Red, Green e Blue).
##### Onde usar:
Em qualquer elemento que possui propriedades de cor. Exemplos: color, background, border-color, etc.
##### Como usar:
```css
seletor { propriedade: rgba(R, G, B, A); }
```

##### Exemplo de uso
A sintaxe geral para aplicar cores e transparência RGB é mostrada a seguir.

```css
seletor { 
      background: rgba(0, 0, 0, 1);
}
```


##### Funcionalidade: Cores HSLA
##### O que é?
A propriedade HSLA destina-se a definir cores e transparência com uso de valores para matiz (Hue), saturação (Saturation) e luminosidade (Lightness).
##### Onde usar:
Em qualquer elemento que possui o atributo background.
##### Como usar:
```css
seletor { propriedade: hsla(H, S, L, A); } 
```

##### Exemplo de uso
A sintaxe geral para aplicar cores e transparência é mostrada a seguir.

```css
seletor { 
     background: hsla(0, 0%, 0%, 1); 
}
```


##### Funcionalidade: Gradiente
##### O que é?
Gradientes permitem exibir transições suaves entre duas ou mais cores especificadas.
##### Onde usar:
Em qualquer elemento que contém o atributo background.
##### Como usar:

Existem dois tipos de gradientes: linear (são definidas pelo menos duas cores de parada) e radial (é definido pelo seu centro).

```css
seletor { propriedade: linear-gradient(direction, color-stop1, color-stop2, ...);}
seletor { propriedade: radial-gradient(shape size at position, start-color, ..., last-color);}
```

##### Exemplo de uso
A sintaxe geral para aplicar gradiente (linear e radial) pode variar conforme o navegador utilizado. Abaixo são exibidas sintaxes para alguns navegadores.

```css
seletor {
  background: -webkit-linear-gradient(red, blue); /* For Safari 5.1 to 6.0 */
  background: -o-linear-gradient(red, blue); /* For Opera 11.1 to 12.0 */
  background: -moz-linear-gradient(red, blue); /* For Firefox 3.6 to 15 */
  background: linear-gradient(red, blue); /* Standard syntax */
}
seletor {
  background: -webkit-radial-gradient(red, green, blue); /* Safari 5.1 to 6.0 */
  background: -o-radial-gradient(red, green, blue); /* For Opera 11.6 to 12.0 */
  background: -moz-radial-gradient(red, green, blue); /* For Firefox 3.6 to 15 */
  background: radial-gradient(red, green, blue); /* Standard syntax */
}
```


##### Funcionalidade: Expressões Matemáticas
##### O que é?
A função calc() permite que se definam valores css com uso de expressões matemáticas, ou seja, o valor adotado para a propriedade é o resultado de uma expressão matemática.
##### Onde usar:
Em qualquer elemento que possui atributos numerados (podendo ser em pixels ou %).
##### Como usar:

Os operadores matemáticos válidos são: + (soma), - (subtração), * (multiplicação) e / (divisão). As unidades de medida css válidas na expressão matemática são as unidades css para: comprimento, ângulo, tempo, frequência e números inteiros e fracionários. Na expressão matemática que define o valor css é permitido que sejam misturadas diferentes unidades de medida. A sintaxe geral para uso desta função é conforme mostrada a seguir:

```css
seletor { propriedade: calc(expressão matemática); }
```

##### Exemplo de uso
A sintaxe geral para aplicar expressões matemáticas nos atributos é mostrada a seguir.

```css
seletor {
width: calc(100% - 100px); 
}
```



##### Funcionalidade: Transform 2D – Rotate
##### O que é?
Essa transformação causa a rotação de um elemento. A rotação deve ser expressa em medida css para ângulos, ou seja, deg, grad, rad e turn.
##### Onde usar:
Em qualquer elemento que possui o atributo transform.
##### Como usar:

Valores positivos causam rotação no sentido horário e valores negativos no sentido anti-horário.

```css
seletor {transform: rotate(adeg); } 
seletor {transform: rotateX(adeg); } 
seletor {transform: rotateY(adeg); } 
seletor {transform: rotateZ(adeg); }
```

##### Exemplo de uso
A sintaxe geral para aplicar rotação é mostrada a seguir.

```css
seletor {
  -webkit-transform: rotate(0deg);
  -moz-transform: rotate(0deg);
  -o-transform: rotate(0deg);
  -ms-transform: rotate(0deg);
  transform: rotate(0deg);
}
```



### Referencia:
[http://www.maujor.com/tutorial/](http://www.maujor.com/tutorial/)</br>
[http://www.w3schools.com/css/default.asp](http://www.w3schools.com/css/default.asp)

<repetir para as demais funcionalidades>

------ FIM do artigo ------
