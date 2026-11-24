# Sitio personal de Santiago Martínez

Sitio estático con Astro para publicar los trabajos de Ingeniería de Requerimientos y ampliar posteriormente el portfolio personal.

## Desarrollo

Requiere Node.js 22 y pnpm 10.

```sh
pnpm install
pnpm dev
```

## Agregar un trabajo

1. Copiar el documento Word a `public/documentos/`, con un nombre sin espacios ni tildes.
2. Agregar una entrada a `src/data/trabajos.ts` con clase, tipo, título, descripción y nombre del archivo.
3. Ejecutar `pnpm build` y revisar localmente con `pnpm preview`.
4. Hacer commit y push a `main`. GitHub Actions construye y publica el sitio.

Los documentos se ofrecen exclusivamente como descargas. Los tres Word originales se conservan sin cambios. Las capturas fueron transcritas a documentos por clase, preservando las respuestas visibles sin resolver consignas adicionales.

## Publicación

Repositorio previsto: `SJMartinez/sjmartinez.github.io`. En Settings → Pages, seleccionar GitHub Actions. El workflow está en `.github/workflows/deploy.yml` y publica `dist/`.

El sitio no requiere backend, base de datos ni servicios pagos. El contenido es navegable y los archivos se descargan aunque JavaScript esté desactivado; JavaScript se usa solamente para filtrar el listado.
