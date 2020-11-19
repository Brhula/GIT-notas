# GIT-notes
Notas personales sobre la utilizacion de Git y GITHUB

**WORKSPACE:** directorio donde se esta trabajando en la maquina local   
**STAGING AREA:** Tambien conocido como INDEX. Lugar intermedio donde se almacenan los cambios que hacemos. Esta en local tambien.   
**LOCAL REPOSITORY:** Base de datos donde se almacenan todas las versiones (o "flases").   
**REMOTE REPOSITORY:** Base de datos en la nube (como GITHUB).   


Mejor utilizar GITBash 

"Index" es el antiguo nombre de la actual "staging area". En algunos comandos se utiliza --cached para indicar el "staging area".

Inicializar al instalar GIT en la computadora:   
```Bash
git config --global user.name "User name"   
git config --global user.email my_mail@server.com   

# Pone en "espera" al terminal cuando editamos los settings
git config --global core.editor "code --wait"   

# Editamos los settings "globales" de este usuario.
# Con el comando anterior, el terminal espera a que salgas del editor.
git config --global -e   

# Si estamos en Windows, que GIt elimine la combinacion de CR+LF y deje solo LF para compatibilidad.
# En linux/Mac el "true" debe ser "input" para que no filtre.
git config --global core.autocrlf true
```   

Para iniciar un nuevo repositorio, nos ponemos en el directorio que corresponda y ejecutamos:   
```bash
git init   
```   
open the editor:   
```bash
code   
```   
Incorporar ficheros al "staging area" (area intermedia antes de ir al repositorio)
```bash
git add file1.txt file2.txt # incorporar dos ficheros
git add *.txt               # incorporar todos los ficheros con esta extension
git add .                   # incorpora todo el directorio
```
comprobar el estado actual (directorio de trabajoi y staging area)
```bash
git status                  # listado largo con detalles
git status -s               # listado "short". imprime dos columnas por fichero 
                            # (izquierda: staging area, derecha directorio actual)
```   
Mostrar lo que hay en el "staging area":
```bash
git ls-files   
```   
Hacer "Commit" para crear un punto de control
```bash
git commit -m "mensaje explicativo" # Hace commit directamente
git commit                          # abre el editor para escribir un mensaje largo y uno corto
git commit -am "mensaje"            # Hace un commit sin pasar por el "staging area" (!)
```   

Mustra el estado de todos los "commits" en una sola linea:   
```bash
git log --oneline
```   
Mannipulacion de ficheros (para que GIT se entere)
```bash
git rm fichero.ext          # borra el "fichero.ext" del directorio y el staging area
git rm --cached fichero.ext # borra el fichero unicamente del "staging area"

git mv A.ext B.py           # Renombra el fichero
```   
