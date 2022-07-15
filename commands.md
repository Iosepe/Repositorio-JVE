# Comandos de Linux y su uso

En esta tabla se verán comandos que se usaron en el curso de Sistemas Operativos, existirán comandos de toda índole

| Comando | ¿Qué hace? | Notas | Ejemplo |
| :---: | :---: | :---: |
| `Pipe`  | Este símbolo llamado pipe sirve para concatenar dos comandos  | Por si solo no es un comando, este símbolo no se puede usar en GitHub ||
| `-l`  | Cambia la forma en que se imprimen ciertos comandos a ser una lista  | Por si solo no es un comando ||
| `sudo`  | Este comando nos servirá para correr cualquier comando que necesite permisos de administrador como si lo fueramos  | Ej: `sudo reboot` ||
| `reboot`  | Reinicia el sistema operativo  | ||
| `ps -aux`  | Muestra los procesos del usuario en cuestión  | `Pipe grep (proceso a buscar)` agregado al comando busca el proceso en cuestión  ||
| `ps -e`  | Muestra los procesos del sistema operativo en su totalidad  |   ||
| `man (cualquier comando)`  | Muestra el manual del comando especificado  |   ||
| `top`  | Muestra los procesos como si se tratara del task manager  |   ||
| `htop`  | Lo mismo que `top` pero de una manera más gráfica  | |
| `pstree`  | Muestra el árbol de procesos, es decir, la jerarquía  |  ||
| `kill -9 (process id)`  | "Mata" un proceso, las ID de estos pueden verificarse con `ps -aux`  |  ||
| `htop`  | Lo mismo que `top` pero de una manera más gráfica  | ||
| `ls`  | Imprime las carpetas que tenemos, las listas  | También podemos ver las de otro directorio con `/(nombre de la carpeta)` ||
| `pwd`  | Muestra el directorio actual  | ||
| `mkdir (nombre de la carpeta a crear)`  | Crea carpetas en el directorio actual  | Usar `pwd` para ver el directorio actual ||
| `cd`  | Para cambiar de directorio  | Con "Tab" podemos ver las opciones disponibles, si dejamos el comando sin argumentos nos llevará a la raíz ||
| `cd ..`  | Nos devuelve al directorio anterior  | ||
| `adduser (nombre del usuario)`  | Para crear un nuevo usuario, nos pedirá la contraseña e información, esto último podemos saltarlo | El nombre de usuario no debe ser todo en  mayúscula ||
| `passwd (usuario)`  | Para cambiar la contraseña de un usuario en cuestión  | Inclusive podemos cambiarle la contraseña a "root" que es el superadmin |
| `userdel (usuario)`  | Elimina el usuario en cuestión  | ||
| `su (usuario)`  | Para logearse como otro usuario dentro de la terminal  | Si le agregamos un sudo nos logeamos como super admin, no debemos poner un usuario, de este modo no tendremos que usar sudo para comandos con permisos ||
| `whoami`  | Muestra quien es el usuario actual  | ||
| `exit`  | El equivalente a cerrar sesión en la terminal  | Debemos hacer esto cada vez que usamos otro usuario si queremos volver al original |
| `clear`  | Limpia la pantalla  | ||
| `cd` -> `nano` | Para ver archivos de texto y editarlos  | Esto es un Notepad en la terminal, para seleccionar una opción ver el menú de abajo y seleccionar una letra de este modo: Ctrl+Letra ||
| `cat (nombre del archivo)` | Para SOLO ver el contenido de un archivo de texto  | ||
| `sl`  | Un pequeño trolleo por si escribes mal ls  | ||
| `cowsay`  | Hace que una vaca diga lo que se le escriba | Incluso se puede concatenar con Pipe y hacer que muestre comandos enteros ||
| `telnet towel.blinkenlights.nl `  | Muestra el episodio 4 de Star Wars completo  | Prepara las palomitas ||
| `history`  | Muestra el historial de comandos  | ||
| `> (nombre de un archivo de texto)`  | Esto guarda los resultados de un comando en un archivo de texto  | Por si solo no es un comando ||
| `head -n (n de líneas a ver) (archivo a ver)`  | Este comando sirve para ver las primeras líneas de un archivo de texto sin abrirlo del todo  | ||
| `tail -n (n de líneas a ver) (archivo a ver)`  | Este comando sirve para ver las últimas líneas de un archivo de texto sin abrirlo del todo  | ||
| `more`  | Concatenado con algún archivo nos permite verlo poco a poco  | Por si solo no es un comando, para salir de esta vista se presiona "q" ||
| `cp (archivo a copiar) (donde queremos copiarlo)`  | Para copiar un archivo a otra carpeta  | ||
| `mv (archivo a copiar) (donde queremos copiarlo)`  | Para mover un archivo a otra carpeta  | Si existe un archivo igual en la carpeta destino lo sobrescribirá ||
| `rm (archivo a borrar)` | Para borrar archivos  | Agregar -R al final si se trata de un directorio, se puede agregar una f al lado para forzar su eliminación ||
| `dpkg -i (instalador.deb) `  | Para instalar un programa descargado  | ||
| `alias (alias del comando)="(comando a usar)" `  | Para añadirle un alias a un comando  | Cuando hagamos esto podremos usar solo el alias para correr el comando ||

