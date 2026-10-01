# Programación Máquinas

Página web estática (un solo `index.html`) para ver y editar la programación mensual de turnos de Inspector de Máquinas. Los datos de octubre 2026 vienen incluidos en el propio HTML.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa |
| `icon-192.png` / `apple-touch-icon.png` | Íconos de la pestaña y de "Agregar a pantalla de inicio" |
| `.nojekyll` | Evita que GitHub Pages procese el sitio con Jekyll |
| `<mes>-<año>.json` | (opcional) Programación publicada de cada mes, por ejemplo `octubre-2026.json` |

## Publicar en GitHub Pages

1. Creá un repositorio nuevo en GitHub y subí todos los archivos de esta carpeta a la raíz.
2. Entrá en **Settings → Pages**.
3. En **Build and deployment**, elegí **Deploy from a branch**, la rama `main` y la carpeta `/ (root)`.
4. Guardá. En un minuto o dos la página queda en `https://<tu-usuario>.github.io/<nombre-del-repo>/`.

## Actualizar un mes

Desde la app, exportá el JSON del mes y subilo al repositorio con el nombre exacto `<mes>-<año>.json` (todo en minúsculas, sin tildes): `septiembre-2026.json`, `octubre-2026.json`, `noviembre-2026.json`, etc. Al abrir la página, la app lo toma automáticamente y reemplaza los datos incluidos en el HTML.

## Probar en tu computadora

Abrí una terminal en esta carpeta y ejecutá:

```
python3 -m http.server 8000
```

Después entrá a `http://localhost:8000`. Hace falta un servidor (y no abrir el archivo directamente) para que la app pueda leer los JSON de cada mes.
