1.Para inicializar un repositorio local en Git, debes ejecutar el siguiente comando en la terminal 
dentro de la carpeta donde quieres crear el repositorioSe, debe ejecutar el comando git init
2.Para sistemas basados en Unix se puede utilizar el comando rm -rf .git 
Para sistema operativo windows se debe usar el comdando dir /s /q .git 
3. Si el archivo es nuevo git no lo rastrea automaticamente, debe ser agregado con el comando git add nombre_del_archivo y realizar el respectivo commit
4.Se utiliza el comando git add nombre_archivo 
5.Para determinar qué archivos fueron modificados en un repositorio Git, se puede utilizar
el comando git status, 
Si quieres ver qué cambios específicos se hicieron en los archivos. Se utiliza el comando git diff
6. git commit -m "nombre commit"
7. El commit es una forma de guardar los cambios realizado al archivo o un proyecto y por medio del cual se puede acceder a cambios posteriores o previos al commit, que ayudan a llevar un versionamiento en tu proyecto.

1.2 Practica
3--
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        luz_ortega.txt

"Untracked files" --> Son archivos que existen en tu carpeta, pero Git no los ha agregado al versionamiento. Básicamente, Git los está ignorando por ahora.
Y la linea "use git add <file>..." to include in what will be committed" → se refiere, si se desea agregar  ese archivo para que sea parte del control de versiones, y se informa el comando 
con el que se puede realizar la acción "git add <file>"

4--Agregando el archivo sandwich.txt al repositorio local
5--Cambios observados: Se mira el nombre del archivo en color verde, y nos dice que el archivo esta preparado para ser confirmado por el commit
6-- se realizo el commit
7-- Al aplica el comando en terminal aparece un hash del commit y estos detalles :
[luz_ortega 8e50cdc] Agrego mi sandwich.txt
 1 file changed, 5 insertions(+), 1 deletion(-)
El nombre del archivo sandwich.txt ya no aparece, solo aparecen los archivos que estan pendienetes por subir al versionamiento
8--Commit "Se Agrego salsas"
9--git log

-------------------------------------------------------
commit d95a946bed35cd50f2e6b9b61fa0a3ee722c261c (HEAD -> luz_ortega)
Author: luz ortega <carineortega9@gmail.com>
Date:   Wed Feb 19 13:12:57 2025 -0500

    Agrego salsas

commit 8e50cdcd483edd0cc765c20f5971d93be8ab5906
Author: luz ortega <carineortega9@gmail.com>
Date:   Wed Feb 19 13:05:17 2025 -0500

    Agrego mi sandwich.txt

commit fafdc7f0bd9a9a556a616c14ff783605909f3803 (origin/practica2025, origin/main, origin/HEAD, practica2025, main)
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:45:03 2025 -0500

    cambio readme.md

commit 5d6dc694d95afb33114a820339acfeeab38cc42a
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:39:56 2025 -0500

    cambio de rama master a main en documentación

commit 3f74d4d0db34f6f6fbcd9f8cfa4b157dccdd48d7
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
---------------------------------------------------------------------

Se enlistan todos el historial de commits con sus respetivos detalles, estan organizados del ms reciente al mas antiguo.
10--
---git log --oneline
Se muestra el historial de commits organizados , con su resoectivo hash, autor y nombre del Commit
---git log --stat
Muestra el historial de commits de una forma mas detallada incluyendo un conteo de los cambios agregados, eliminados o inserciones.

11--Inspeccionando diferencias entre commits 8e50cdc d95a946

diff --git a/1.commit/sandwich.txt b/1.commit/sandwich.txt

Indica que hay diferencias en el archivo sandwich.txt, dentro de la carpeta 1.commit.
a/1.commit/sandwich.txt → Versión anterior del archivo (commit 8e50cdc).
b/1.commit/sandwich.txt → Versión nueva del archivo (commit d95a946).

--- a/1.commit/sandwich.txt (versión anterior)
+++ b/1.commit/sandwich.txt (versión nueva)

Indican que se está comparando el archivo antes (---) y después (+++) del cambio.
@@ -5,4 +5,9 @@

Indica que los cambios comienzan en la línea 5.
Antes (-5,4): El archivo tenía 4 líneas a partir de la línea 5.
Ahora (+5,9): Tiene 9 líneas a partir de la línea 5

Este git diff está mostrando que, entre los dos commits:
Se mantuvieron algunos ingredientes del sandwich.txt.
y se agregó una lista de salsas preferidas.

14--En el historial aparece el commit recientemente aplicado.

15--En el estado aparece que el archivo  sandwich2_feo.txt` eliminado y en los commits se adiciono al
historial el commit de eliminacion de este archivo.
16--Se observa elos detalles del último commit realizado.
