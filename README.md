# Catálogo de libros en español (tuslibrosvip.com) / Spanish Books Catalog

Spanish-language book catalog: more than 94,000 titles (paperback, Kindle and
audiobook) with author, format, category and publication year. Updated daily
on the website; this copy is an archived snapshot.

CSV con más de 94.000 libros en papel, Kindle y audiolibro. Se regenera a diario
en la web; esta copia es una versión archivada.

**Fuente viva y última versión / Live source and latest version:**
https://www.tuslibrosvip.com/catalogo-libros-csv

## Archivos / Files

- `Todos-los-libros-de-tuslibrosvip-com.csv.gz`: la misma información comprimida.

## Campos / Fields

| Campo | Descripción |
|---|---|
| `asin` | Identificador del libro en Amazon |
| `isbn` | ISBN, cuando está disponible |
| `titulo` | Título del libro |
| `autor` | Autor o autores |
| `formato` | Formato concreto (por ejemplo, "Tapa blanda", "Audible Audiolibro") |
| `tipo` | Libro (papel), Compra de libro digital (Kindle) o Audible |
| `categoria` | Género o categoría literaria |
| `anio_publicacion` | Año de publicación |
| `url` | Enlace a la ficha del libro en tuslibrosvip.com |

## Uso rápido / Quick start

```python
import pandas as pd

df = pd.read_csv("Todos-los-libros-de-tuslibrosvip-com.csv")
print(df.shape)
print(df["categoria"].value_counts().head(10))
```

## Para qué sirve

- Estudiar el mercado editorial en español: géneros, autores o formatos más habituales.
- Montar un recomendador, un buscador o un chatbot de libros.
- Cruzar datos con una biblioteca personal, lista de lecturas o inventario.
- Proyectos de análisis de datos, docencia y trabajos académicos.

## Licencia / License

[Creative Commons Atribución 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
Puedes usarlo, copiarlo y modificarlo, incluso con fines comerciales, citando la fuente.

Cita como: "Fuente: tuslibrosvip.com, Catálogo de libros en CSV ([fecha])",
con enlace a https://www.tuslibrosvip.com/catalogo-libros-csv

## Limitaciones / Limitations

- La categoría se asigna de forma automática con IA y puede tener errores puntuales.
- El ISBN está vacío en audiolibros y en muchos libros digitales.
- No incluye precios, imágenes ni descripciones.
- Que un libro aparezca en el catálogo no garantiza que esté disponible en este momento.
- Esta copia es una instantánea: la versión actualizada está siempre en la web.

## Contacto

Para comunicar un error, escribe a contacto@tuslibrosvip.com indicando el ASIN del libro.
