# Actividad intermedia del curso GIT
NOTA: Se recomienda el uso de Markdown como formato de texto y la herramienta web dillinger.io

### 1.Crear un repositorio en Gitlab o Github y agregar los archivos de texto relacionados a la clase (actividades, resoluciones de las actividades, anotaciones que pueden ser públicas, imágenes, gráficos, datos, etc).

### 2.Crear al menos dos versiones (commits) distintas y obtener una captura con la salida del comando logs donde se vean esos commits.
```sh
 upa6-samo3@upa6-samo3:~/Documentos/curso GIT$ git commit -m "modificacion del archivo README.MD"
[main dc41221] modificacion del archivo README.MD
 1 file changed, 3 insertions(+), 1 deletion(-)
upa6-samo3@upa6-samo3:~/Documentos/curso GIT$ git push
Enter passphrase for key '/home/upa6-samo3/.ssh/id_ed25519': 
Enumerando objetos: 5, listo.
Contando objetos: 100% (5/5), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (2/2), listo.
Escribiendo objetos: 100% (3/3), 353 bytes | 353.00 KiB/s, listo.
Total 3 (delta 0), reusados 0 (delta 0), pack-reusados 0
To github.com:CharlyUpa/IPAP-GIT.git
   64f72cd..dc41221  main -> main
```


### 3.Pushear el proyecto y obtener una captura del directorio raíz del proyecto en la plataforma utilizada (Github o Gitlab).
- La captura se encuentra en el archivo "captura2commits.png"

### 4.Enumerar y describir las principales diferencias entre Subversion y Git (no más de 1 carilla).
los Sistemas de Control de Versiones (VCS) se dividen en dos grandes grupos: VCS Centralizados (ejemplificados por Subversion, Perforce, etc.) y VCS Distribuidos (ejemplificados por Git, Mercurial, etc.) y la principal diferencia entre estas esta dada por la arquitectura del repositorio:
 - En los VCS Centralizados como Subversion, hay un servidor como repositorio central que almacena la "copia oficial" del código y mantiene la única versión del historial del repositorio. Los desarrolladores realizan "checkouts" de esta única versión a sus copias locales.
 - En los VCS Distribuidos como Git, no se realiza un "checkout" de un repositorio central. En cambio, se realizan operaciones de "clone" y "pull" de los cambios del repositorio. Cada repositorio local en Git es una copia completa de todo lo que hay en el servidor (repositorio remoto), incluyendo todo el historial de versiones.

### 5.Enumerar y describir las principales diferencias entre Gitlab y Github (no más de 1 carilla).

 - Github es un sitio donde se alojan proyectos utilizando el sistema de control de versiones Git. Se utiliza principalmente para la creación y control de versiones de código fuente de sistemas informaticos. 
 
 - Gitlab es definida como una compañía de núcleo abierto y el principal proveedor del software GitLab, que es un servicio web que proporciona el servicio para alojar proyectos, control de versiones y desarrollo basado en Git.

Las diferencias principales según comprendo es que:

- Aunque ambos sirven como plataformas para la gestión de repositorios Git, la descripción de Github se centra más en ser un sitio para el almacenamiento de proyectos, especialmente de código fuente. mientras que, segun la descripción de Gitlab, enfatiza su naturaleza como una compañía de "núcleo abierto" que provee un servicio web que abarca no solo la gestión de versiones sino también funcionalidades de desarrollo (facilitando herramientas que mejoren el desarrollo de nuevo codigo).
