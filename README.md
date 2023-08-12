# React + Vite

## Deploy React En GitHub Pages
```BASH
npm install gh-pages --save-dev
```

## Configurar Git con Github al Proyecto
```BASH
git init
git add .
git commit -m "React Vite JS"
git branch -M "main"
git remote add origin "https://github.com/HenryCCoillo/vite_reploy.git"
git push -u origin "main"
```

## Configuramos package.json
```JSON
{
  "homepage":"https://henryccoillo.github.io/vite_reploy",
  "name": "deploy",
  ...
  "scripts": {
    "predeploy":"npm run build",
    "deploy":"gh-pages -d dist",
...
  },
...
}

```
## Configuramos vite.config.json
```JSON
export default defineConfig({
  plugins: [react()],
  base:'/vite_reploy/'
})
```

## Comando de deploy
```BASH
npm run deploy
```
