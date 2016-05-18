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


