# Análisis de SERPs

Este script de Python permite analizar las páginas de resultados de búsqueda (SERPs) para una palabra clave específica. Utiliza las librerías `requests`, `BeautifulSoup` de `bs4`, `Counter` de `collections` y `openpyxl` para obtener y procesar datos de sitios web, y almacenar los resultados en un archivo Excel.

## Funcionalidades

- **Obtener SERPs**: Extrae los primeros cinco resultados de búsqueda de Google para una palabra clave ingresada.
- **Análisis de contenido**: Descarga y analiza el contenido de las páginas obtenidas para contar palabras, pares de palabras, y extraer todos los encabezados y atributos `alt` de imágenes.
- **Generación de reportes en Excel**: Crea un archivo Excel con múltiples hojas para organizar la información recopilada como conteo de palabras, encabezados y atributos de imágenes, además de una comparativa entre todas las páginas analizadas.

## Uso

1. Instale las dependencias con `pip install requests beautifulsoup4 openpyxl`.
2. Ejecute el script. Se le pedirá que ingrese una palabra clave.
3. El script generará un archivo Excel titulado `{palabra_clave} - análisis.xlsx` con los resultados del análisis.

## Estructura del Proyecto

El script se divide en varias funciones:
- `obtener_serps(palabra_clave)`: Obtiene las URL de las SERPs.
- `obtener_contenido(url)`: Extrae el contenido textual de la URL especificada.
- `contar_palabras(texto)`, `contar_pares_palabras(texto)`: Funciones para contar palabras y pares de palabras en el texto.
- `contar_imagenes(url)`, `extraer_encabezados(url)`, `extraer_atributo_alt(url)`: Funciones para analizar elementos específicos de las páginas web.
- Se incluyen instrucciones detalladas para agregar datos al archivo Excel y organizar las hojas de cálculo.

Este script es útil para SEO y análisis de contenido web. Asegúrese de tener permisos adecuados para scrapear los sitios web que analiza.
