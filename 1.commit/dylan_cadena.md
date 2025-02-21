## Ejercicio 1

### 1.1. Respuestas

1.  Se debe ejecutar el siguiente comando dentro del directorio donde se quiere crear el repositorio git init

2.   Se debe eliminar la carpeta oculta .git dentro del directorio rm -rf .git

3.  No inmediatamente. El archivo solo será controlado por Git cuando se agregue al área de preparación con git add y se confirme con un git commit.

4. Se usa el siguiente comando git add <nombre_del_archivo> 
   

5. Se utiliza el siguiente comando git status  
 

6.  Se usa el siguiente comando git commit -m "Mensaje descriptivo del cambio"

7.  Un commit es una confirmación de cambios en el repositorio para ser enviados y registrados al repositorio principal donde se este trabajando


### 1.2. Ejercicio Práctico

3. git status
On branch dylan_cadena
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   1.commit/sandwich.txt



no changes added to commit (use "git add" and/or "git commit -a")

significa que me encuentra en la rama dylan_cadena y que los cambios realizados en sandiwch y dylan_cadena.md y no se han añadido al stage area (SA) de momento.

5. On branch dylan_cadena
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   sandwich.txt
Significa que los cambios del archivo pasaron al stage area y estan listos para aplicarles un commit

7. la salida indica que el cambio fue aceptado para el repositorio

9. dilan@DESKTOP-KPK1AU9 MINGW64 ~/Desktop/Taller1/tallergit/1.commit (dylan_cadena)
 git log
commit 2ee2b53470b4260ed08b1f57e73bad768e7383cf (HEAD -> dylan_cadena)
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:48:39 2025 -0500

    agrego salsas

commit 727886247f9f7aee433ca9e05dd5f83afcc45e9a
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:46:29 2025 -0500

    agrego mi sandwich

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
Date:   Mon Feb 17 23:17:02 2025 -0500

    primer commit
(END) 

Lo mostrado en terminal son los commits que se han realizado y aparaecen en orden del mas reciente al mas antiguo

10.  git log --oneline
2ee2b53 (HEAD -> dylan_cadena) agrego salsas
7278862 agrego mi sandwich
fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025, main) cambio readme.md
5d6dc69 cambio de rama master a main en documentación
3f74d4d primer commit

es como el anterior git log pero se muestra de una manera mas resumida


git log --stat
commit 2ee2b53470b4260ed08b1f57e73bad768e7383cf (HEAD -> dylan_cadena)
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:48:39 2025 -0500

    agrego salsas

 1.commit/sandwich.txt | 2 ++
 1 file changed, 2 insertions(+)

commit 727886247f9f7aee433ca9e05dd5f83afcc45e9a
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:46:29 2025 -0500

    agrego mi sandwich

 1.commit/sandwich.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

commit fafdc7f0bd9a9a556a616c14ff783605909f3803 (origin/practica2025, origin/main, origin/HEAD, practica2025, main)
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:45:03 2025 -0500

    cambio readme.md

 README.md | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

commit 5d6dc694d95afb33114a820339acfeeab38cc42a
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:39:56 2025 -0500

    cambio de rama master a main en documentación

 2.branchs/README.md   | 16 ++++++++--------
 3.conflicts/README.md | 10 +++++-----
 README.md             |  7 +++++--
 3 files changed, 18 insertions(+), 15 deletions(-)

commit 3f74d4d0db34f6f6fbcd9f8cfa4b157dccdd48d7
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:17:02 2025 -0500

    primer commit

 .gitignore               |  2 ++
 1.commit/README.md       | 55 ++++++++++++++++++++++++++++++++++
 1.commit/sandwich.txt    |  4 +++
 2.branchs/README.md      | 78 ++++++++++++++++++++++++++++++++++++++++++++++++
 2.branchs/pizza.txt      |  3 ++
 3.conflicts/README.md    | 48 +++++++++++++++++++++++++++++
 3.conflicts/milanesa.txt |  2 ++
 README.md                | 54 +++++++++++++++++++++++++++++++++
 8 files changed, 246 insertions(+)
