### 2.2. Ejercicio Práctico

    git graph                                                                                       

    * 83e7e48 (HEAD -> juan_cabrera, personal/juan_cabrera) Resuelto ejercicio 1
    * 0ce6864 Remover sandwich2_feo.txt
    * 496b03b Agrego sandwich2_feo.txt
    * 18d74f8 Agrego mi_nombre.txt
    * 01713ad Agrego salsas
    * 17d477e Agrego mi sandwich.txt
    * fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025,
    main) cambio readme.md
    * 5d6dc69 cambio de rama master a main en documentación
    * 3f74d4d primer commit

3. Verificar que se encuentra en la branch `experimento`. (Puede usar el comando `git branch`). 
    git branch                                                                                      
    * experimento
    juan_cabrera
    main
    practica2025    

4. Agregarle el condimento `albahaca` **arriba del queso** al archivo `2.branchs/pizza.txt` y "commitee" los cambios. 
    git commit -m "Agregar albahaca arriba de queso"                                               
    [experimento 5c376ca] Agregar albahaca arriba de queso
    1 file changed, 1 insertion(+)

5. Agregarle el condimento `oregano` **arriba de la albahaca** al archivo `2.branchs/pizza.txt` y "commitee" los cambios.
    git commit -m "Agregar oregano arriba de albahaca"                                             
    [experimento b68d78d] Agregar oregano arriba de albahaca
    1 file changed, 1 insertion(+)

6. Correr el comando `git graph` y observar el resultado. ¿Qué observa?
    Agregar oregano arriba de albahaca
    * 5c376ca Agregar albahaca arriba de queso
    | * 83e7e48 (personal/juan_cabrera, juan_cabrera) Resuelto ejercicio 1
    | * 0ce6864 Remover sandwich2_feo.txt
    | * 496b03b Agrego sandwich2_feo.txt
    | * 18d74f8 Agrego mi_nombre.txt
    | * 01713ad Agrego salsas
    | * 17d477e Agrego mi sandwich.txt
    |/
    * fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025,
    main) cambio readme.md
    * 5d6dc69 cambio de rama master a main en documentación
    * 3f74d4d primer commit
    Según la salida me muestra en la parte de arriba los commits de las ramas más recientes, las difirentes ramas con sus respectivos commites y la union de de ramas.

10. Correr el comando `git graph` y observar el resultado. ¿Qué observa?
    Agegar anana arriba de queso
    | * b68d78d (experimento) Agregar oregano arriba de albahaca
    | * 5c376ca Agregar albahaca arriba de queso
    |/
    | * 83e7e48 (personal/juan_cabrera, juan_cabrera) Resuelto ejercicio 1
    | * 0ce6864 Remover sandwich2_feo.txt
    | * 496b03b Agrego sandwich2_feo.txt
    | * 18d74f8 Agrego mi_nombre.txt
    | * 01713ad Agrego salsas
    | * 17d477e Agrego mi sandwich.txt
    |/
    * fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025,
    main) cambio readme.md
    * 5d6dc69 cambio de rama master a main en documentación
    * 3f74d4d primer commit
    En la salida se puede observar la nueva rama anana con su respectivo commit

13. Correr el comando `git graph` y observar el resultado. ¿Qué observa?
    Agegar cebolla debajo de salsa de tomate
    | * a9b2612 (anana) Agegar anana arriba de queso
    |/
    | * b68d78d (experimento) Agregar oregano arriba de albahaca
    | * 5c376ca Agregar albahaca arriba de queso
    |/
    | * 83e7e48 (personal/juan_cabrera, juan_cabrera) Resuelto ejercicio 1
    | * 0ce6864 Remover sandwich2_feo.txt
    | * 496b03b Agrego sandwich2_feo.txt
    | * 18d74f8 Agrego mi_nombre.txt
    | * 01713ad Agrego salsas
    | * 17d477e Agrego mi sandwich.txt
    |/
    * fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025) cambio
    readme.md
    * 5d6dc69 cambio de rama master a main en documentación
    * 3f74d4d primer commit
    Se puede observar como en la rama main se ha creado un nuevo commit

15. Correr el comando `git graph` y observar el resultado. ¿Qué observa?
    Merge branch 'anana'
    |\
    | * a9b2612 (anana) Agegar anana arriba de queso
    * | ace944c Agegar cebolla debajo de salsa de tomate
    |/
    | * b68d78d (experimento) Agregar oregano arriba de albahaca
    | * 5c376ca Agregar albahaca arriba de queso
    |/
    | * 83e7e48 (personal/juan_cabrera, juan_cabrera) Resuelto ejercicio 1
    | * 0ce6864 Remover sandwich2_feo.txt
    | * 496b03b Agrego sandwich2_feo.txt
    | * 18d74f8 Agrego mi_nombre.txt
    | * 01713ad Agrego salsas
    | * 17d477e Agrego mi sandwich.txt
    |/
    * fafdc7f (origin/practica2025, origin/main, origin/HEAD, practica2025) cambio
    readme.md
    * 5d6dc69 cambio de rama master a main en documentación
    * 3f74d4d primer commit
    Se observa en la parte superior como main ha hecho un merge con anana

16. ¿Qué branches están "mergeadas" a main? (Puede usar el comando `git branch --merged`).
    git branch --merged                                                                              

    anana
    * main
    practica2025

