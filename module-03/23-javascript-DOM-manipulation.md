# JavaScript DOM manipulation
Você pode pensar no DOM como um controle remoto de TV que permite alterar o conteúdo da página da Web na tela. Ele ainda permite que você substitua apenas certas partes da página, como uma imagem ou o título ou ambos. Um controle remoto, no entanto, tem certas limitações. Você só pode alterar o canal, contraste, brilho e volume. O DOM oferece um controle muito mais refinado do que um controle remoto de TV jamais poderia. Por exemplo, imagine que você pode alterar a aparência dos personagens de um filme de TV com alguns comandos simples enquanto o filme está sendo reproduzido.

O **DOM** permite alterar as propriedades dos objetos em uma página da web. Você pode pensar no **DOM** como um controle remoto superpoderoso para sites. Dá aos desenvolvedores poder em como eles podem manipular e atualizar páginas da web. O **DOM** está na forma de um objeto JavaScript com objetos aninhados para diferentes partes da página. Esses objetos têm seus próprios objetos aninhados até que todo o arquivo **HTML** seja mapeado no que parece ser uma **estrutura de árvore**. O **DOM** é o modelo do arquivo **HTML** salvo como objeto JavaScript na **memória do seu navegador**. O navegador cria automaticamente o **DOM** para cada página da Web baixada. Por exemplo, se você digitar um **URL** na barra de endereços do seu navegador, o navegador buscará a página da web que existe neste domínio. Se o navegador se conectar ao servidor e permitir que o navegador baixe a página, ele receberá todo o código **HTML** e o **salvará em sua memória**. O navegador irá então mostrar a página baixada. Também construiria o **DOM** dessa página da Web um modelo do documento **HTML** que seu navegador acabou de baixar.

Como desenvolvedor, você pode interagir com o **DOM** da página para fazer alterações na página da web. Para interagir com o **DOM**, você pode usar a guia **Elements** dentro do **DevTools** do navegador. Você acessa o **DevTools** clicando com o botão direito do mouse em qualquer lugar na janela do navegador e clicando em "**Inspecionar**".
![devtools](https://i.ibb.co/zJSh6fc/Screen-Shot-2022-10-23-at-11-27-07.png)

A guia **Elements** permite que você interaja com o **DOM** da página da Web atualmente ativa usando uma interface gráfica do usuário, também conhecida como **GUI**. O navegador também permite que você interaja com o **DOM** usando JavaScript. Para fazer isso, você deve clicar na guia **Console** no **DevTools** do navegador. Você pode focar no painel **Console** pressionando a tecla **Escape** no teclado. Uma vez feito, você pode começar a digitar comandos JavaScript para visualizar e manipular o **DOM**. Isso é semelhante a como você interage com o **DOM** usando o painel **Elements**, só que desta vez você está usando código para fazer isso. Todo o objeto **DOM** é salvo dentro da variável do documento e acessível através do console. Agora deixe-me demonstrar como funciona a **manipulação do DOM**.

O uso do modelo de objeto de documento nos permite manipular sites ativos. Por exemplo, abri meu navegador e carreguei a página do google.com na Internet. Desejo adicionar um elemento HTML de título 2 (`h2`) a esta página da Web usando o **DOM**. Mais uma vez, tenho as Ferramentas do desenvolvedor abertas na janela à direita na guia **Console** está ativa. É importante lembrar que quaisquer alterações que eu fizer no **DOM** são relativas à cópia local da página do meu navegador, não estou atualizando o conteúdo do site ao vivo, então não se preocupe, você não vai quebrá-lo. Se eu recarregar a página da Web, todas as alterações feitas no DOM serão perdidas.
![exemplo no devtools](https://i.ibb.co/KDFQ8mk/Screen-Shot-2022-10-23-at-11-35-24.png)

Este é o trecho de código que vamos por no **Console** do **DevTools**, vou explicar ele em seguida. 
```js
  const Title2 = document.createElement('h2');

  Title2.innerText = "This is an h2 heading";

  Title2.setAttribute('id', 'sub-heading');

  Title2.setAttribute('class', 'secondary');

  document.body.appendChild(Title2);
```

Para criar meu cabeçalho `h2` vou atribuir esta declaração a uma variável `const`, eu digito `const Title2` e em seguida preciso atualizar o objeto do `document`, para fazer isso vou usar o método `createElement`, entāo eu digito `document.createElement('h2');`, nota que no fim eu abri e fechei parêntese e dentro coloquei o `h2` com aspas simples.
```js
  const Title2 = document.createElement('h2');
```

Meu elemento `h2` também precisa de algum texto, sem ele, mesmo após adiionar o elemento `h2` ao `document`, não haveria uma mudança visível na página porque o elemento `h2` adicionado, embora não teria texto dentro em outras palavras, ficaria em branco. Eu posso executar isso na minha variável `Title2`. Eu digito `Title2.innerText` e, em seguida, atribuo uma string com um valor para o texto.
```js
  Title2.innerText = "This is an h2 heading";
```

Em seguida, quero que meu elemento de `h2` tenha um `id` e uma `class` como atributo **HTML**. Para fazer isso, preciso usar o método `setAttribute`. Eu digito `Title2.setAttribute`, que recebe dois parâmetros, o nome do atributo dentro de aspas simples e depois o valor do atributo eles devem ser separados por virgula.
```js
  Title2.setAttribute('id', 'sub-heading');

  Title2.setAttribute('class', 'secondary');
```

Agora eu preciso executar o método `appendChild` no corpo do documento (`body`) para fazer isso. Agora, eu digito `document.body.appendChild` e dentro dos parênteses, coloco minha estrutura **HTML** armazenada na variável `Title2`. 
```js
  document.body.appendChild(Title2);
```

Sucesso, meu objeto é anexado ao corpo desta página da Web e o texto do título 2 é exibido no navegador.

Agora você deve ser capaz de explicar os fundamentos da manipulação do DOM e usar alguns dos métodos de manipulação do DOM mais comuns.