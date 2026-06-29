# Generador de CV

Aplicación web de una sola página para crear currículums con apartados
personalizables, dos formatos (Diseño a 2 columnas y ATS a 1 columna),
exportación a PDF y autorrelleno por apartados.

- **No necesita servidor, build, ni base de datos.** Es estática: solo `index.html`.
- **No guarda ni envía datos.** Todo vive en el navegador de quien la usa y
  desaparece al cerrar la pestaña.
- **Quien la use no necesita iniciar sesión.**

## Archivos

| Archivo        | Para qué sirve                                              |
|----------------|------------------------------------------------------------|
| `index.html`   | La aplicación completa (HTML + CSS + JS en un solo archivo).|
| `vercel.json`  | Configuración mínima para Vercel (opcional).               |
| `.gitignore`   | Ignora archivos temporales en Git.                        |
| `README.md`    | Este documento.                                            |

---

## Opción A — Subir a GitHub

### A.1 Por la web (sin instalar nada)

1. Crea una cuenta en https://github.com y pulsa **New repository**.
2. Ponle un nombre (p. ej. `generador-cv`), déjalo **Public** y crea el repo.
3. En la página del repo vacío, pulsa **uploading an existing file**
   (o **Add file → Upload files**).
4. Arrastra `index.html`, `vercel.json`, `.gitignore` y `README.md`.
5. Pulsa **Commit changes**. Ya están subidos.

### A.2 Por terminal (si usas Git)

```bash
cd cv-app
git init
git add .
git commit -m "Generador de CV"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/generador-cv.git
git push -u origin main
```

### A.3 (Opcional) Publicar gratis con GitHub Pages

1. En el repo: **Settings → Pages**.
2. En **Source**, elige **Deploy from a branch**.
3. Branch: `main`, carpeta `/ (root)`. Pulsa **Save**.
4. En unos segundos aparece la URL pública, del tipo
   `https://TU_USUARIO.github.io/generador-cv/`.

---

## Opción B — Desplegar en Vercel

### B.1 Importando el repo de GitHub (recomendado)

1. Entra en https://vercel.com y regístrate **con tu cuenta de GitHub**.
2. Pulsa **Add New… → Project**.
3. Selecciona el repositorio `generador-cv` e **Import**.
4. Configuración:
   - **Framework Preset:** `Other`
   - **Root Directory:** `./`
   - **Build Command:** déjalo vacío
   - **Output Directory:** déjalo vacío (o `./`)
5. Pulsa **Deploy**. En ~30 segundos tendrás una URL pública del tipo
   `https://generador-cv.vercel.app`.

Cada vez que actualices el repo en GitHub, Vercel volverá a desplegar solo.

### B.2 Sin GitHub, con la CLI de Vercel

```bash
npm i -g vercel
cd cv-app
vercel        # sigue el asistente; al terminar te da la URL
vercel --prod # para publicarlo en la URL definitiva
```

### B.3 Sin GitHub ni terminal (lo más rápido)

Para un despliegue instantáneo arrastrando el archivo, usa
**Netlify Drop**: https://app.netlify.com/drop — arrastra `index.html`
(o toda la carpeta) y te da un enlace al momento.

---

## Probar en local

Solo tienes que abrir `index.html` con doble clic en tu navegador.
No requiere servidor. El botón de descarga a PDF funciona mejor abierto así
que dentro de un visor incrustado.
