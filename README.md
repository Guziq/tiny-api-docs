# tiny-api-docs

The **tiny-api-docs** can be used as a lightweight alternative to [Swagger](https://swagger.io/) or [Slate](https://github.com/lord/slate).

It’s tiny because it needs just three files to work: the place when you write the content (`content.md`), the file with stylings (`github-markdown.css`), and the file that renders your docs (`index.html`).

## Get Started

1. Copy everything to a static directory on your server (e.g. `api/docs`) , so it could serve the `index.html` file.
2. Edit the `content.md` for your own purpose.
3. Have fun!

## Features:

* Markdown support (thanks to [marked](https://github.com/chjj/marked)).
* Clean styling (thanks to [github-markdown-css](https://github.com/sindresorhus/github-markdown-css)).
* Table of Contents (thanks to [tocbot](https://github.com/tscanlin/tocbot)).
* Clean column layout (thanks to [Bootstrap](http://getbootstrap.com)).
* Single file edition.

