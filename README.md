# APP

## Esta pagina web usa la API de TheMealDB

## Run App
```
marin@PC-SALON-JUAN MINGW64 ~/Desktop/app-food (main)
$ npm run dev

```

## Crear repositorio en github.com

>food


## Añadir al archivo vite.config.js 


>base: "/food/"


### vite.config.js

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vitejs.dev/config/
export default defineConfig({
  plugins: [react()],
  base: "/food/"
})


```
### package.json

```json
{
  "name": "app",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview",
    "deploy": "gh-pages -d dist"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-router-dom": "^6.14.2"
  },
  "devDependencies": {
    "@types/react": "^18.0.27",
    "@types/react-dom": "^18.0.10",
    "@vitejs/plugin-react": "^3.1.0",
    "gh-pages": "^5.0.0",
    "vite": "^4.1.0"
  }
}


```

## Crear carpeta dist para produccion

```
marin@PC-SALON-JUAN MINGW64 ~/Desktop/app-food (main)
$ npm run build

```

## Deploy App

```
marin@PC-SALON-JUAN MINGW64 ~/Desktop/app-food (main)
$ npm run deploy

```


---

# Para publicar una web creada con Vite en GitHub Pages, estos son los pasos detallados que debes seguir:

CREA UN REPOSITORIO EN GIT HUB

✅ 1. Configura tu proyecto Vite
Asegúrate de tener tu proyecto listo. Si ya lo tienes creado, sigue estos pasos.

✅ 2. Configura la variable base en vite.config.js
En vite.config.js, debes indicar la ruta base, que generalmente es https://tu-usuario.github.io/nombre-del-repo/.

Ejemplo:

__________________________________________________________________________________________

```js
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';

export default defineConfig({
  plugins: [react()],
  base: '/nombre-del-repo/',  // Coloca aquí el nombre EXACTO de tu repo
});

```
_____________________________________________________________________________________________

⚠️ Importante: Si el repo se llama, por ejemplo, mi-portafolio, la base debe ser:

 
base: '/mi-portafolio/',

__________________________________________________________________________
✅ 3. Instala gh-pages
En la terminal, dentro del proyecto:

 ```
npm install --save-dev gh-pages
 ```
_______________________________________________________________________
✅ 4. Agrega scripts al package.json
En tu package.json, añade los siguientes scripts:

 ```
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "preview": "vite preview",
  "deploy": "gh-pages -d dist"
}
 ```
__________________________________________________________________________
✅ 5. Publica en GitHub Pages
A. Haz un build del proyecto:
 ```
npm run build
 ```
____________________________________________________________________

B. Sube el contenido de dist a GitHub Pages usando:
 ```
npm run deploy
 ```
_________________________________________________________________________________
Esto usará la rama gh-pages para alojar tu sitio.

✅ 6. Activa GitHub Pages en el repositorio
Ve a tu repositorio en GitHub.

Entra en Settings → Pages.

En Branch, selecciona gh-pages y la carpeta / (root) o /dist si se requiere.

Guarda los cambios.
______________________________________________________________________________________________
✅ 7. Abre tu sitio
Generalmente estará disponible en:

 
https://tu-usuario.github.io/nombre-del-repo/
 
 