# Trabajando con Git

Git es un software de control de versiones diseñado por Linus Torvalds, pensando en la eficiencia, la confiabilidad y compatibilidad del mantenimiento de versiones de aplicaciones cuando estas tienen un gran número de archivos de código fuente. Su propósito es llevar registro de los cambios en archivos de computadora incluyendo coordinar el trabajo que varias personas realizan sobre archivos compartidos en un repositorio de código. Más información, [aquí](https://es.wikipedia.org/wiki/Git).

## Comandos básicos

- **`git init`**: Inicializa tu carpeta como un repositorio. Esto lo hace al crear una carpeta denominada `.git`, en donde se coloca el esqueleto del repositorio de Git. Al realizar este comando, git todavía no le está dando seguimiento a ninguna carpeta o archivo dentro del repositorio.

- **`git fetch`**: Descarga los cambios realizados en el repositorio remoto.

- **`git merge <nombre_rama>`**: Impacta en la rama en la que te encuentras parado, los cambios realizados en la rama “nombre_rama”.

    * Ejemplo: Estando situado en una rama llamada `master`. Ejecutar `git merge develop` mezclaría los cambios en la rama `develop`, hacia la rama `master`.

- **`git pull`**: Unifica los comandos fetch y merge en un único comando.

    * Ejemplo: Estando situado en una rama llamada `master`. Al ejecutar el comando `git pull`, sería la abreviatura de ejecutar el comando `git pull origin master`. Lo que haría git es hacer `git fetch` y luego hacer un `git merge origin/master`. 

- **`git commit -m "<mensaje>"`**: Confirma los cambios realizados. El “mensaje” generalmente se usa para asociar al commit una *breve* descripción de los cambios realizados.

- **`git push origin <nombre_rama>`**: Sube la rama “nombre_rama” al servidor remoto. La palabra `origin` se refiere al servidor remoto de git, ese nombre puede cambiar, pero por defecto se le denomina `origin`.

- **`git status`**: Muestra el estado actual de la rama, como los cambios que hay sin commitear.

- **`git add <nombre_archivo>`**: Comienza a darle seguimiento el archivo "nombre_archivo". También es común usar este comando de esta manera: `git add .`, que lo que haría sería agregar todos los cambios en la carpeta en la que estés situado al *STAGE*. Normalmente este comando se ejecuta desde la carpeta raíz del repositorio, pero puede hacerse desde cualquier carpeta hija.

- **`git checkout -b <nombre_rama_nueva>`**: Crea una rama a partir de la que te encuentres parado con el nombre “nombre_rama_nueva”, y luego salta sobre la rama nueva, por lo que quedas parado en esta última.
    * Ejemplo: Estando situado en una rama llamada `master`, al ejecutar el comando `git checkout -b develop`, generará una *nueva* rama llamada `deve

- **`git checkout -t origin/<nombre_rama>:`**: Si existe una rama remota de nombre “nombre_rama”, al ejecutar este comando se crea una rama local con el nombre “nombre_rama” para hacer un seguimiento de la rama remota con el mismo nombre.
