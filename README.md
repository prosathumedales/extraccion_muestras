# Extracción de datos estadísticos de datos satelitales

El repositorio incluye scripts para la extracción de datos satelitales SAR y ópticos, a partir de muestras vectoriales (archivos shapefiles) representativos de distintas clases de información.

## Datos de microondas activas SAR

El script se elaboró en lenguaje Python y actualmente se encuentra disponible en [este repositorio]([https://github.com/prosathumedales/extraccion_muestras/blob/main/SAR_dataframe](https://github.com/prosathumedales/extraccion_muestras/blob/main/2_creaci%C3%B3n_de_DataFrames_emprolijando(1).ipynb)) y en [Google Colab](https://colab.research.google.com/drive/1vzbcz5d23IM8H3CrfQIX7BBFmBdEQP0S).

**Autora:** Mariela Rajngewerc - [@marielaraj](https://github.com/marielaraj)

### Inputs
1. Archivo vectorial con **polígonos de muestra** de cada clase de humedal, en formato _shapefile_.
2. **Escenas SAR** en formato Geotiff.
Las escenas SAR fueron bajadas y pre-procesadas por integrantes del proyecto (ver repositorio con scripts para procesamiento) y se encuentran almacenadas en disco. En esta primera versión, el script trabaja desde Google Colab y toma una muestra pequeña de escenas SAR de un Google Drive. Las escenas son de los sistemas satelitales:
- SAOCOM 1A y 1B (CONAE). Además de las escenas en formato .tif, se requiere del encabezado en formato .xemt.
- Sentinel 1A y 1B (ESA)
- ALOS/PALSAR-1 (JAXA). Adems de las escenas en formato .tif, se requiere de un listado con las fechas de adquisición, disponible al descargar las escenas en ASF. 

### Ouput
El output es un dataframe en formato csv, con la media y desvío para cada banda de cada escena. Los campos del dataframe incluyen información de la escenae información del polígono del shapefile. 

## Datos ópticos

Se elaboró un script en Python utilizando la API de Google Earth Engine (GEE).  Desde GEE, se leen y extraen muestras de escenas Sentinel-2 (ESA) y Landsat 5-TM y 8-OLI (NASA).
El script se subirá a este repositorio.

**Autor:** Esteban Roitberg - [@loibel](https://github.com/Loibel)

### Inputs
1. Archivo vectorial con **polígonos de muestra** de cada clase de humedal, en formato _shapefile_.
2. **Escenas ópticas** del catálogo de GEE.

### Ouput
El output es un dataframe en formato csv, con la media y desvío para cada banda de cada escena. Los campos del dataframe incluyen información de la escenae información del polígono del shapefile. 


## Licencia
[CC BY SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es)

El proyecto está en desarrollo, consultar cómo citar. Contacto: Natalia Morandeira (nmorandeira@unsam.edu.ar, [@nmorandeira](https://github.com/nmorandeira))
