# Javascript

Para desenvolver seu jogo com os scripts na PlayKitJS, é nessesário conhecimentos básicos em Javascript. Esta sessão aborda alguns tópicos com as funcionalidades do Javascript na PlayKitJS.

# Objetos

Na PlayKitJS, existem alguns tipos de objetos dos quais podem ser utilizados para desenvolver seus jogos, entre eles:

- Object: Objeto padrão, usado para criar um player, inimigos, chão, moedas, etc.
- Ball: Similar ao `Object`, porém com uma colisão circular.
- Gui: Elemento da interface.
- Backdrop: Objeto usado para criar cenários e fundos.

## Object

O object é o objeto padrão que contém colisão com outros objetos e com seus devidos parâmetros:

- sprite: A sprite padão do objeto.
- X: A posição X do objeto na tela.
- Y: A posição Y do objeto na tela.
- largura: A largura do objeto.
- altura: A altura do objeto.
- é_estático: Se o objeto deve permanecer parado.

```{.js linenums="1" title="Exemplo de criação de um object"}
var nome_do_objeto = new object("sprite", x, y, largura, altura, é_estático);
```

```{.js linenums="1" title="Exemplo com valores"}
var nome_do_objeto = new object("sprite.png", 0, 0, 100, 100, false);
```