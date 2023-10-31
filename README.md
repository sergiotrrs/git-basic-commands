# Instrucciones de Git

A continuación se describen algunas de las instrucciones más comunes de Git, desde el comienzo de un proyecto.

## Crear un repositorio local.

1. `git init`: Este comando se utiliza para inicializar un nuevo repositorio Git en el directorio actual.

    ```bash
    git init
    ```
<div style="text-align:center">
  <img src="./assets/img/img01.jpg" alt="crear archivos con touch" width="400px">
  <img src="./assets/img/img02.jpg" alt="git init" width="400px">
</div>

2. `git branch -M main`: Este comando se utiliza para renombrar la rama actual a "main".

    ```bash
    git branch -M main
    ```
<div style="text-align:center">
  <img src="./assets/img/img03.jpg" alt="cambiar nombre de rama" width="400px">
</div>

3. `git status`: Este comando muestra el estado del repositorio Git, incluyendo los cambios que están en el área de preparación pero aún no han sido confirmados.

    ```bash
    git status
    ```
<div style="text-align:center">
  <img src="./assets/img/img04.jpg" alt="saber el estado del repositorio" width="400px">
</div>

## Agregar archivos al repositorio.

4. `git add .`: Este comando agrega todos los archivos y directorios del directorio actual al área de preparación de Git, preparándolos para el próximo commit.

    ```bash
    git add .
    git status
    ```
<div style="text-align:center">
  <img src="./assets/img/img05.jpg" alt="agregar archivos y directorios" width="400px">
</div>

5. `git commit -m "add: empty html, css, and js files"`: Este comando realiza un commit con todos los cambios que están en el área de preparación, se recomiendo utilizar el formato "verbo: descripción" como mensaje del commit.

    ```bash
    git commit -m "add: empty html, css, and js files"
    ```
<div style="text-align:center">
  <img src="./assets/img/img06.jpg" alt="haciendo commit" width="400px">
</div>

6. `git log`: Este comando muestra información detallada sobre la historia de confirmaciones, incluyendo quién realizó cada confirmación, cuándo se hizo y un resumen de los cambios realizados.

    ```bash
    git log
    ```

<div style="text-align:center">
  <img src="./assets/img/img07.jpg" alt="mostrar el historial de commits" width="400px">
</div>

También puedes optar por usar con las sig. opciones:
- `git log --oneline`: Muestra cada confirmación en una sola línea con su identificador abreviado y el mensaje del commit.
Ver un gráfico de ramas:

- `git log --graph`: Muestra un gráfico ASCII que representa las relaciones entre las ramas y las confirmaciones.

<div style="text-align:center">
  <img src="./assets/img/img08.jpg" alt="uso de git log --oneline --graph" width="400px">
</div>

## Crear ramas.

7. `git branch newFeature`: Este comando crea una nueva rama llamada "newFeature".

    ```bash
    git branch basic-html
    ```
<div style="text-align:center">
  <img src="./assets/img/img09.jpg" alt="uso de git branch" width="400px">
</div>

8. `git checkout basic-html`: Este comando cambia a la rama "newFeature".

    ```bash
    git checkout basic-html
    ```
<div style="text-align:center">
  <img src="./assets/img/img10.jpg" alt="uso de git checkout" width="400px">
</div>

9. `git add .` y `git commit `: Estos comandos agregan todos los cambios al área de preparación y luego realizan un commit con el mensaje "verbo: descripción". Estos mismo comandos se repetirá por cada avance significativo que realices en tu proyecto.

    ```bash
    git add .
    git commit -m "feat: basic HTML structure tags"
    ```
- Creando la estructura básica del archivo html.
<div style="text-align:center">
  <img src="./assets/img/img11.jpg" alt="estructura html básica" width="400px">
</div>

- Verificando el estado del repositorio
<div style="text-align:center">
  <img src="./assets/img/img12.jpg" alt="verificar esto del repositorio" width="400px">
</div>

- `git diff`: ver las diferencias entre el área de trabajo y el área de preparación. Se puede incluir el nombre de un archivo en específico `git diff filename`.
<div style="text-align:center">
  <img src="./assets/img/img13.jpg" alt="diferencias del archivo" width="400px">
</div>

