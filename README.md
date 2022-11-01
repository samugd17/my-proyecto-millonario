<div align="justify">

# Manipulación Avanzada en Git (trabajo con tags y ramas).

Crear un repositorio en vuestro GitHub llamado **my-proyecto-millonario**.

Clonar vuestro repositio en local.

## README

Crear (si no lo habéis creado ya) en vuestro repositorio local
un documento **README.md**.

## Commit inicial

Añadir al README.md los comanddos utilizados hasta ahora
y hacer un coomit inicial con el mensaje **commit inicial**.

## Push inicial

Subir los cambios al repositorio remoto.


> Pregunta: Si has clonado el repositorio, puede que parte del comando anterior puedas omitirlo. Justifica tu respuesta en el fichero **README.md**.
  
- En mi caso, yo  me he saltado estos pasos iniciales, ya que al crear el repositorio he clicado sobre la opción _Add a README file_ que nos brinda Github a la hora de crear un repositorio.

<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/Add%20a%20readme%20file.png" >
</div>
  
## Ignorar archivos
  
**1.** Crear en el repositorio local un fichero llamado **privado.txt**.

**2.** Crear en el repositorio local una carpeta llamada **privada**.

**3.** Realizar los cambios oportunos para que tanto el archivo como
la carpeta sean ignorados por git.
  
</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/1.%20Hasta%20ignorar%20archivos.png?raw=true" >
</div>
</br>

> Pregunta: el fichero y el directorio privado debe de subir al repositorio si se encuentra añadido al fichero .gitingnore. [Si/No]. Justifica tu respuesta en el fichero README.md.

- Tanto el fichero como el directorio privado no serán subidos al repositorio gracias a la acción del _".gitignore"_, cuyo misión consiste decirle a Git qué archivos o directorios completos debe ignorar y no subir al repositorio de código. No todos los archivos y carpetas son necesarios de gestionar a partir del sistema de control de versiones. Hay código que no necesitas enviar a Git, ya sea porque sea privado para los desarrolladores y no lo necesiten (o lo deban) conocer el resto de las personas.

## Añadir fichero 1.txt

Añadir fichero **1.txt** al repositorio local.

> Pregunta: Las acciones add y commit, que realiza cada una sobre el/los ficheros. Justifica tu respuesta en el fichero **README.md**.
- Por una parte, la acción _"git add"_ añade cambios en el directorio de trabajo. Por su parte, _"Git commit"_ confirma estos cambios y permite asociarles una pequeña descripción para saber que ha hecho el cambio.

## Crear y subir el tag v0.1

**1.** Crear un tag **v0.1**.  

**2.** Subir los cambios al repositorio remoto.

> Pregunta: ¿Qué es un tag sobre un repositorio git, en nuestro caso Github?. Justifica tu respuesta en el fichero README.md.

- A través del comando _"git tag"_ podemos crear etiquetas. Cuando hablamos de Git tag no nos referimos a la versión de un archivo en particular, sino de todo el proyecto de manera global. Sirve para etiquetar con un tag el estado del repositorio completo, algo que se suele hacer cada vez que se libera una nueva versión del software.

## Crear una rama v0.2

**1.** Crear una rama **v0.2**.

**2.** Posiciona tu carpeta de trabajo en esta rama.

## Añadir fichero 2.txt

Añadir un fichero **2.txt** en la rama **v0.2**.


> Pregunta: Cuando estamos trabajando con ramas, cual es su fin, y sentido en organizaciones pequeñas/medianas/grandes. Justifica tu respuesta en el fichero README.md.

- Las ramas en Git, proporcionan un entorno aislado para cada cambio en tu código base. Es una forma de organizar éste, en una especie de subcarpetas, las cuales están compuestas cada una por ejemplo de una funcionalidad del código. De esta forma, cuando queramos implementar una nueva utilidad, podremos hacerlo sin poner en peligro todo el código base. Una vez esté hecho y bien probado, podremos fusionarlo con nuestro código base a través de la función git “merge”. Esto garantiza que la rama principal siempre contenga código de calidad para producción. 

- Las ramas son muy útiles en todo tipo de organizaciones, ya que como mencionamos anteriormente,  permite crear o avanzar en diferentes funcionalidades del código de forma simultánea, ordenada para cada grupo de desarrolladores y sin poner en riesgo el código base.

## Crear rama remota v0.2

Subir los cambios al repositorio remoto.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/2.%20Hasta%20crear%20rama%20remota%200.2.png?raw=true" >
</div>
</br>

## Merge directo

1. Posicionarse en la rama **master/main** según sea tu rama principal.
2. Hacer un merge de la rama **v0.2** en la rama **master/main**.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/3.%20Hasta%20Merge%20con%20conflicto.png?raw=true" >
</div>
</br>

> Pregunta: Se tendrían que producir conflictos en esta acción. [Si/No] Justifica tu respuesta en el fichero README.md.

- No se tiene por qué producir un conflicto en esta acción, ya que antes de fusionar la rama v0.2, hemos hecho un _"git checkout"_ a la rama _"main"_, situándonos sobre ella y ahi hemos pedido el _"merge"_ de la anterior. 

## Merge con conflicto

**1.** En la rama **master/main** poner **Hola** en el fichero **1.txt** y hacer commit.

**2.** Posicionarse en la rama **v0.2** y poner **Adios** en el fichero "1.txt" y hacer commit.

**3.** Posicionarse de nuevo en la rama **master/main** y hacer un merge con la rama **v0.2**.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/4.%20Hasta%20Merge%20con%20conflicto%20antes%20de%20vim.png?raw=true" >
</div>
</br>

## Listado de ramas

Listar las ramas con merge y las ramas sin merge.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/5.%20Listado%20de%20ramas.png" >
</div>
</br>

## Arreglar conflicto

Arreglar el conflicto anterior y hacer un commit.

- Lo hacemos a través del comando _"vim 1.txt"_, el cual nos permitirá  abrir un editor de código donde podremos elegir con qué versión quedarnos definitivamente además de poder editarla.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/VIM.png" >
</div>
</br>

- Una vez lo hayamos seleccionado y guardado, paramos el proceso con "ctrl + z".
- Realizamos el _"add y commit"_.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/6.%20Conflicto%20arreglado.png" >
</div>
</br>

## Borrar rama

**1.** Crear un tag **v0.2**

**2.** Borrar la rama **v0.2**

## Listado de cambios

Listar los distintos commits con sus ramas y sus tags.

</br>
<div align="center">
  <img src="https://github.com/samugd17/my-proyecto-millonario/blob/main/IMG/7.%20Final.png" >
</div>
</br>

<div align="right">
  Samuel Eloy González Díaz. 1ºDAW.
</div>  


</div>
