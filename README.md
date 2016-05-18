 
# Practica 1 :  
*Por: Araceli Macía Barrado*

![UrlCorta](/images/CreoRepositorio1.png)

![urlLarga](
https://github.com/araceliMacia/campusciff/blob/master/images/CreoRepositorio1.png)

# Repositorio campusciff

 nicial con el mensaje "commit inicial".  

 - He creado el repositorio en GITHUB ( en una versión posterior subiré el pantallazo de como se hace)
  luego he ejecutado esta sentencia para clonar el repositorio creado en remoto en mi copia en local.

  **git clone git@github.com:araceliMacia/campusciff.git** 
  
- tras realizado esto, inicializamos git
 
  **git init** 

# README

- Una vez hecho esto, he creado en local el fichero README.md

  **echo "Generando fichero" > README.md**
   
   Procedo a modificarlo con una aplicación para editar,  y estoy utilizando el editor online : https://jbt.github.io/markdown-editor,  para visualizar lo que escribo en formado markdown, de forma que pueda asegurar el resultado una vez subido dicho fichero al repositorio a la web.

# Subir los cambios al repositorio remoto.
*  Hago un commit, realizando la accion de añadir al area de stage en un solo paso y lo subo al repositorio remoto.


  **git commit -a -m "commit inicial"**
  
   **git push**

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

*Subir los cambios al repositorio remoto.

Una vez que ya esta todo "commitado" lo subo al repositorio local con:

**git push**


# Crear una tabla

Crear una tabla de este estilo en el fichero README.md con la información de varios de tus compañeros de clase.

|Nombre Compañero   | Enlace GitHun   |
|---|---|
|Ainhoa Calvo   |[Ainhoa](https://github.com/AinhoaCE)    |
| Anna Lawrenc  |[Anna](https://github.com/annalawrenc)    |
| Enrique Serrano Muñoz|[Enrique](https://github.com/eserranom)    |
| Juan Antonio García Cuevas|[Juan Antonio](https://github.com/juangarciaciff)|