- `git add .`: agrega la modificación del archivo al área de preparación de Git (staging area).
<div style="text-align:center">
  <img src="./assets/img/img14.jpg" alt="prepar archivos" width="400px">
</div>

- `git commit -m "verbo: mensaje"`: realiza un commit con el cambio realizado.
<div style="text-align:center">
  <img src="./assets/img/img15.jpg" alt="realizar commit de los cambios" width="400px">
</div>

- `git status`: información sobre el estado actual del repositorio.
<div style="text-align:center">
  <img src="./assets/img/img16.jpg" alt="verificar los cambios" width="400px">
</div>

## Fusionar ramas.

10. `git checkout main`: Este comando cambia de nuevo a la rama "main".

    ```bash
    git checkout main
    ```

<div style="text-align:center">
  <img src="./assets/img/img17.jpg" alt="cambiar de rama" width="400px">
</div>

11. `git merge newFeature`: Este comando fusiona los cambios de la rama "newFeature" en la rama actual (en este caso, "main").

    ```bash
    git merge basic-html
    git status
    ```

<div style="text-align:center">
  <img src="./assets/img/img18.jpg" alt="fusionar ramas" width="400px">
</div>
<div style="text-align:center">
  <img src="./assets/img/img19.jpg" alt="verificar los cambios" width="400px">
</div>

## Agregar una dirección remota a un repositorio Git existente

12. Crear un respositorio nuevo en GitHub. 
Se recomienda tener configurada la llave pública para realizar la conexión con la dirección SSH. Si no tienes la configuración revisa la sección "Generar llave pública".

<div style="text-align:center">
  <img src="./assets/img/img20.jpg" alt="crear un reposotorio en github" width="400px">
</div>

- Copia la direcció SSH del nuevo repositorio.

<div style="text-align:center">
  <img src="./assets/img/img21.jpg" alt="repositorio creado" width="400px">
</div>

13. `git remote add <nombre_remoto> <URL_del_repositorio>`: Este comando agrega una nueva dirección remota a un repositorio Git existente. Puedes hacer la configuración desde cualquier rama.

- `<nombre_remoto>`: Esto es un nombre descriptivo que le das a la dirección remota. Por convención, "origin" es el nombre más comúnmente utilizado, pero puedes elegir cualquier nombre que tenga sentido para ti. El nombre se utiliza posteriormente para referirse a la dirección remota en otros comandos Git.

- `<URL_del_repositorio>`: Aquí debes proporcionar la URL del repositorio remoto al que deseas conectarte. La URL puede ser una dirección HTTP/HTTPS o una dirección SSH, dependiendo de cómo esté configurado el repositorio remoto.

    ```bash
    git remote add origin git@github.com:usergithub/cohorte-x-sesions.git
    ```

<div style="text-align:center">
  <img src="./assets/img/img22.jpg" alt="agregar repositorio remoto" width="400px">
</div>

- `git remote`: Se utiliza en Git para mostrar una lista de las direcciones remotas (remotes) configuradas en un repositorio Git junto con sus URL asociadas. 
- `git remote -v`: La opción -v o --verbose muestra información detallada sobre cada una de las direcciones remotas.

    ```bash
    git remote -v
    ```

<div style="text-align:center">
  <img src="./assets/img/img23.jpg" alt="mostrar los repositorios remotos configurados" width="400px">
</div>

## Subir cambios locales a GitHub.

11. `git push origin main`: Este comando se utiliza en Git para enviar (subir) tus cambios locales en la rama main de tu repositorio local al repositorio remoto (GitHub) denominado "origin".

    ```bash
    git push origin main
    ```

<div style="text-align:center">
  <img src="./assets/img/img24.jpg" alt="subir cambios al repositorio remoto" width="400px">
</div> 

- Si deseas subir otra rama tendrás que idicarla `git push origin basic-html`.

12. Verificar los cambios en GitHub en la rama main.

<div style="text-align:center">
  <img src="./assets/img/img25.jpg" alt="subir cambios al repositorio remoto" width="400px">
</div>

- Puedes trabajar en otra rama y hacer merge a tu rama main, posteriormente hacer de nueva `git push origin main`. Puedes hacer varios `commits` y al final un solo `git push`.