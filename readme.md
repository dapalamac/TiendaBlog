TiendaBlog

Tienda en línea estática construida con **Jekyll** y desplegada en **GitHub Pages**.

**Demo en vivo:** [https://dapalamac.github.io/TiendaBlog/](https://dapalamac.github.io/TiendaBlog/)

---

## Estructura del proyecto

```
TiendaBlog/
├── _layouts/
│   ├── default.html       # Layout base de todas las páginas
│   └── post.html          # Layout de página de producto
├── _posts/
│   ├── 2025-05-18-cancelaciónRuido.md
│   ├── 2025-05-18-inalámbricoBluetooth.md
│   └── 2025-05-18-paraGamers.md
├── assets/
│   └── style.css          # Estilos globales
├── img/
│   ├── portada.jpg
│   ├── audifono-bluetooth.jpg
│   ├── audifono-cancelacion.jpg
│   └── audifono-gamer.jpg
├── _config.yml            # Configuración de Jekyll
├── index.md               # Página principal
└── README.md
```

---

## ⚙️ Configuración

El archivo `_config.yml` contiene la configuración principal del sitio:

```yaml
title: Mi Tienda
email: contacto@mitienda.com
description: Una tienda sencilla hecha con Jekyll
baseurl: "/TiendaBlog"
url: "https://dapalamac.github.io"
theme: null
```

> **Importante:** El `baseurl` debe coincidir exactamente con el nombre del repositorio en GitHub para que las rutas de imágenes y CSS funcionen correctamente.

---

##  Agregar un nuevo producto

1. Crea un archivo en `_posts/` con el formato:
   ```
   YYYY-MM-DD-nombreProducto.md
   ```

2. Agrega el siguiente **front matter** al inicio del archivo:
   ```yaml
   ---
   layout: post
   title: Nombre del Producto
   image: /img/nombre-imagen.jpg
   price: 25.0
   ---
   ```

3. Debajo del front matter escribe la descripción del producto en Markdown.

4. Agrega la imagen del producto a la carpeta `img/`.

---

## 🚀 Despliegue

El sitio se despliega automáticamente en **GitHub Pages** con cada push a la rama `main`.

Puedes verificar el estado del despliegue en la pestaña **Actions** del repositorio.

---

## Errores comunes y soluciones

| Problema | Causa | Solución |
|---|---|---|
| Imágenes no cargan | `baseurl` vacío o incorrecto | Verificar `_config.yml` y usar `{{ site.baseurl }}` en todas las rutas |
| CSS no aplica | Carpeta de layouts mal nombrada | Asegurarse de que se llame `_layouts` (con guión bajo) |
| Dos páginas de inicio | Archivos `index.md` e `index.markdown` coexistiendo | Eliminar `index.markdown` |
| Layout no se aplica | Carpeta `layout` sin guión bajo | Renombrar a `_layouts` |
| CSS no se encuentra | Archivo CSS en carpeta no reconocida por Jekyll | Mover CSS a carpeta `assets/` |

---

## Tecnologías usadas

- [Jekyll](https://jekyllrb.com/) — Generador de sitios estáticos
- [GitHub Pages](https://pages.github.com/) — Hosting gratuito
- HTML5, CSS3 — Diseño y maquetación
- Liquid — Motor de plantillas de Jekyll

---

##  Autor

**David Palacio Macias**  
GitHub: [@dapalamac](https://github.com/dapalamac)
