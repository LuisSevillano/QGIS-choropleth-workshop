#Como realizar un sencillo mapa de cloropletas en QGIS

En este sencillo tutorial aprenderemos a realizar un sencillo mapa de cloropletas con QGIS. Todos los pasos necesarios están descritos aquí abajo. Vamos a crear un mapa de densidad de población por municipios (renta).   
Necesitaremos descargar dos conjuntos de datos, los `shapefiles` y el `csv`. Después cruzaremos los datos mediante el id único de cada municipio. Empecemos:   
1. Descargamos los shapefiles originales del enlace oficial:   
	**Centro de descargas del Instituto Geográfico Nacional** (CNIG) [Link ](http://centrodedescargas.cnig.es/CentroDescargas/equipamiento/lineas_limite.zip)   
	En este enlace descargaremos los archivos oficiales en formato _shapefie_ (.shp). Este archivo incluye más shapefiles de los que vamos a necesitar. Si hubiera algún problema con la desgarga también se encuentra en la carpeta `shapefiles`del repositorio.    


2. Descomprimimos los archivos. Vamos a trabajar con dos archivos incluidos en dos carpetas diferentes:

	- `recintos_municipales_inspire_canarias_wgs84`   
	- `recintos_municipales_inspire_peninbal_etrs89`   

	El resto de carpetas contienen las entidades Comunidades Autónomas y Provincias (recintos) además de las contornos (líneas).

3. Abrimos los dos archivos en QGIS. Es importante seleccionar la **codificación** `UTF-8` para no perder información. Si observamos, el mapa ha adoptado una apariencia _achatada_ debido a una proyección incorrecta. Es importante que especifiquemos el sistema de coordenadas en la pestaña inferior derecha.

																**Imagen cambiar sistema de coordenadas**   
	Seleccionamos la proyección `ETRS89 / UTM zone 30N` ó  `EPSG:25830`).   
	Tenemos todo el mapa de España por municipios dividido en dos capas, dos archivos diferentes.   
	La siguiente operación será unir o `mergear` los dos `shapefiles` para conseguir un único archivo que contenga los polígonos de todos los municipios de España.

4. Seleccionamos la pestaña `vectorial` del menú superior. Seguidamente `Herramientas de geoproceso`. Y a continuación `Unión`.
