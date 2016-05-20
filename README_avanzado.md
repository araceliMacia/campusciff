# Practica 2 : Ejercicio Avanzado
*Araceli Macía Barrado*

# Crear una rama v0.2
1. Crear una rama v0.2.
	Para crear una rama realizo el siguiente comando
    **git branch v0.2**

1. Posiciona tu carpeta de trabajo en esta rama.
	**git checkout v0.2**

	A continuación muestro un pantallazo de como queda.

	![ramacreada.png](/images/ramacreada.png)

# Añadir fichero 2.txt
1. Añadir un fichero 2.txt en la rama v0.2.
	Genero el fichero
	**echo "fichero2.txt" > fichero2.txt**
	lo añado al area de staging y hago un commit.
	**git add -A**
	**git commit -m "inicio trabajo con ramas"**
# Crear rama remota v0.2
1. Subir los cambios al reposiorio remoto.
	**git push --set-upstream origin v0.2**
	Ahora desde la web, puedo ver que tengo las dos ramas.

	![VistaRamas.png](/images/VistaRamas.png)

	En la rama master, no veo el fichero2.txt
![VistaRamas1.png](/images/VistaRamas1.png)

	En la rama v0.2 si lo veo.
![VistaRamas2.png](/images/VistaRamas2.png)

# Merge directo
1. Posicionarse en la rama master.

	**git checkout master**
1. Hacer un merge de la rama v0.2 en la rama master.

	**git merge v0.2**

Ha ido bien, a continuación muestro pantallazo. Al estar realizando el fichero README al mismo tiempo que la practica, se ve tambien en el pantallazo los ficheros que voy subiendo al repositorio.

![MergeRama.png.png](/images/MergeRama.png)

# Merge con conflicto
1. En la rama master poner Hola en el fichero 1.txt y hacer commit.
	**git branch -v**
	* master 05352a5 [ahead 1] ReadAvanzado cambio
  	v0.2   dd0e88c [ahead 1] cambios rama2
  	Estamos en la rama master,  modificamos el fichero para poner hola

	**echo "HOLA" >> fichero1.txt**
	**git add fichero1.txt **
	**git commit -m "mod fichero1"**

1. Posicionarse en la rama v0.2 y poner Adios en el fichero "1.txt" y hacer commit.
**git checkout v0.2**

Switched to branch 'v0.2'
Your branch is ahead of 'origin/v0.2' by 1 commit.
  (use "git push" to publish your local commits)

**more fichero1.txt** 
fichero1.txt 

**echo "ADIOS" >> fichero1.txt **
**more fichero1.txt **
fichero1.txt 
ADIOS

**git commit -a -m "mod fichero1"**

1. Posicionarse de nuevo en la rama master y hacer un merge con la rama v0.2

**git checkout master**
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 2 commits.
  (use "git push" to publish your local commits)

Hacemos el merge: 
**git merge v0.2**
Auto-merging fichero1.txt
CONFLICT (content): Merge conflict in fichero1.txt
Automatic merge failed; fix conflicts and then commit the result.


#Listado de ramas
1. Listar las ramas con merge y las ramas sin merge.
	**git branch --merged**
	* master

	**git branch --no-merged**
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
**cat fichero1.txt**
fichero1.txt 
HOLA
ADIOS

git commit -a -m "fichero1 mod"


