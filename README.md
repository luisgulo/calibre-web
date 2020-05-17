# CALIBRE-WEB

Calibre-Web es una aplicacion Web con una interfaz limpia para mostrar, leer o descargar eBooks usando una base de datos existente de [Calibre](https://calibre-ebook.com).

Esta repositorio es un fork del original [calibre-web] https://github.com/janeczku/calibre-web, y este a su vez de otro:

*Calibre-Web es un fork de [library](https://github.com/janeczku/calibre-webhttps://github.com/mutschler/calibreserver) y esta bajo la licencia GPL v3.*

![Main screen](https://github.com/janeczku/calibre-web/wiki/images/main_screen.png)

## Características

- Interaz Bootstrap 3 con HTML5
- Totalmente configurable en modo gráfico
- Gestion de permisos de usuario perfectamente detallada
- Interfaz de Administrador
- Intefaz disponible en Español. Y también en: czech, dutch, english, finnish, french, german, hungarian, italian, japanese, khmer, polish, russian, simplified chinese, swedish, turkish, ukrainian
- OPDS feed for eBook reader apps 
- Se puede filtrar y buscar por título, autor, etiqueta, serie e idioma
- Se pueden crear colecciones propias de libros -Estanterías- (Shelves)
- Permite editar metadatos de los eBooks o borrarlos de Calibre (sólo si has concedido permiso para ello al usuario)
- Permite convertir a otros formatos de eBooks (usando los binarios de Calibre)
- Permite restringir la descarga de eBook a los usuarios
- Suporte de registro público a los usuarios.
- Puede enviar los eBooks a dispositivos Kindle simplemente haciendo click en un botón
- Sincroniza los dispositivos Kobo a través de Calibre-Web con tu librería Calibre
- Soporte para leer directamente eBooks desde el navegador .txt, .epub, .pdf, .cbr, .cbt, .cbz)
- Permite subir nuevos eBools en varios formatos, incluso audio (.mp3, .m4a, .m4b)
- Suporta las columnas personalizadas de Calibre
- Permite habilitar el contenido oculto basado en las categorias personalizadas del usuario
- Capacidad de Auto-Actualización (NO USAR, A MI ME FALLA con PYTHON 2.7)
- Permite "Enlaces Mágicos (Magic Link)" a login para crear facilmente log de lectores
- Permite Login via LDAP, google/github oauth u otra autenticación via proxy

## INSTALACION RAPIDA (Chequeado en Debian 10 Buster)
1. Revise su versión de python activa ejecutando `python --version`
2. Debe de tener pip ó pip3 instalado:

   2a. Si su version de python es 2.7.x asegurese de tener instalado pip. `apt-get -y install python-pip`
   
   2b. Si su version de python es 3.x asegurese de tener instalado pip. `apt-get -y install python3-pip`
3. Cambiese a la ruta donde ha instalado el programa e instale las dependencias segun su versión de python:

   3a. Para python 2.7.x ejecute: `pip install --target vendor -r requirements.txt`
   
   3b. Para python 3.x   ejecute: `pip3 install --target vendor -r requirements.txt`   
   
4. Ya puede inicar el programa. 
   4a. Lanzar mientras etamos en la consola. Simplemente escriba: `python cps.py` 
   
   4b. Para dejarlo lanzado permanentemente, utilice el comando: `nohup python cps.py &`
   
5. Comprobar funcionamiento en el navegador:   

   5a. Utilice la URL `http://localhost:8083` ó `http://nombre.de.su.servidor:8083`
   
   5b. Para acceder al catalogo OPDS navege a: `http://localhost:8083/opds` ó `http://nombre.de.su.servidor:8083/opds`
   
6. Cuando inicie le pedirá `Location of Calibre database` debe escribir la Ruta Absoluta en donde tiene la librería de Calibre (en donde se encuentra el fichero metadata.db), pulse el botón  "Submit" button
NOTA: Opcionalmente puede integar Google Drive para almacenar su libreria Calibre. [-> Usar integración con Google Drive](https://github.com/janeczku/calibre-web/wiki/Configuration#using-google-drive-integration)
7. Se le pedira el login inicial para acceder y configurar el servidor.

**Login por defecto para el usuario admin:**\
*Username:* admin\
*Password:* admin123


## Requisitos

python 3.x+ ó Python 2.7+

Para el uso de imágenes Docker de calibre-web se recomienda visita el proyecto original y sus notas en [calibre-web] https://github.com/janeczku/calibre-web

# Wiki

Para información extra, FAQs y otros detalles, visite [Wiki de calibre-web](https://github.com/janeczku/calibre-web/wiki)

## Este es un FORK No oficial de Calibre-Web. Código sometido a la licencia GPL v3
