# Web Storage API

📽 Veja esta vídeo-aula no Youtube: _Em breve..._

Programas em Javascript podem precisar acessar informações que são usadas comumente por um usuário, através de uma página na Web e um navegador.

Estas informações então, são salvas __localmente__, para personalizar a experiência do usuário na interação com o site.

Um navegador em 2020 suporta duas formas de se persistir informações localmente, pelo nagevador:

* [Cookies](https://developer.mozilla.org/en-US/docs/Glossary/Cookie)
* Web Storage API.

Neste curso utilizaremos a _Web Storage API_, que possui mecanismos mais intuitivos que os _Cookies_ 🍪

## Conceitos

Os mecanismos utilizados pela _Web Storage API_ para armazenar informações de um navegador *localmente* são baseados em chave / valor, ou seja, para cada chave única de um conjunto de dados, a API proverá um determinado valor.

* nome / Programação Web
* nomeNeri / Diego Neri de Souza Felix

Há dois objetos de Storage na _Web Storage API_, que podem ser manipulados:

* `sessionStorage` --> área de armazenamento utilizada por uma página Web em sua sessão, ou seja, as informações persistidas são válidas enquanto o navegador estiver aberto, *incluindo* a página em questão, inclusive durante atualizações da página.<br/>🍌 Abrir a página em uma nova aba ou nova janela do navegador cria uma nova sessão.<br/>🍌 O backend pode definir um tempo de duração da sessão, que também pode afetar estes dados.

* `localStorage` --> área de armazenamento permanente do navegador, ou seja, elas não expiram e as informações estarão acessíveis para o site mesmo que ele seja fechado e reaberto em outro momento.

🍌 Cada **domínio** possui a sua referência ao `localStorage` ou ao `sessionStorage`, ou seja, não é possível reaproveitar valores entre domínios.

Ambos os mecanismos são acessíveis via `Window`, `Window.sessionStorage` e `Window.localStorage`, ou simplesmente por `sessionStorage` e `localStorage`.

Em 2020, todos os navegadores de mercado suportam a _Web Storage API_.

## Session storage

```js
// Salva os dados com setItem
sessionStorage.setItem('chave', 'valor');

//Salva os dados com chave
sessionStorage.chave = 'valor'

//Salva os dados com arranjo
sessionStorage['chave'] = 'valor'
```

```js
// Obtém os dados com getItem
let valorGetItem = sessionStorage.getItem('chave');

// Obtém os dados com chave
let valorChave = sessionStorage.chave;

// Obtém os dados com arranjo
let valorArranjo = sessionStorage['chave'];
```

## Local storage

```js
// Salva os dados com setItem
localStorage.setItem('chave', 'valor');

//Salva os dados com chave
localStorage.chave = 'valor'

//Salva os dados com arranjo
localStorage['chave'] = 'valor'
```

```js
// Obtém os dados com getItem
let valorGetItem = localStorage.getItem('chave');

// Obtém os dados com chave
let valorChave = localStorage.chave;

// Obtém os dados com arranjo
let valorArranjo = localStorage['chave'];
```
_Em breve..._