# Practica 2 : Ejercicio Avanzado
*Araceli Macía Barrado*

# Crear una rama v0.2
1. Crear una rama v0.2.
  Para crear una rama realizo el siguiente comando
    
        git branch v0.2

1. Posiciona tu carpeta de trabajo en esta rama.

        git checkout v0.2

  A continuación muestro un pantallazo de como queda.

  ![ramacreada.png](/images/ramacreada.png)

# Añadir fichero 2.txt
1. Añadir un fichero 2.txt en la rama v0.2.

    Genero el fichero

        echo "fichero2.txt" > fichero2.txt

    lo añado al area de staging y hago un commit.

        git add -A
        git commit -m "inicio trabajo con ramas"

# Crear rama remota v0.2

1. Subir los cambios al repositorio remoto.

        git push --set-upstream origin v0.2
    
  Ahora desde la web, puedo ver que tengo las dos ramas.

  ![VistaRamas.png](/images/VistaRamas.png)

  En la rama master, no veo el fichero2.txt
    
![VistaRamas1.png](/images/VistaRamas1.png)

   En la rama v0.2 si lo veo.
    
![VistaRamas2.png](/images/VistaRamas2.png)

# Merge directo
1. Posicionarse en la rama master.

        git checkout master
    
1. Hacer un merge de la rama v0.2 en la rama master.

        git merge v0.2

Ha ido bien, a continuación muestro pantallazo. Al estar realizando el fichero README al mismo tiempo que la practica, se ve tambien en el pantallazo los ficheros que voy subiendo al repositorio.

![MergeRama.png.png](/images/MergeRama.png)

# Merge con conflicto

1. En la rama master poner Hola en el fichero 1.txt y hacer commit.

        git branch -v
        * master 05352a5 [ahead 1] ReadAvanzado cambio
        v0.2   dd0e88c [ahead 1] cambios rama2

    Estamos en la rama master,  modificamos el fichero para poner hola

        echo "HOLA" >> fichero1.txt
        git add fichero1.txt 
        git commit -m "mod fichero1"

1. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.

        git checkout v0.2
        Switched to branch 'v0.2'
        Your branch is ahead of 'origin/v0.2' by 1 commit.
        (use "git push" to publish your local commits)

   Revisamos contenido de fichero1.txt

        more fichero1.txt
        fichero1.txt 

   Añado contenido al fichero:

        echo "ADIOS" >> fichero1.txt 
        more fichero1.txt 
            fichero1.txt 
            ADIOS

  Subo el fichero al repositorio local en la rama v0.2

        git commit -a -m "mod fichero1"


1. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

        git checkout master
        Switched to branch 'master'
        Your branch is ahead of 'origin/master' by 2 commits.
          (use "git push" to publish your local commits)

    Hacemos el merge:    
   
        git merge v0.2
        Auto-merging fichero1.txt
        CONFLICT (content): Merge conflict in fichero1.txt
        Automatic merge failed; fix conflicts and then commit the result.


#Listado de ramas
1. Listar las ramas con merge y las ramas sin merge.
  
  Ramas con Merge

        git branch --merged
        * master

  Ramas sin merge

        git branch --no-merged**
        v0.2

#Arreglar conflicto
1. Arreglar el conflicto anterior y hacer un commit.

  El merge ha fallado, en el fichero1 tenemos lo siguiente:

        fichero1.txt 
        <<<<<<< HEAD
        HOLA
        =======
        ADIOS
        >>>>>>> v0.2

  Voy a quitar las lineas que me sobran y voy a hacer commit.
  Lo dejo asi:

        cat fichero1.txt
        fichero1.txt 
        HOLA
        ADIOS

        git commit -a -m "fichero1 mod"

#Borrar rama
  1. Crear un tag v0.2

     En la siguiente imagen se puede ver como he generado la etiqueta v0.2 a todo lo que llevo hecho, y luego el estado del repositorio.

     ![EtiquetarVersion](/images/EtiquetarVersion.png)

  1. Borrar la rama v0.2

      Para borrar la rama ejecuto el siguiente comando ( forzando el borrado)
        git branch -D v0.2

    Si la rama v0.2 se hubiese realizado el merge sin problemas, tambien podría haber utilizado:

        git branch -D v0.2


#Listado de cambio
  1. Listar los distintos commits con sus ramas y sus tags.

    A continuacion muestro pantallazo:
    lo que hago es ejecutar git log --oneline --decorate --graph --all, que esta incorporado
    como un alias llamado list en el fichero de configuracion de git.

   ![listadoRepositorio](/images/listadoRepositorio.png)

---
# Crear una organización
  1. Crear una organización llamada campusciff-araceliMacia
    A continuación muestro los pantallazos de como he generado la organización.

  ![CrearOrganizacion](/images/CrearOrganizacion.png)
  ![CrearOrganizacion2](/images/CrearOrganizacion2.png)

  Establezco los permisos por defecto para los permisos de la organización
  ![CrearOrganizacion4](/images/CrearOrganizacion4.png)



