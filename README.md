# practica-etl-dgii-edesur

# Proyecto ETL: DGII y EDESUR

Este proyecto realiza la extracción, transformación y carga (ETL) de dos grandes conjuntos de datos hacia una base de datos MySQL hospedada en Aiven.

## Tecnologías utilizadas:
* **Python 3.x**: Lenguaje principal.
* **Pandas**: Para el procesamiento de datos y técnica de *Chunking* (lectura por bloques).
* **SQLAlchemy**: Para la conexión eficiente con MySQL.
* **Aiven**: Hosting de la base de datos en la nube.

## Estructura del Proyecto:
1. **RNC (DGII)**: Se procesaron millones de registros usando bloques de 50,000 filas para optimizar la memoria RAM.
2. **Cobros EDESUR**: Se normalizaron nombres de columnas y formatos de fecha antes de la carga.
3. **Vistas SQL**: Se crearon vistas para segmentar contribuyentes por Régimen (RST y Normal) y por provincias.
