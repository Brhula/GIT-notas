# GIT-notes
Notas personales sobre la utilizacion de Git y GITHUB

Mejor utilizar GITBash 

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

open the editor:   
```bash
code   
```   


