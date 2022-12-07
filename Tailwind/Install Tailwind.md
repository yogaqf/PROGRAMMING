


Git Bash Here
```bash
npm install -D tailwindcss
npx tailwindcss init
```

tailwind.config.js
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

input.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

run di terminal
```bash
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch
```

index.html
```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/dist/output.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

