## Tailwind css
> Basic setup of tailwind css using Tailwind CLI
> Goto official website: [Install Tailwind CSS using PostCSS - Tailwind CSS](https://tailwindcss.com/docs/installation)

#### Install Tailwind CSS

``` bash
npm install -D tailwindcss
npx tailwindcss init
```
 
#### Configure your template paths
Add the paths to all of your template files in your tailwind.config.js file.

```json
/** @type {import('tailwindcss').Config} */

module.exports = {

content: ["./src/**/*.{html,js}"],

theme: {

extend: {},

},

plugins: [],

}

```

#### Add the Tailwind directives to your CSS
Add the  `@tailwind`  directives for each of Tailwind’s layers to your main CSS file.

```css
/* src/input.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

#### Add src/index.html

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

#### Add in packages.json
```json
"scripts": {
	"watch": "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
}
```

#### now run
```bash
npm run watch
```