(END)

Es como el git log inicial pero este es mas detallado indicando ramas, archivos editados, eliminados entre otras cosas


11. revisar punto


14. git status
On branch dylan_cadena
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        deleted:    sandwich2.txt

Indica que sandwich2 fue regresado al stage area para editarlo y volverle a hacer un commit ya con el nombre cambiado a sandwich2feo

15. git log --oneline
5256273 (HEAD -> dylan_cadena) sandwich2 eliminado
448a679 agrego sandwich2
71386c4 agrego sandwich2
2ee2b53 agrego salsas
7278862 agrego mi sandwich
fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025, main) cambio readme.md
5d6dc69 cambio de rama master a main en documentación
3f74d4d primer commit

el archivo sandwich2feo fue eliminado pero sigue en el historial de versiones de git

16.  git log --stat
commit 5256273096a66df6234baeb4065445dff8b43161 (HEAD -> dylan_cadena)
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 23:26:14 2025 -0500

    sandwich2 eliminado

 1.commit/sandwich2_feo.txt | 4 ----
 1 file changed, 4 deletions(-)

commit 448a679de233cd01845e9f7befcc8d83dcc2f8a3
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 23:19:02 2025 -0500

    agrego sandwich2

 1.commit/sandwich2.txt | 4 ----
 1 file changed, 4 deletions(-)

commit 71386c48d62dc057b7071026fb12ea343fa4a57a
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 23:14:52 2025 -0500

    agrego sandwich2

 1.commit/sandwich2.txt     | 4 ++++
 1.commit/sandwich2_feo.txt | 4 ++++
 2 files changed, 8 insertions(+)

commit 2ee2b53470b4260ed08b1f57e73bad768e7383cf
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:48:39 2025 -0500

    agrego salsas

 1.commit/sandwich.txt | 2 ++
 1 file changed, 2 insertions(+)

commit 727886247f9f7aee433ca9e05dd5f83afcc45e9a
Author: Dylan Cadena <dylancv@udenar.edu.co>
Date:   Thu Feb 20 22:46:29 2025 -0500

    agrego mi sandwich

 1.commit/sandwich.txt | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)

commit fafdc7f0bd9a9a556a616c14ff783605909f3803 (origin/practica2025, origin/main, origin/HEAD, practica2025, main)
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:45:03 2025 -0500

    cambio readme.md

 README.md | 4 ++--
 1 file changed, 2 insertions(+), 2 deletions(-)

commit 5d6dc694d95afb33114a820339acfeeab38cc42a
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:39:56 2025 -0500

    cambio de rama master a main en documentación

 2.branchs/README.md   | 16 ++++++++--------
 3.conflicts/README.md | 10 +++++-----
 README.md             |  7 +++++--
 3 files changed, 18 insertions(+), 15 deletions(-)

commit 3f74d4d0db34f6f6fbcd9f8cfa4b157dccdd48d7
Author: Franklin Jimenez <f.jimenezg@hotmail.com>
Date:   Mon Feb 17 23:17:02 2025 -0500

    primer commit

 .gitignore               |  2 ++
 1.commit/README.md       | 55 ++++++++++++++++++++++++++++++++++
 1.commit/sandwich.txt    |  4 +++
 2.branchs/README.md      | 78 ++++++++++++++++++++++++++++++++++++++++++++++++
 2.branchs/pizza.txt      |  3 ++
 3.conflicts/README.md    | 48 +++++++++++++++++++++++++++++
 3.conflicts/milanesa.txt |  2 ++
 README.md                | 54 +++++++++++++++++++++++++++++++++
 8 files changed, 246 insertions(+)
(END)


Aqui se puede ver los cambios hechos en el repositorio de manera detallada.








    
