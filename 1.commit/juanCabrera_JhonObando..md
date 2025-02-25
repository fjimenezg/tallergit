Nombre_estudiante: Juan Sebastián Cabrera Bolaños

### 1.1. Preguntas

    1. ¿Cómo se inicializa un repositorio local? (que comando se debe ejecutar?)
        Un repositorio local de git se inicializa con el comando git init

    2. ¿Cómo hago para que un directorio deje de ser controlado por git? (que comando se debe ejecutar?)
    Para que un directorio deje de ser controlado por git se debe eliminar la carpeta .git del directorio controlado por git. Para ver la carpeta .git en la terminal de linux agregamos estando en el directorio de trabajo ls -a y para eliminarlo agregamos rm -r .git

    3. Si agrego un archivo a un directorio que ya está siendo controlado por git, ¿está siendo controlado por git?
    SI, ya que al agregar un archivo al directorio controlado por git este, a pesar de que no se enuentra rastreado por git este sabe que el    archivo existe y que no se encuentra en la staging area.

    4. ¿qué comando se utiliza para agregar un archivo al repositorio local?
    git add nombre_archivo

    5. ¿Cómo determino que archivos fueron modificados? (que comando se debe ejecutar?)
        git status

    6. ¿Qué comando se utiliza para hacer un commit?
        git commit -m "mensaje"

    7. En sus propias palabras, ¿qué es un commit?
        Un commit es una version de una rama en un punto de tiempo


### 1.2. Ejercicio Práctico

    3. Antes de realizar cualquier acción con git, guarde el estado actual del directorio en el archivo `nombre_apellido.txt`. Para esto, se debe ejecutar el comando `git status` y copiar el resultado en el archivo `nombre_apellido.txt`. Explique que significa la salida del comando.
        git status juan_sebastian_cabrera.txt                                                        
        En la rama juan_cabrera
        Archivos sin seguimiento:
        (usa "git add <archivo>..." para incluirlo a lo que será confirmado)
            juan_sebastian_cabrera.txt

        no hay nada agregado al commit pero hay archivos sin seguimiento presentes (usa "git add" para hacerles seguimiento)
        R// Según la salida nos indica que nos encontramos en la rama juan_cabrera y que el archivo juan_sebastian_cabrera.txt no se encuentra en seguimiento, lo que significa que no esta siendo rastreado por git y por ende no se encuentra en la staging area. Finalmente el porpio gut recomienda incluir el archivo al staging area con el comando git add <archivo>, donde <archivo> es el nombre del archivo que queremos agregar.
    
    5. Explique que cambio en la salida del comando `git status` luego de ejecutar el comando `git add sandwich.txt`.
        En la salida se muestra que el archivo sandwich.txt ya se encuentra en la staging area y nos indica que también podemos removerlo de ahi con el comando restore --staged <archivo>, pero el archivo juan_sebastian_cabrera.txt sigue sin seguimiento y tiene la misma salida del punto 3.
    
    7. Explique que cambio en la salida del comando `git status` luego de ejecutar el comando `git commit -m "Agrego mi sandwich.txt"`.
        El comando git status dice que se puede hacer un commit en el archivo nombre_apellido.txt. Y si el directorio esta limpio, significa que en la rama no se puede hacer un commit.

    9. Escriba la salida del comando `git log` en el archivo `sandwich.txt`. Y explique que significa. ¿En qué orden aparecen los commits?
        git log sandwich.txt                                                                              
        commit 01713ad8d8cb70789780791a92bdd4cca4684698
        Author: Juan Sebastián Cabrera Bolaños <juansabas2021@udenar.edu.co>
        Date:   Mon Feb 24 17:30:22 2025 -0500

            Agrego salsas

        commit 17d477e436afe0d6c1bec2bc918f5ddf701821c4
        Author: Juan Sebastián Cabrera Bolaños <juansabas2021@udenar.edu.co>
        Date:   Mon Feb 24 17:26:31 2025 -0500

            Agrego mi sandwich.txt

        commit 3f74d4d0db34f6f6fbcd9f8cfa4b157dccdd48d7
        Author: Franklin Jimenez <f.jimenezg@hotmail.com>
        Date:   Mon Feb 17 23:17:02 2025 -0500

            primer commit
        R//El orden en que aparecen los commits son desde el último commit hecho hasta el primer commit.

    10. Pruebe las variaciones del comando `git log` y explique que observa en cada una de ellas.
    10.1. `git log --oneline`
        Este comando muestra una versión simplificada del historial de commits, donde cada commit se representa en una sola línea.
    10.2. `git log --stat`
        Este comando muestra el historial de commits junto con estadísticas de los archivos modificados en cada commit.

    11. Inspeccione diferencias entre los commits, use el comando git diff <hash> <hash> y explique que significa cada uno de los resultados.
        Para el desarrollo del ejemplo se usara los commits del archivo sandwich.txt. Primeramente miramos los hash de los diferentes commits
            git log --oneline                                                                               
            18d74f8 (HEAD -> juan_cabrera) Agrego mi_nombre.txt
            01713ad Agrego salsas
            17d477e Agrego mi sandwich.txt
            fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025, ma
            in) cambio readme.md
            5d6dc69 cambio de rama master a main en documentación
            3f74d4d primer commit
        Después comparamos:
            git diff 01713ad 17d477e                                                                       
            diff --git a/1.commit/sandwich.txt b/1.commit/sandwich.txt
            index 2d580d4..87d8a4d 100644
            --- a/1.commit/sandwich.txt
            +++ b/1.commit/sandwich.txt
            @@ -4,6 +4,4 @@ medallón
            pan
            mortadela
            atún
            -lechuga
            -salsa de tomate
            -salsa rosada
            \ No newline at end of file
            +lechuga
            \ No newline at end of file
        Según la salida nos dice que lechuga, salsa de tomatey salsa de tomate rosada fueron añadidas y que medallón pan,  mortadela, atún no cambiaron

   11.1. En Windows, pruebe `git difftool --tool=meld <hash>`
        En una herramienta que nos ayuda ver las diferencias entre commits de forma visual
    
    11.2. En Linux, pruebe `git difftool --tool=opendiff <hash>`
        Desafortunadamente laopendiff no es una herramienta nativa
    
    14. Renombrar el archivo `sandwich2.txt` a `sandwich2_feo.txt`. Para esto, se debe ejecutar el comando `git mv sandwich2.txt sandwich2_feo.txt`. Explique que cambio en la salida del comando `git status` luego de hacer un commit con esos cambios y de `git log --oneline`.
        * Al realizar este comando `git mv sandwich2.txt sandwich2_feo.txt`, no sucedio nada relevante, solo cambio el nombre del archivo
    
    15. Borre el archivo `sandwich2_feo.txt`. Para esto, se debe ejecutar el comando `git rm sandwich2_feo.txt`. Explique que cambio en la salida del comando `git status` luego de hacer un commit con esos cambios y de `git log --oneline`.
        Parecido al punto 14, en git status no ocurre nada, el arbol de trabajo esta limpi y con git log --oneline tampoco ouccure nada
    
    16. Inspeccione la bitácora usando `git log --stat` y explique lo que ve.
        Se observa mas información de los commits, como la fecha, el número de lineas agregadas, el número de archivos cambiados, el autor y el hash del commit.
