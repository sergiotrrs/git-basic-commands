# Instrucciones de Git

A continuación se describen algunas de las instrucciones más comunes de Git, desde el comienzo de un poryecto y con la implementación de una función:

1. `git init`: Este comando se utiliza para inicializar un nuevo repositorio Git en el directorio actual.

    ```bash
    git init
    ```

2. `git branch -M main`: Este comando se utiliza para renombrar la rama actual a "main".

    ```bash
    git branch -M main
    ```

3. `git status`: Este comando muestra el estado del repositorio Git, incluyendo los cambios que están en el área de preparación pero aún no han sido confirmados.

    ```bash
    git branch -M main
    ```

4. `git add .`: Este comando agrega todos los archivos y directorios del directorio actual al área de preparación de Git, preparándolos para el próximo commit.

    ```bash
    git add .
    ```

5. `git commit -m "feat: boilerplate"`: Este comando realiza un commit con todos los cambios que están en el área de preparación, utilizando "verbo: descripción" como mensaje del commit.

    ```bash
    git commit -m "feat: boilerplate"
    ```

6. `git branch newFeature`: Este comando crea una nueva rama llamada "newFeature".

    ```bash
    git branch newFeature
    ```

7. `git checkout newFeature`: Este comando cambia a la rama "newFeature".

    ```bash
    git checkout newFeature
    ```

8. `git add .` y `git commit -m "feat: lastname sorted"`: Estos comandos agregan todos los cambios al área de preparación y luego realizan un commit con el mensaje "verbo: descripción". Estos mismo comandos se repetirá por cada avance significativo que realices en tu proyecto.

    ```bash
    git add .
    git commit -m "feat: lastname sorted"
    ```

9. `git checkout main`: Este comando cambia de nuevo a la rama "main".

    ```bash
    git checkout main
    ```

10. `git merge newFeature`: Este comando fusiona los cambios de la rama "newFeature" en la rama actual (en este caso, "main").

    ```bash
    git merge newFeature
    ```
