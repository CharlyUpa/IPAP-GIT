# Actividad INTEGRADORA del curso GIT

## Resolucion de conflictos al mergear ramas main - proyectos
Al momento de mergear las ramas se produjo un error para la combinacion de los archivos README.md, y la forma de solucionarlo fue abrir el archivo donde tenia tanto la informacion que tenia el archivo original como el de la rama proyectos. Decidi dejar la info de los dos archivos combinandolos. para luego volver a realizar el git add . -> git commit -> git push.
```sh
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git checkout proyectos
Cambiado a rama 'proyectos'
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git status
En la rama proyectos
Cambios no rastreados para el commit:
  (usa "git add <archivo>..." para actualizar lo que será confirmado)
  (usa "git restore <archivo>..." para descartar los cambios en el directorio de trabajo)
	modificados:     README.md

sin cambios agregados al commit (usa "git add" y/o "git commit -a")
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git add . 
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git commit -m "modifico readme"
[proyectos c931c7d] modifico readme
 1 file changed, 1 insertion(+), 1 deletion(-)
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git push
fatal: The current branch proyectos has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin proyectos

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git push origin proyectos
Enter passphrase for key '/home/upa6-samo3/.ssh/id_ed25519': 
Enumerando objetos: 10, listo.
Contando objetos: 100% (10/10), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (8/8), listo.
Escribiendo objetos: 100% (8/8), 928 bytes | 928.00 KiB/s, listo.
Total 8 (delta 4), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To github.com:CharlyUpa/IPAP-GIT.git
   c898941..c931c7d  proyectos -> proyectos
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git checkout main
Cambiado a rama 'main'
Tu rama está adelantada a 'origin/main' por 1 commit.
  (usa "git push" para publicar tus commits locales)
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git merge proyectos
Auto-fusionando 3-ActividadIntegradora/README.md
CONFLICTO (agregar/agregar): Conflicto de fusión en 3-ActividadIntegradora/README.md
Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git add .
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git commit -m "soluciono conflictos al realizar el merge"
[main 73b24d1] soluciono conflictos al realizar el merge
upa6-samo3@upa6-samo3:~/Documentos/curso GIT/3-ActividadIntegradora$ git push origin main
Enter passphrase for key '/home/upa6-samo3/.ssh/id_ed25519': 
Enumerando objetos: 14, listo.
Contando objetos: 100% (14/14), listo.
Compresión delta usando hasta 4 hilos
Comprimiendo objetos: 100% (8/8), listo.
Escribiendo objetos: 100% (9/9), 1.22 KiB | 1.22 MiB/s, listo.
Total 9 (delta 4), reusados 0 (delta 0), pack-reusados 0
remote: Resolving deltas: 100% (4/4), completed with 1 local object.
To github.com:CharlyUpa/IPAP-GIT.git
   3d07052..73b24d1  main -> main

```
NOTA: uno de los puntos del ejercicio era el siguiente, no supe donde ponerlos. 
###### Elección de tecnología: Describir al menos dos de los servicios a libre elección que aparecen como templates en la creación de proyectos en Gitlab.
- En mi caso no uso gitlab, sino github. En cuanto a los templates posibles para elegir se encuentran: 
  1- Plantillas de CI: Son archivos YAML que constan de trabajos, anclas y etapas
Se hacen referencia a ellas en un archivo gitlab-ci.yml diferente de un proyecto para ejecutar su flujo de trabajo
  2- Plantillas de problemas: Mejoran los flujos de trabajo de los proyectos
Garantizan informes de problemas coherentes y exhaustivos, Permiten una resolución de problemas más eficiente.
  3- Plantillas de proyectos: Cualquier usuario autenticado puede seleccionar proyectos públicos e internos como plantilla para un nuevo proyecto Los proyectos privados sólo pueden ser seleccionados por usuarios que sean miembros de los proyectos.
  4- Plantillas de grupos: Permiten compartir plantillas genéricas para evitar repeticiones

otra clasificacion de los templates:
 - 1.Static Site Generator: Un template que proporciona una estructura básica para construir sitios web estáticos utilizando generadores como Jekyll o Hugo. Este template podría incluir una configuración inicial, ejemplos de estructura de carpetas y un flujo de despliegue básico.
 - 2.Basic Web Application (Python/Node.js): Un template que configura un proyecto web básico utilizando un framework popular como Flask (Python) o Express.js (Node.js). Podría incluir una estructura de proyecto estándar, archivos de configuración iniciales y quizás un ejemplo de "Hola Mundo" funcional.

###### Mi repositorio del curso: https://github.com/CharlyUpa/IPAP-GIT
