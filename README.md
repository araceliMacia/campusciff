 
# Practica 1 :  
*Por: Araceli Macía Barrado*

# Repositorio campusciff

 1. Crear un repositorio en vuestro GitHub llamado campusciff 

  Desde la web de GitHub y una vez logada con  [mi usuario](https://github.com/araceliMacia/campusciff), realizo los pasos para crear el repositorio

![CreoRepositorio1](/images/CreoRepositorio1.png)

![CreoRepositorio3](/images/CreoRepositorio3.png)

Una vez creado el repositorio remoto, copio la cadena SSH del repositorio remoto.

![CreoRepositorio4](/images/CreoRepositorio4.png)

Desde el terminal ejecuto:

  **git clone git@github.com:araceliMacia/campusciff.git** 
  
- tras realizado esto, inicializamos git
 
  **git init** 

# README

- Una vez hecho esto, he creado en local el fichero README.md

  **echo "Generando fichero" > README.md**
   
   Procedo a modificarlo con una aplicación para editar,  y estoy utilizando el editor online : https://jbt.github.io/markdown-editor,  para visualizar lo que escribo en formado markdown, de forma que pueda asegurar el resultado una vez subido dicho fichero al repositorio a la web.

# Commit Inicial

*  Hago un commit, realizando la accion de añadir al area de stage en un solo paso y lo subo al repositorio remoto.

  **git commit -a -m "commit inicial"**
  
# Push inicial

   **git push**

A continuación desde la web, veo como esta quedando el fichero README.md ( es una versión anterior a la que estas viendo ahora)

![PrimerReadme](/images/ReadPrimero.png)


# Ignorar archivos

* Crear en el repositorio local un fichero llamado privado.txt
  	
  **echo "Inicial" > privado.text**
           
 * Crear en el repositorio local una carpeta llamada privada.
  
    **mkdir privada**
    
    dentro de la carpet privada genero otro fichero, de modo que al realizar **git status** veo esto:
         
         	On branch master
            Your branch is up-to-date with 'origin/master'.
            Untracked files:
              (use "git add <file>..." to include in what will be committed)

                privada/
                privado.text
    
* Realizar los cambios oportunos para que tanto el archivo como la carpeta sean ignorados por git.
    
   He generado un fichero **.gitignore** con el siguiente contenido:
        
   privado.text

   /privada
	
   Ahora al ejecutar git status obtengo lo siguiente:
      
          On branch master
			Your branch is up-to-date with 'origin/master'.
        	Untracked files:
          (use "git add <file>..." to include in what will be committed)	
            .gitignore
            nothing added to commit but untracked files present (use "git add" to track)

# Añadir fichero 1.txt

* Añadir fichero 1.txt al repositorio local
Genero el fichero: 

**echo "fichero1.txt " > fichero1.txt**
         
Lo añado a la area de staging.
		 
**git add fichero1.txt**
         
lo subo al repositorio local
         
**git commit -m "Vers. con fichero1.txt"**

Ahora al ejecutar un git list obtengo lo siguiente:
         
		 	* 3649d55 (HEAD -> master) Vers. con fichero1.txt
			* dcae639 (origin/master) Vers. ignorando archivos
			* e81c831 Ver con gigignore
			* 0b69fa9 Fin Parte 1 Pract 1
			* 092a819 commit inicial
			* 55bb5dd Subo fichero README.md
		
Aqui vemos los commits con las comentarios que he ido subiendo al repositorio local.

# Crear el tag v0.1

* Crear un tag v0.1.
	
**git tag v0.1**
        
Ahora al realizado un git list, ya veo la etiqueta del ultimo commit.

          * 3649d55 (HEAD -> master, tag: v0.1) Vers. con fichero1.txt
          * dcae639 (origin/master) Vers. ignorando archivos
          * e81c831 Ver con gigignore
          * 0b69fa9 Fin Parte 1 Pract 1
          * 092a819 commit inicial
          * 55bb5dd Subo fichero README.md

# Subir el tag v0.1

* Subir los cambios al repositorio remoto.

Una vez que ya esta todo "commitado" lo subo al repositorio local con:

**git push**



---
# Cuenta de GitHub
1. Poner una foto en vuestro perfil de GitHub.

  He accedido a la web para configurar una foto en mi perfil.
  ![MiFotoPerfil](/images/ProfilePicture.png)

1. Poner el doble factor de autentificación en vuestra cuenta de GitHub.
  He accedido al menú de Security para configurar el doble factor de autentificación.
![DobleAutentificacion1](/images/DobleAutentificacion1.png)
![DobleAutentificacion3](/images/DobleAutentificacion3.png)

   He seleccionado la opcion de mensaje de texto a mi número de móvil, y también he guardado los códigos de recuperación.

1. Añadir (si no lo habéis hecho ya) la clave pública que se corresponde a tu ordenador.

  Esto ya lo hice en la clase, y lo tengo correctamente configurado.

# Uso social de GitHub

1. Preguntar los nombres de usuario de GitHub de tus compañeros de clase, búscalos, y sigueles.
1. Seguir los repositorios campusciff del resto de tus compañeros.
1. Añadir una estrella a los repositorios campusciff del resto de tus compañeros.

En las siguientes imagenes muestro que me estoy siguiendo a varios compañeros, asi como varios compañeros a mi. 
Tambien se puede ver que he añadido una entralla a los repositorios de algunos compañeros.

![SiguiendoCompaneros](/images/SiguiendoCompaneros.png)

![PuntuandoEstrellas2](/images/PuntuandoEstrellas2.png)

# Crear una tabla

Crear una tabla de este estilo en el fichero README.md con la información de varios de tus compañeros de clase.

|Nombre Compañero   | Enlace GitHun   |
|---|---|
|Ainhoa Calvo   |[Ainhoa](https://github.com/AinhoaCE)    |
| Anna Lawrenc  |[Anna](https://github.com/annalawrenc)    |
| Enrique Serrano Muñoz|[Enrique](https://github.com/eserranom)    |
| Juan Antonio García Cuevas|[Juan Antonio](https://github.com/juangarciaciff)|

# Colaboradores
1. Poner a github.com/asanzdiego como colaborador del repositorio campusciff

A continuación muestro los pantallazos de lo que he hecho para incluir a Adolfo Sanz como colaborador del repositorio.
![NuevoColaborador](/images/NuevoColaborador.png)

![NuevoColaborador2](/images/NuevoColaborador2.png)

