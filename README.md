
# Scraper de Noticias de La Republica

Este es un scraper en Python que recopila las noticias del sitio web La Republica y las almacena como archivos de texto.

## Requerimientos
Este proyecto requiere las siguientes bibliotecas de Python:

- requests
- lxml
Puede instalar estas bibliotecas usando el siguiente comando:
```bash
  pip install requests lxml
```
    
## Uso

Para usar este scraper, simplemente ejecute el archivo scraper.py:

```bash
  python scraper.py
```
Esto recopilará las noticias del día actual y las almacenará como archivos de texto en una carpeta con el formato 'DD-MM-YYYY'.

## Funcionamiento
El scraper utiliza las bibliotecas requests y lxml para obtener y analizar el contenido de la página web de La Republica. Primero se obtienen los enlaces de las noticias del día en la página principal utilizando el xpath `XPATH_LINK_TO_ARTICLE`.

Luego, para cada enlace, se utiliza la función parse_notice para obtener el título, resumen y cuerpo de la noticia utilizando los xpaths `XPATH_TITLE`, `XPATH_SUMMARY` y `XPATH_BODY`, respectivamente. Estos elementos se almacenan en un archivo de texto con el nombre del título de la noticia.

Finalmente, el archivo `scraper.py` utiliza la función `parse_home` para obtener los enlaces de las noticias y la función run para ejecutar el scraper.

## Créditos
Este scraper fue creado por Edgar Javier para fines educativos. Este proyecto es de código abierto y puede ser utilizado y modificado libremente.

