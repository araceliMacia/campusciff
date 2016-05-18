  *Araceli Macía* 
# Practica 1 :  

Añadir al README.md los comandos utilizados hasta ahora y hacer un commit inicial con el mensaje "commit inicial".  

 - He creado el repositorio en GITHUB ( en una versión posterior subiré el pantallazo de como se hace)
- luego he ejecutado esta sentencia para clonar el repositorio creado en remoto en mi copia en local.

  **git clone git@github.com:araceliMacia/campusciff.git** 
  
- tras realizado esto, inicializamos git
 
  **git init** 

- Una vez hecho esto, he creado en local el fichero README.md

  **echo "Generando fichero" > README.md**
   
   Procedo a modificarlo con una aplicación para editar,  y estoy utilizando el editor online : https://jbt.github.io/markdown-editor,  para visualizar lo que escribo en formado markdown, de forma que pueda asegurar el resultado una vez subido dicho fichero al repositorio a la web.

- Subir los cambios al repositorio remoto.
	1. Hago un commit, realizando la accion de añadir al area de stage en un solo paso y lo subo al repositorio remoto.
	
  **git commit -a -m "commit inicial"**
  
  **git push**

..............................

  - Ignorar archivos
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
	
      Ahora al ejecutar git status me dice lo siguiente:
      
          On branch master
			Your branch is up-to-date with 'origin/master'.
        	Untracked files:
          (use "git add <file>..." to include in what will be committed)	
            .gitignore
            nothing added to commit but untracked files present (use "git add" to track)