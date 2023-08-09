# Projeto LogOperation - Estudos

---

> Projeto para fins de estudo

## Instruções para build

---

1° Passo - instalar o Tailwind no projeto, conforme abaixo:

Para baixar o pacote Tailwind:

```bash
npm install -D tailwindcss
npx tailwindcss init
```

Crie o aquivo `input.css` em `./src` conforme abaixo

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Para configurar o tailwindCSS referenciar os arquivos `html/js` no arquivo `tailwind.config.js` como no exemplo abaixo:

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

Após rodar o comando faça o build do projeto:

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

Por fim, referencia o arquivo `./output.css` no head do arquivo `index.html`

```html
<link href="/dist/output.css" rel="stylesheet" />
```

---

Caso ja possua as dependecias(\*.json) só rodar o comando:

```bash
npm install
```

E, rodar o comando abaixo para build do tailwind

```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```
