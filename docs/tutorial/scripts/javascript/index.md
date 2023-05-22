# Javascript

Para desenvolver seu jogo com os scripts na PlayKitJS, é nessesário conhecimentos básicos em Javascript. Esta sessão aborda alguns tópicos com as funcionalidades do Javascript na PlayKitJS.

# Objetos

Na PlayKitJS, existem alguns tipos de objetos dos quais podem ser utilizados para desenvolver seus jogos, entre eles:

- Object: Objeto padrão, usado para criar um player, inimigos, chão, moedas, etc.
- Ball: Similar ao `Object`, porém com uma colisão circular.
- Gui: Elemento da interface.
- Backdrop: Objeto usado para criar cenários e fundos estáticos.

## Object

O object é o objeto padrão que contém colisão com outros objetos e com seus devidos parâmetros:

- sprite: A sprite padão do objeto.
- X: A posição X do objeto na tela.
- Y: A posição Y do objeto na tela.
- largura: A largura do objeto.
- altura: A altura do objeto.
- é_estático: Se o objeto deve permanecer parado.
- pode_rotacionar: Se o objeto pode rotacionar.
- camera: Se a camera vai seguir o objeto.

### Componentes

O object tem componentes simples mas úteis para cada situação.
Para usar os componentes você deve colocar *nome_do_objeto*.*função()*, alguns componentes são váriaveis então você deve usar *nome_do_objeto*.*função*

Aqui os devidas componentes do object:

- .die() - Deleta o objeto
- .canRotate = *false*/*true* - Define se o objeto pode rotacionar
- .flip = *false*/*true* - Inverte a sprite do objeto horizontalmente
- .setSprite("files/sprite.png") - Define a sprite do objeto
- .opacity(0-1) - Define a opacidade do objeto de 0 a 1

```{.js linenums="1" title="Exemplo de criação de um object"}
var nome_do_objeto = new object("sprite", x, y, largura, altura, é_estático, pode_rotacionar, camera);
```

```{.js linenums="1" title="Exemplo com valores"}
var player = new object("sprite.png", 0, 0, 100, 100, false, true, true);
```

## Ball

O ball é similar ao *object* porém nele você define o perímetro - *tamanho* - e não largura e altura.

- sprite: A sprite padão do objeto.
- X: A posição X do objeto na tela.
- Y: A posição Y do objeto na tela.
- perímetro: O tamanho do objeto.
- é_estático: Se o objeto deve permanecer parado.
- pode_rotacionar: Se o objeto pode rotacionar.
- camera: Se a camera vai seguir o objeto.

Aqui os devidas componentes do ball:

- .die() - Deleta o objeto
- .canRotate = *false*/*true* - Define se o objeto pode rotacionar
- .flip = *false*/*true* - Inverte a sprite do objeto horizontalmente
- .setSprite("files/sprite.png") - Define a sprite do objeto
- .opacity(0-1) - Define a opacidade do objeto de 0 a 1

```{.js linenums="1" title="Exemplo de criação de um object"}
var nome_do_objeto = new ball("sprite", x, y, perímetro, é_estático, pode_rotacionar, camera);
```

```{.js linenums="1" title="Exemplo com valores"}
var bola = new ball("sprite.png", 0, 0, 50, false, true, false);
```

## Gui

O gui é um elemento para criar GUI - *Interfaçes* - como exemplo, botões e scrolls e tem seus devidos parâmetros e funções.

- X: A posição X do gui na tela.
- Y: A posição Y do gui na tela.
- largura: A largura do gui.
- altura: A altura do gui.
- cor: A cor do gui.
- tipo: Tipo da gui - *"normal, scroll* -.

### Componentes

Aqui os devidas componentes do gui:

- .content("texto") - Define o texto do gui
- .min = 0 - Define o valor mínimo do gui caso seja um scroll
- .max = 0 - Define o valor máximo do gui caso seja um scroll
- .onClick() - Função de clique, vai ser explicada mais afrente
- .setValue(valor) - Define o valor atual do gui caso seja um scroll
- .isClick - Retorna true se o gui estiver tocado

### OnClick

O onClick é uma função do gui que serve para criar eventos de clique, para usar o onClick você deve criar uma função com ele, aqui um exemplo:

```{.js linenums="1" title="Exemplo"}
botao.onClick = function(){
  //Oque deve ser feito quando o botão for clicado
}
```

## Backdrop

O backdrop serve para criar fundos estáticos e sempre fica atrás de todos os objetos e guis.

- sprite: A sprite padão do gui.
- X: A posição X do gui na tela.
- Y: A posição Y do gui na tela.
- largura: A largura do gui.
- altura: A altura do gui.

Diferente dos demais objetos, o gui começa no canto da tela, então o 0, 0 do objeto é no canto de sua tela.
