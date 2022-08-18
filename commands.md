# Comandos de Linux y su uso

En esta tabla se verán comandos que se usaron en el curso de Sistemas Operativos, existirán comandos de toda índole

| Comando | ¿Qué hace? | Notas | Ejemplo |
| :---: | :---: | :---: | :---: |
| &#124; | Este símbolo llamado pipe sirve para concatenar dos comandos  | Por si solo no es un comando | ps -aux &#124; grep "firefox" busca en la lista de procesos alguno llamado Firefox |
| `-l`  | Cambia la forma en que se imprimen ciertos comandos a ser una lista  | Por si solo no es un comando | `ls -l` muestra los directorios en forma de lista|
| `sudo`  | Este comando nos servirá para correr cualquier comando que necesite permisos de administrador como si lo fueramos  | | `sudo reboot` reinicia el sistema|
| `reboot`  | Reinicia el sistema operativo  | | El mismo ejemplo del comando anterior |
| `grep (patrón) (archivo o directorio)`  | Busca un patrón que definamos e imprime las líneas solicitadas  |  | `grep -r Log /home/` buscará el texto Log en home |
| `ps -aux`  | Muestra los procesos del usuario en cuestión  | &#124; grep (proceso a buscar) agregado al comando busca el proceso en cuestión  | Lo descrito en su descripción |
| `ps -e`  | Muestra los procesos del sistema operativo en su totalidad  |   | Lo descrito en su descripción |
| `man (cualquier comando)`  | Muestra el manual del comando especificado  |   | `man ps` muestra el manual de comandos de procesos |
| `top`  | Muestra los procesos como si se tratara del task manager  |   | Lo descrito en su descripción |
| `htop`  | Lo mismo que `top` pero de una manera más gráfica  | | Lo descrito en su descripción |
| `pstree`  | Muestra el árbol de procesos, es decir, la jerarquía  |  | Lo descrito en su descripción |
| `kill -9 (process id)`  | "Mata" un proceso del sistema  | Las ID de estos procesos pueden verificarse con `ps -aux` | `kill -9 2254` elimina un proceso con esa ID en el sistema |
| `ls` | Imprime las carpetas que tenemos, y las lista  | También podemos ver las de otro directorio con `/(nombre de la carpeta)` | `ls /snap` muestra todas las carpetas que existen dentro de snap |
| `pwd` | Muestra el directorio actual  | | Lo descrito en su descripción |
| `mkdir (nombre de la carpeta a crear)`  | Crea carpetas en el directorio actual  | Usar `pwd` para ver el directorio actual | `mkdir Test` creará la carpeta "Test" en el directorio que se encuentre en ese momento |
| `cd`  | Para cambiar de directorio | Con "Tab" podemos ver las opciones disponibles, si dejamos el comando sin argumentos nos llevará a la raíz | `cd Escritorio/` nos llevará a la carpeta de Escritorio |
| `cd ..`  | Nos devuelve al directorio anterior  | | Lo descrito en su descripción |
| `adduser (nombre del usuario)`  | Para crear un nuevo usuario, nos pedirá la contraseña e información, esto último podemos saltarlo | El nombre de usuario no debe ser todo en  mayúscula | `sudo add user test` creará un nuevo usuario llamado "test", seguidamente nos pedirá su contraseña |
| `passwd (usuario)`  | Para cambiar la contraseña de un usuario en cuestión  | Inclusive podemos cambiarle la contraseña a "root" que es el superadmin | `sudo passwd test` nos permitirá ingresar una nueva contraseña para el usuario "test" | 
| `userdel (usuario)`  | Elimina el usuario en cuestión  | | `sudo userdel test` nos permitirá eliminar el usuario "test" |
| `su (usuario)` | Para logearse como otro usuario dentro de la terminal  | Si le agregamos un sudo nos logeamos como super admin, no debemos poner un usuario, de este modo no tendremos que usar sudo para comandos con permisos | `su test` nos permitirá estar logeados como el usuario "test" dentro de la terminal |
| `whoami`  | Muestra quien es el usuario actual  | | Lo descrito en su descripción, esto puede funcionar mejor al usar el comando anterior |
| `exit`  | El equivalente a cerrar sesión en la terminal  | Debemos hacer esto cada vez que usamos otro usuario si queremos volver al original | Lo descrito en su descripción |
| `clear`  | Limpia la terminal | | Lo descrito en su descripción |
| `nano` | Para ver archivos de texto y editarlos  | Esto es un Notepad en la terminal, para seleccionar una opción, ver el menú de abajo y seleccionar una letra de este modo: Ctrl+Letra | Tenemos un archivo de texto llamado "Test.txt" en el directorio actual, con `nano Test.txt` podemos abrirlo y editarlo |
| `cat (nombre del archivo)` | Para SOLO ver el contenido de un archivo de texto  | | `cat Test.txt` nos muestra el contenido del archivo "Test.txt" si se encuentra en el mismo directorio |
| `echo`  | Imprime algo en la terminal | | `echo Hola Mundo` imprime "Hola Mundo" en la terminal |
| `sl`  | Un pequeño trolleo por si escribes mal ls  | | Lo descrito en su descripción |
| `cowsay`  | Hace que una vaca diga lo que se le escriba | Incluso se puede concatenar con pipe y hacer que muestre comandos enteros | `ps -aux (pipe) cowsay` muestra la lista de procesos en una vaca |
| `telnet towel.blinkenlights.nl `  | Muestra el episodio 4 de Star Wars completo  | Prepara las palomitas | Lo descrito en su descripción |
| `history`  | Muestra el historial de comandos  | | Lo descrito en su descripción |
| `> (nombre de un archivo de texto)`  | Esto guarda los resultados de un comando en un archivo de texto, se llama redirección  | Por si solo no es un comando | `history > Test.txt` guardará el historial de comandos en el archivo "Test.txt" |
| `head -n (n de líneas a ver) (archivo a ver)`  | Este comando sirve para ver las primeras líneas de un archivo de texto sin abrirlo del todo  | | `head -n 2 Test.txt` mostrará las primeras dos líneas de texto del archivo "Test.txt" |
| `tail -n (n de líneas a ver) (archivo a ver)`  | Este comando sirve para ver las últimas líneas de un archivo de texto sin abrirlo del todo  | | `tail -n 2 Test.txt` mostrará las últimas dos líneas de texto del archivo "Test.txt" |
| `more` | Concatenado con algún archivo nos permite verlo poco a poco  | Por si solo no es un comando, para salir de esta vista se presiona "q" | cat Test.txt &#124; more nos permitirá ver el archivo "Text.txt" poco a poco |
| `cp (archivo a copiar) (donde queremos copiarlo)`  | Para copiar un archivo a otra carpeta | | `cp -r /etc/[abcdef]* $HOME` copiará recursivamente todos los archivos con un nombre iniciado en a,b,c,d,e,f desde /etc hacia el directorio home |
| `mv (archivo a copiar) (donde queremos copiarlo)`  | Para mover un archivo a otra carpeta  | Si existe un archivo igual en la carpeta destino lo sobrescribirá | `mv Test.txt Escritorio/` moverá el archivo Test.txt al escritorio |
| `rm (archivo a borrar)` | Para borrar archivos  | Agregar -R al final si se trata de un directorio, se puede agregar una f al lado para forzar su eliminación | `rm Test.txt` borrará el archivo "Test.txt" si está en el mismo directorio |
| `dpkg -i (instalador.deb) `  | Para instalar un programa descargado por fuera de los repositorios y la tienda de aplicaciones | | Lo descrito en su descripción |
| `alias (alias del comando)="(comando a usar)" `  | Para añadirle un alias a un comando  | Cuando hagamos esto podremos usar solo el alias para correr el comando | `alias restart="sudo reboot" ` nos permitirá añadir el alias "restart" al comando "reboot" y así usarlo sin tener que escribirlo como normalmente se haría |
| `ip addr ` | Para verificar la IP de la sesión actual | Esta cambia cada sesión, por lo que en aplicaciones como "Termius" debemos cambiarla periodicamente |  Al ingresar `ip addr` se mostrará una lista de direcciones, la más importante será la llamada "inet" |
| `chmod (números de permisos en octal) (archivo a cambiar)` | Para cambiar los permisos de un archivo en específico | Usaremos una tabla especial con números en Octal para cambiar cada permiso, también podemos usar por separado comandos para cambiar la ejecución, lectura y escritura, estos siendo `chmod +x` `chmod +r` y `chmod +w` respectivamente, o todos al mismo tiempo | `chmod 706 Test.txt` cambiará los permisos para el archivo "Text.txt" |
| `du -h (archivo)` | Para verificar el tamaño de un archivo | -h sirve para hacerlo "human readable", es decir, haciendo que muestre la medida del tamaño |  `du -h Test.txt` nos mostrará el tamaño del archivo "Test.txt" |
| `stat (archivo)` | Muestra información de un archivo | Entre esta información se incluye la fecha de creación, de modificación, de ingreso, entre otras |  `stat Test.txt` nos mostrará información del archivo "Test.txt" |
| `file (archivo) ` | Muestra el formato de un archivo |  |  `file Test.txt` nos mostrará el formato del archivo "Test.txt" |
| `chown (usuario a darle el archivo) (archivo)` | Para cambiar el dueño de un archivo |  |  `chown Usr2 Test.txt` hará que Usr2 sea el dueño del archivo "Test.txt" |
| `df -h ` | Muestra el espacio utilizado en disco, todos los discos duros |  | Lo descrito en su descripción |
| `for file in /proc/*/status ; do awk '/VmSwap(pipe)Name/{printf $2 " " $3}END{ print ""}' $file; done (pipe) sort -k 2 -n -r (pipe) less` | Nos dice cuanta memoria virtual gasta cada proceso en específico |  | Lo descrito en su descripción |
| `free -h ` | Muestra la memoria total, usada, libre, y además el tamaño del swap |  | Lo descrito en su descripción |
| `swapon` | Para activar el swap | `swapoff` desactiva el swap  | Lo descrito en su descripción |
| `cat /proc/sys/vm/swappiness` | Nos dice cuanto usa el sistema operativo de memoria swap, con cuanta frecuencia mueve programas al swap | Va de 0 a 100, si tenemos un 0 no pasa ningún archivo al swap, y si tenemos un 100 prácticamente pasa todo de memoria a swap. Esto se puede cambiar con el siguiente comando | Lo descrito en su descripción |
| `sudo sysctl vm.swappiness=(valor de swappines)` | Nos permite cambiar el valor del swappines |  | `sudo sysctl vm.swappiness=60` cambiará el valor de swappines a 60 |
| `sudo mkdir /mnt/ram_disk ` -> `sudo mount -t tmpfs -o size=1024m new_ram_disk /mnt/ram_disk` | Nos permite montar un RAM Disk, lo que hace es crear un disco duro como memoria RAM | Con `df -h` podemos ver si se creó correctamente  | Lo descrito en su descripción |
| `mount` | Para montar dispositivos en el sistema de archivos |   | El ejemplo de arriba muestra una parte |
| `Gparted` | Para administrar particiones |   | `sudo apt install gparted` para instalarlo |
| `gnome-disk-utility` | Muestra información sobre el disco |   | `sudo apt install gnome-disk-utility` para instalarlo |
| `pacman` | Gestor de paquetes de ArchLinux, nos permitirá instalar y gestionar paquetes |   | `sudo pacman -S yay` instala el repositorio AUR |
| `systemctl` | Es la herramienta principal para controlar el sistema y sus servicios  | Dependiendo de la orden que le demos, los servicios harán diferentes cosas | `sudo systemctl start (servicio)` sirve para iniciar un servicio,<br /> `sudo systemctl stop (servicio)` sirve para detener un servicio,<br /> `sudo systemctl restart (servicio)` sirve para reiniciar un servicio,<br /> `sudo systemctl enable (servicio)` sirve para iniciar un servicio en el arranque,<br /> `sudo systemctl disable (servicio)` sirve para revertir lo anterior,<br /> `sudo systemctl status (servicio)` sirve para ver el estado de un servicio |
| `uname -a` | Para mostrar el kernel que utiliza el sistema operativo |   | Lo descrito en su descripción |
| `useradd (parámetros)` | Para crear un nuevo usuario con sus respectivos directorios y funciones, cosa que lo hace distinto de adduser |   | `sudo useradd -m Test -G wheel -p 123` creará el usuario "Test" en el grupo wheel con la contraseña 123 |
| `touch (archivo)` | Para crear un archivo vacío |   | `sudo touch test` creará un archivo vacío llamado "test" en el directorio actual |
| `ln (ruta o nombre del archivo original) (ruta o nombre del enlace duro)` | Sirve para crear un enlace duro de un archivo o ruta |  | `ln /home/Test /home/Test2` creará un enlace duro de Test en Test2 |
| `ln -s (ruta o nombre del archivo original) (ruta o nombre del enlace duro)` | Sirve para crear un enlace suave de un archivo o ruta |  | `ln /home/Test /home/Test2` creará un enlace duro de Test en Test2 |
| `unlink (ruta del enlace)` | Sirve para eliminar un enlace duro o suave |  | `unlink /home/Test2` eliminará el enlace creado en Test2 |

# Scripts

Para crear scripts primeramente deberemos crear un archivo con la extensión `.sh` y agregar la siguiente línea de texto al puro inicio:
`#!/bin/bash`<br />
Luego de esto podremos ir agregando comandos por línea, y estos se ejecutarán en ese orden.<br />

Para ejecutar un script, deberemos usar el siguiente comando:<br />
`cat (archivo del script)`<br />

Para cambiar el crontab (que definirá la configuración de ejecución en el tiempo del script), deberemos ejecutar el siguiente comando:<br />
`crontab -e`<br />
Esto abrirá un archivo de texto donde deberemos ingresar la siguiente configuración:<br />
`m h dom mon dow command`<br />

##Donde:<br />
m: Minutos<br />
h: Hora<br />
dom: Día del mes<br />
mon: Mes<br />
dow: Día de la semana<br />
command: Comando o ruta del script a ejecutar

En caso de no requerir algún parámetro se puede dejar con un asterisco<br />

##Ejemplo de crontab:<br />
`00 19 * * * root echo Hola Mundo`<br />
Esto ejecutará como root el comando echo todos los días a las 7 de la tarde
