# CAMPUSFIX · Front alfa

Plataforma de reportes de mantenimiento del campus (Universidad del Valle Claro, entorno de demostración).
Esta versión alfa es solo **frontend** (HTML + CSS + JS, sin dependencias). El backend se agregará en la siguiente etapa.

## Funciones
- Registro de usuario con rol: **Comunidad**, **Mantenimiento** o **Coordinación**; inicio y cierre de sesión.
- Cada cuenta inicia vacía: sin reportes, historial ni conteos.
- Comunidad: crea reportes (ubicación en cascada, categoría, descripción, hasta 3 imágenes JPG/PNG de 5 MB) y consulta su seguimiento.
- Coordinación: ve todos los reportes y asigna responsable (personal de Mantenimiento registrado).
- Mantenimiento: ve sus reportes asignados y registra la solución.
- Panel con conteos, búsqueda y filtros, detalle con historial, ubicaciones y diseño adaptable a celular.

## Estructura
```
index.html      Punto de entrada
css/styles.css  Estilos (modo claro/oscuro, responsive)
js/app.js       Lógica, vistas y rutas (hash)
```

## Ejecutar
Abre `index.html` en el navegador, o sirve la carpeta: `python3 -m http.server 8000`.

## Publicar en GitHub Pages
1. Sube esta carpeta a un repositorio.
2. Settings → Pages → Deploy from a branch → `main` / `/ (root)`.

## Limitaciones de la alfa
- Los datos se guardan en `localStorage` del navegador (no se comparten entre personas ni dispositivos).
- Las evidencias solo guardan el nombre del archivo.
- La autenticación es simulada; las contraseñas se almacenan como hash SHA-256 solo en el navegador.

## Siguiente etapa: backend
API REST con base de datos, autenticación por rol y almacenamiento de imágenes.
