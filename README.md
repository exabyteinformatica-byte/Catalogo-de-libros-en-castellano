# Catálogo de libros en español (www.tuslibrosvip.com) / Spanish Books Catalog

Spanish-language book catalog: more than 94,000 titles (paperback, Kindle and
audiobook) with author, format, category and publication year. Updated daily
on the website.

CSV con más de 94.000 libros en papel, Kindle y audiolibro. Se regenera a diario
en la web.

**Fuente viva y última versión / Live source and latest version:**
https://www.tuslibrosvip.com/catalogo-libros-csv

**Otras copias / Other mirrors:**
- Hugging Face: https://huggingface.co/datasets/tuslibrosvipcom/catalogo-libros-espanol
- Kaggle: https://www.kaggle.com/datasets/tuslibrosvipcom/catlogo-de-libros-en-espaol-tuslibrosvip-com

## Archivos / Files

- `Todos-los-libros-de-tuslibrosvip-com.zip`: fichero ZIP estándar que contiene:

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
| `anio_publicacion` | Año de publicación (puede estar vacío) |
| `url` | Enlace a la ficha del libro en tuslibrosvip.com |

## Uso rápido / Quick start

Con pandas, leyendo directamente desde GitHub (pandas abre el ZIP solo, no hace
falta descomprimirlo antes):

```python
import pandas as pd

URL = "https://raw.githubusercontent.com/exabyteinformatica-byte/Catalogo-de-libros-en-castellano/main/Todos-los-libros-de-tuslibrosvip-com.zip"

df = pd.read_csv(URL, compression="zip", dtype={"anio_publicacion": "Int64"})
print(df.shape)
print(df["categoria"].value_counts().head(10))
```

Con la librería `datasets` de Hugging Face:

```python
from datasets import load_dataset

ds = load_dataset("tuslibrosvipcom/catalogo-libros-espanol", split="train")
print(ds)
print(ds[0])
```

Para abrirlo en Excel: descomprime el ZIP y, en Excel, usa
*Datos → Desde texto/CSV* eligiendo la codificación UTF-8 (si lo abres con
doble clic, los acentos pueden verse mal).

## Para qué sirve

- Estudiar el mercado editorial en español: géneros, autores o formatos más habituales.
- Montar un recomendador, un buscador o un chatbot de libros.
- Cruzar datos con una biblioteca personal, lista de lecturas o inventario.
- Proyectos de análisis de datos, docencia y trabajos académicos.

## Licencia / License

[Creative Commons Atribución 4.0 (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
Puedes usarlo, copiarlo y modificarlo, incluso con fines comerciales, citando la fuente.

Cita como: "Fuente: tuslibrosvip.com, Catálogo de libros en CSV",
con enlace a https://www.tuslibrosvip.com/catalogo-libros-csv

## Limitaciones / Limitations

- La categoría se asigna de forma automática con IA y puede tener errores puntuales.
- El ISBN está vacío en audiolibros y en muchos libros digitales.
- `anio_publicacion` puede estar vacío. Al leerlo con pandas se recomienda `dtype="Int64"`.
- No incluye precios, imágenes ni descripciones.
- Que un libro aparezca en el catálogo no garantiza que esté disponible en este momento.
- Esta copia es una instantánea: la versión actualizada está siempre en la web.

## Contacto

Para comunicar un error, escribe a contacto@tuslibrosvip.com indicando el ASIN del libro.
