---
layout: default
title: Escribir en Markdown
nav_order: 4
---

# Escribir en Markdown

Markdown es el formato principal para escribir contenido en tu sitio (Just the Docs). La idea es que puedas crear páginas claras y consistentes, sin depender de Word ni formatos complicados.

**Figura 14 (pendiente):** Ejemplo de una página con títulos, listas, callouts e imagen.
<!-- ![Figura 14 — Ejemplo de pagina](assets/img/fig14-ejemplo-markdown.png) -->

---

## 1) Regla de oro (para el curso)

- En cada página usa **un solo H1** (el título de la página).
- Dentro del contenido usa **H2 para secciones** y **H3 para subsecciones**.
- Mantén frases cortas y listas para pasos o requerimientos.

---

## 2) Encabezados (títulos)

```md
# Título de la página (H1)
## Sección (H2)
### Subsección (H3)
```

Recomendación: usa **H2** como secciones principales dentro de páginas; evita múltiples H1.

---

## 3) Negritas, cursivas y texto en línea

```md
**negrita**
*cursiva*
`codigo en linea`
```

Ejemplos:
- **Entrega final** el viernes.
- Usa `git status` para ver cambios.

---

## 4) Listas (viñetas, numeradas y tareas)

### Viñetas

```md
- Punto 1
- Punto 2
  - Subpunto 2.1
```

### Numeradas (pasos)

```md
1. Abre Codespaces
2. Edita el archivo
3. Haz commit
4. Haz push
```

### Checklists (útiles para entregas)

```md
- [ ] Agregué portada (index.md)
- [ ] Publiqué en GitHub Pages
- [ ] Verifiqué Actions en verde
```

---

## 5) Enlaces (a páginas, secciones, archivos y web)

### Enlace a otra página del sitio

```md
[Ir a Estructura del repositorio](02-estructura-del-repo.md)
```

### Enlace a una sección dentro de la misma página (ancla)

Primero, crea un encabezado:

```md
## Mi Seccion Importante
```

Luego enlaza así:

```md
[Ir a Mi Seccion Importante](#mi-seccion-importante)
```

> Nota: los espacios se convierten en guiones y todo queda en minúsculas.

### Enlace a un archivo (PDF, ZIP, etc.)

Guarda el archivo en `assets/files/` y enlaza así:

```md
[Descargar hoja de datos](assets/files/datasheet-sensor.pdf)
```

### Enlace externo

```md
[GitHub](https://github.com)
```

---

## 6) Imágenes (y buenas prácticas de rutas)

Guarda imágenes en `assets/img/`.

```md
![Diagrama del sistema](assets/img/diagrama-sistema.png)
```

Buenas prácticas:
- Usa nombres consistentes: `fig15-...`, `diagrama-...`, `captura-...`
- Evita espacios y acentos en nombres de archivo.
- Respeta mayúsculas/minúsculas (en web sí importa).

**Figura 15 (pendiente):** Ejemplo de referencia a imagen desde Markdown.
<!-- ![Figura 15 — Imagen en Markdown](assets/img/fig15-imagen-markdown.png) -->

---

## 7) Video (opciones recomendadas)

### Opción A: Enlace (simple y robusto)
Ideal para no romper el diseño.

```md
[Ver video de demostración (YouTube)](https://www.youtube.com/watch?v=ID_DEL_VIDEO)
```

### Opción B: Embed (si el curso lo requiere)
Puedes incrustar un video con HTML. Úsalo con moderación.

```html
<iframe
  width="560"
  height="315"
  src="https://www.youtube.com/embed/ID_DEL_VIDEO"
  title="Video"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen>
</iframe>
```

**Figura 16 (pendiente):** Video incrustado en una página.
<!-- ![Figura 16 — Video embed](assets/img/fig16-video-embed.png) -->

---

## 8) Código (bloques con resaltado y fragmentos)

### Bloque con resaltado

````md
```python
print("hola")
```
````

### Bloque sin lenguaje (texto plano)

````md
```text
git status
git add .
git commit -m "mensaje"
git push
```
````

### Código en línea

```md
Usa `git status` para ver cambios.
```

---

## 9) Tablas (cuando conviene y cómo alinearlas)

Ejemplo con alineación:

```md
| Campo | Tipo | Ejemplo |
|------:|:----:|:--------|
| RAM   | GB   | 8       |
| CPU   | x86  | i5      |
```

Buenas prácticas:
- No abuses de tablas anchas (en móvil se vuelven incómodas).
- Si la tabla se vuelve enorme, considera dividir en 2 o pasar a lista.

---

## 10) Citas y separadores

### Cita (blockquote)

```md
> Esto es una cita o nota rápida.
```

### Separador

```md
---
```

---

## 11) Callouts (notas, advertencias, importante)

Just the Docs soporta callouts con clases:

```md
{: .note }
Nota: esto es un recordatorio.

{: .warning }
Advertencia: cuidado con esto.

{: .important }
Importante: esto es crítico para que funcione.

{: .new }
Nuevo: esto se agregó recientemente.
```

{: .note }
Nota: si no aparecen con estilo, revisa que el tema sea Just the Docs y que el sitio se esté construyendo correctamente.

---

## 12) Bloques colapsables (útil para “solución” o “detalle”)

Puedes usar HTML nativo:

```html
<details>
  <summary>Ver solución</summary>

  Aquí va la explicación o solución paso a paso.
</details>
```

---

## 13) Plantilla rápida para una página del curso

Copia y adapta:

```yml
---
layout: default
title: Titulo de mi pagina
nav_order: 50
---
```

```md
## Objetivo
- ...

## Materiales
- ...

## Pasos
1. ...
2. ...

## Evidencia
- Foto / captura / enlace
```

---

## Siguiente sección

[Navegación y menú (Just the Docs)](04-navegacion.md)
