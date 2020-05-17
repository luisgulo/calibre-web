# About

Calibre-Web es una aplicacion Web con una interfaz limpia para mostrar, leer o descargar eBooks usando una base de datos existente de [Calibre](https://calibre-ebook.com).

Esta repositorio es un fork del original [calibre-web] https://github.com/janeczku/calibre-web, y este a su vez de otro:
*This software is a fork of [library](https://github.com/janeczku/calibre-webhttps://github.com/mutschler/calibreserver) and licensed under the GPL v3 License.*

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
- Support for reading eBooks directly in the browser (.txt, .epub, .pdf, .cbr, .cbt, .cbz)
- Upload new books in many formats, including audio formats (.mp3, .m4a, .m4b)
- Support for Calibre Custom Columns
- Ability to hide content based on categories and Custom Column content per user
- Self-update capability
- "Magic Link" login to make it easy to log on eReaders
- Login via LDAP, google/github oauth and via proxy authentication

## Quick start

1. Install dependencies by running `pip3 install --target vendor -r requirements.txt` (python3.x) or `pip install --target vendor -r requirements.txt` (python2.7).
2. Execute the command: `python cps.py` (or `nohup python cps.py` - recommended if you want to exit the terminal window)
3. Point your browser to `http://localhost:8083` or `http://localhost:8083/opds` for the OPDS catalog
4. Set `Location of Calibre database` to the path of the folder where your Calibre library (metadata.db) lives, push "submit" button\
   Optionally a Google Drive can be used to host the calibre library [-> Using Google Drive integration](https://github.com/janeczku/calibre-web/wiki/Configuration#using-google-drive-integration)
5. Go to Login page

**Default admin login:**\
*Username:* admin\
*Password:* admin123

**Issues with Ubuntu:**
Please note that running the above install command can fail on some versions of Ubuntu, saying `"can't combine user with prefix"`. This is a [known bug](https://github.com/pypa/pip/issues/3826) and can be remedied by using the command `pip install --system --target vendor -r requirements.txt` instead.

## Requirements

python 3.x+, (Python 2.7+)

Optionally, to enable on-the-fly conversion from one ebook format to another when using the send-to-kindle feature, or during editing of ebooks metadata:

[Download and install](https://calibre-ebook.com/download) the Calibre desktop program for your platform and enter the folder including program name (normally /opt/calibre/ebook-convert, or C:\Program Files\calibre\ebook-convert.exe) in the field "calibre's converter tool" on the setup page.

\*** DEPRECATED \*** Support will be removed in future releases

[Download](http://www.amazon.com/gp/feature.html?docId=1000765211) Amazon's KindleGen tool for your platform and place the binary named `kindlegen` in the `vendor` folder.

## Docker Images

Pre-built Docker images are available in these Docker Hub repositories:

#### **Technosoft2000 - x64**
+ Docker Hub - [https://hub.docker.com/r/technosoft2000/calibre-web/](https://hub.docker.com/r/technosoft2000/calibre-web/)
+ Github - [https://github.com/Technosoft2000/docker-calibre-web](https://github.com/Technosoft2000/docker-calibre-web) 

    Includes the Calibre `ebook-convert` binary.
    + The "path to convertertool" should be set to `/opt/calibre/ebook-convert`

#### **LinuxServer - x64, armhf, aarch64**
+ Docker Hub - [https://hub.docker.com/r/linuxserver/calibre-web/](https://hub.docker.com/r/linuxserver/calibre-web/)
+ Github - [https://github.com/linuxserver/docker-calibre-web](https://github.com/linuxserver/docker-calibre-web)
+ Github - (Optional Calibre layer) - [https://github.com/linuxserver/docker-calibre-web/tree/calibre](https://github.com/linuxserver/docker-calibre-web/tree/calibre) 

   This image has the option to pull in an extra docker manifest layer to include the Calibre `ebook-convert` binary.  Just include the environmental variable `DOCKER_MODS=linuxserver/calibre-web:calibre` in your docker run/docker compose file. **(x64 only)**
  
   If you do not need this functionality then this can be omitted, keeping the image as lightweight as possible.
    
   Both the Calibre-Web and Calibre-Mod images are rebuilt automatically on new releases of Calibre-Web and Calibre respectively, and on updates to any included base image packages on a weekly basis if required.
   + The "path to convertertool" should be set to `/usr/bin/ebook-convert`
   + The "path to unrar" should be set to `/usr/bin/unrar`

# Wiki

For further information, How To's and FAQ please check the [Wiki](https://github.com/janeczku/calibre-web/wiki)
