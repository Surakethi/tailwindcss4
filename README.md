# tailwindcss4
Plain Tailwind CSS version 4 + Vite

### Step instalasi 
1. download repo dari github
```
git clone https://github.com/Surakethi/tailwindcss4.git
cd tailwindcss4
```

2. inisiali node project, es6 untuk membuatnya type module
```
npm init es6 -y 
```

3. instalasi vite 
```
npm install vite@latest
```

4. masukkan script untuk running vite, di package.json
```
    "dev": "vite",
    "build": "tsc -b && vite build",
    "lint": "eslint .",
    "preview": "vite preview"
```

5. instalasi tailwindcss
```
    npm install tailwindcss @tailwindcss/vite
```

6. bikin file vite.config.ts
```
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'
export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})
```

7. bikin file style.css yang akan menggunakan tailwindcss
```
@import "tailwindcss";
```

8. bikin file index.html yang menggunakan style.css
```
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="/src/style.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

9. running vite server untuk development
```
    npm run dev
```
