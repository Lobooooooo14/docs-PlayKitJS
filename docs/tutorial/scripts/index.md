# Estrutura

Para desenvolver seu jogo com os scripts na PlayKitJS, é nessesário conhecimentos básicos em programação. 

Os scripts são compostos por duas funcões principais:

- Start: Tudo que deve ocorrer quando o jogo for iniciado.
- Update: O que deve ser atualizado de acordo com o FPS.

Com isso em mente, esta é a estrutura principal:

```{.js linenums="1" title="scripts"}
function Start() {
    //On Start
}

function Update() {
    //On Update
}
```

Sendo assim, no `Start()` é definido o tamanho da tela, e no `Update()` a movimentação, por exemplo. Isso será abordado mais a fundo na próxima sessão.