# Crear equipos
1. Crear 2 equipos en la organización campusciff-tunombredeusuariodegithub, uno llamado administradores con más permisos y otro colaboradores con menos permisos.

  Creo los dos equipos en la organizacion.
  ![CrearEquipos](/images/CrearEquipos.png)
  ![CrearEquipos2](/images/CrearEquipos2.png)
  ![CrearEquipos3](/images/CrearEquipos3.png)

  A continuación genero un repositorio dentro de la organización.
  ![CrearRepoorganizacion2](/images/CrearRepoorganizacion2.png)

  Ahora doy permisos sobre el repositorio, dando mas permisos para el equipo administrador que para los colaboradores.
  ![PermisosEquipos](/images/PermisosEquipos.png)
  ![PermisosEquipos2](/images/PermisosEquipos2.png)

1. Meter a github.com/asanzdiego y a 2 de vuestros compañeros de clase en el equipo administradores.

  ![AnadirMiembros](/images/AnadirMiembros.png)
  ![AnadirMiembros2](/images/AnadirMiembros2.png)
   Aqui se puede ver las invitaciones para el grupo administrador.

  ![AnadirMiembros3](/images/AnadirMiembros3.png)


1. Meter a github.com/asanzdiego y a otros 2 de vuestros compañeros de clase en el equipo colaboradores.
  
  Aquí se puede ver las invitaciones pendientes de aceptar para el equipo de colaboradores.

  ![AnadirMiembros6](/images/AnadirMiembros6.png)
  

#Crear un index.html

1. Crear un index.html que se pueda ver como página web en la organización.

  En la opción de Settings de la organización, vamos a la parte de GitHub Pages para generar el indice.
 ![CrearIndex2](/images/CrearIndex2.png)
  
  Lo genero con la opción automatica.

 ![CrearIndex3](/images/CrearIndex3.png)
 ![CrearIndex6](/images/CrearIndex6.png)

 La Url de acceso a mi organización: http://campusciff-aracelimacia.github.io/PracticaAvanzada/


#Crear Pull-requests
1. Hacer 2 forks de 2 repositorios campusciff-tunombredeusuariodegithub.github.io de 2 organizaciones de las que no seais ni administradiores ni colaboradores.
  Sobre el repositorio de dos de mis compañeros, pulso sobre el boton de Folk para hacer una copia del repositorio en uno de los mios.


![Fork1](/images/Fork1.png)
![Fork2](/images/Fork2.png)
![Fork3](/images/Fork3.png)

De modo que en mi organización veo el repositorio que he creado, y los otros dos que he copiado.
![Fork6](/images/Fork6.png)


2. Crearos una rama en cada fork.
3. En cada rama modificar el fichero index.html añadiendo vuestro nombre.
4. Con cada rama hacer un pull-request.


  En cada uno de los repositorios he generado la rama y el fichero de formas distintas. Con uno lo he hecho bajandome el repositorio en local y generando el fichero desde mi terminal, para subir las modificaciones con comandos GIT, y en el otro lo he hecho todo con la web.

  **A continuacion los pantallazos de los ejercicios realizados en local, y subiendolo luego con comandos git.**

  Clon de repositorio:
  ![CrearRama2](/images/CrearRama2.png)

  He creado una rama:
  ![CrearRama3](/images/CrearRama3.png)

  Modificado el fichero Readme, ya que el compañero aun no tiene fichero index.

  ![CrearRama4](/images/CrearRama4.png)

  Subido la rama y los cambios al repositorio remoto.
  ![CrearRama6](/images/CrearRama6..png)

  Ya veo los cambios en la web:
  ![CrearRama8](/images/CrearRama8.png)

  Hago el pullrequest en este repositorio.
   ![CrearRama10](/images/CrearRama10.png)
   ![CrearRama13](/images/CrearRama13.png)

   ** A continuación lo mismo, pero sobre el otro repositorio y haciendo los ejercicios en la web.

    Genero la rama:
    ![CrearRamaFork2](/images/CrearRamaFork2.png)

    Genero un fichero nuevo, para no tocar el Fichero Readme que veo que lo esta haciendo el compañero:
    ![CrearRamaFork3](/images/CrearRamaFork3.png)

    Hago el pullrequest:  
    ![CrearRamaFork5](/images/CrearRamaFork5.png)

    Estos son los pullrequest que tengo pendientes de aceptación:
    ![CrearRamaFork6](/images/CrearRamaFork6.png)

#Gestionar Pull-requests
  1. Aceptar los pull-request que lleguen a los repositorios de tu organización.
    Me ha llegado una solicitud. A continuación muestro los pantallazos.
  ![AceptarPullRequest2](/images/AceptarPullRequest2.png)
  ![AceptarPullRequest](/images/AceptarPullRequest.png)
   Lo confirmo:

  ![AceptarPullRequest3](/images/AceptarPullRequest3.png)

    Ya ven el mi repositorio el fichero de Juan
  ![AceptarPullRequest4](/images/AceptarPullRequest4.png)








