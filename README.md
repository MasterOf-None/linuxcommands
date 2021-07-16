# \*NIX Commands

Actualmente, mientras aprendo sobre algunas tecnologías trato de compartir mi aprendizaje en forma de apuntes, si puedes considerar comprarme un cafecito. Muchas Gracias!

<button>
<a href="https://ko-fi.com/m4ster_0fnone">
<img src="https://camo.githubusercontent.com/88b9e664b2a500cbdc892ab041e3fd1d7c348082650f3e5cf38da8ce3865e922/68747470733a2f2f7777772e6b6f2d66692e636f6d2f696d672f676974687562627574746f6e5f736d2e737667" alt="ko-fi" data-canonical-src="https://www.ko-fi.com/img/githubbutton_sm.svg" style="max-width:100%;">
</a>
</button>
	
# Commands Terminal

- `"backspace"command`: Ejecuta el comando indicado sin guardarlo en el historial.
- `--help ó -h`: La mayoría de los comandos acepta este flag y meciona la descripción del comando.
- `info [command]`: Muestra la descripción del comando.
- `man [command] {“man man: Mostrará una guía de cómo están estructurados los manuales”}`: Manual. Muestra la descripción completa del comando.
- `apropos [keyword]`: Es un comando que sirve para buscar ayuda en el manual de la palabra clave, que se le pase como parámetro.
- `uname ["-a": All]`: Que version del sistema operativo y del kernel tiene el equipo.
- `cd [(“.”: Directorio actual), (“..”: Directorio Padre), (“-": Regresa al directorio donde se estuvo antes de ir a ese directorio usando cd), (“cd": cd sin argumentos nos envía a Home) path]`: Change Directory. Cambiar Directorio.
- `chdir [destiny]`: Change Directory. Se utilliza al igual que `cd` para moverse a otro directorio.
- `pushd [directory]`: Guarda la ubicación del directorio pasado como parámetro en una pila y luego pasa a dicho directorio.
- `popd`: Se utiliza para volver al último directorio almacenado en la pila.
- `ls (“-a": All) [(“-l": Long, Muestra mayor información acerca de los archivos) ("-h": En formato humano, va de la mano con la opción "-l")] (“-t": Time, ordena los archivos por fecha de modificación de forma descendente) ("-S": Sort, ordena los archivos por tamaño en orden descendente) (“-1": Muestra la lista de archivos en una sola columna) ("-d": Muestra solo los directorios) ("--group-directories-first": Lista primero los directorios) [path]`: List. Cuando un nombre de un directorio a listar contenga espacios, la forma rápida de escribir su nombre es poniendo entre comillas. ls “Nombre Con Espacios” ó con "\ ".
- `ll`: Long List. Listado Largo es un alias del comando “ls -l”.
- `dir`: Es similar a “ls”.
- `cp ("-a": Dicha opción representa la suma de tres opciones, donde se copia de forma recursiva, descartando los enlaces simbólicos, y conservando las propiedases de los archivos tales como: fecha de modificacnión, fecha de acceso, flgas, User ID, Group ID, ) ("-n": Numera las líneas del archivo) [path] (new_name)`: Copy. Copiar.
- `rsync ("-av": Donde "a" habilita el modo archivo y "v" viene de verbose) ("-a" ó "--archive": Es una forma rápida de indicar que se desea recursión y que se desea preservar casi todo, aunque no se copian los hardlinks) ("--chown=[user:group]": Copia los archivos conservadando el propietario al que pertenecían) [{username@host:}src] [path_destiny]`: Transfiere y sincroniza archivos de forma eficiente, entre una máquina local, un servidor remoto o cualquiera de estos. La difrencia con "cp" es que esta utilidad copia de forma inteligente, es decir, si el archivo previamente ya se copio ya no se volverá copiar, pero si algún archivo de la copia aún falta solo procederá a copiar este. Esto resulta útil cuando la copia se llegó a interrumpir por alguna razón.
- `mv ( “-r”: Mueve de manera recursiva los archivos que están dentro de un directorio) [path]`: Move. Mover. Sirve para mover un archivo/carpeta de un sitio a otro o renombrarlo si por defecto no se le da otra ruta diferente, en tal caso sí esa no es la opción deseada conviene mejor usar “cp”.
- `touch [file_name]`: Sirve para editar las fechas de modificación y de un archivo o carpeta, esto es más seguro porque cambia la fecha de modificación sin tener que modificar el contenido, útil para comprobar permisos de escritura sobre dicho archivo. Pero también permite creación de archivos.
- `mkdir ["-p": Permite crear subdirectorio dentro de un directorio.] [directory_name]`: Make Directory, permite la creación de un directorio.
- `mktemp ("-d": Directory. Crea un directorio temporal) ("Template": Formato a partir del cual proporciona una base ó patrón, para nombrar ese archivo o carpeta)`: Permite la creación de un archivo ó directorio temporal.
- `ln (-s: Crear enlace simbólico) [file_origin: Archivo fuente del cual, al cúal se creará el vículo] [path_link]`: Make links. Permite realizar enlaces soft y enlaces hard.
- `rm [( “-r”: Borra de manera recursiva los archivos que están dentro de un directorio), (“f” forza el borrado)] [file]`: Sirve para eliminar un archivo o carpeta.
- `rmdir [folder]`: Elimina una carpeta, pero debe estar vacía.
- `cat ("-n": Muestra el número correspondiente en cada línea) [file]`: Concatenate. Visualiza el contenido de un archivo.
- `less [file]`: Less al igual que "more" es un pager, que permite mayor flexibilidad de visualización de un archivo, paginando la información, pero permitiendo la visualización de este línea por línea mientras se baja el cursor ó con la teclas de "Down arrow, Pg Up/Up arrow, Pg Down" y de la misma forma haciendo scroll hacia arriba. Se baja una página con la tecla "Backspace". Con la tecla "/" se puede realizar una búsqueda. Con la tecla "N" permite ir viendo a tráves de las coincidencias que se ncontrarón. Y con las teclas "Shift N", para retroceder a través de las palabras encontradas. Y para salir con la tecla "Q".
- `more [file]`: Permite la visualización de un archivo, paginando la información, pero mostrando lo que quepa en la pantalla, es decir por bloques, y no permite volver el texto de arriba, así mismo al llegar al final del documento la ejecución del comando termina.
\-\- Notice: Cuando la salida de este comando no se muestra completamente en la terminal, ya sea porque esta se encuentra minimizada ó porque la data es muy extensa al presionar la tecla `v` y luego `Shift:Command` permite abrir desde aquí una shell interactiva (pwning shell).
- `head [file]`: Muestra las primeras líneas de un archivo. Por defecto son las primeras 10 líneas.
- `tail (“-n15 number: Cuántas líneas se quiere mostrar, por ejemplo: 15) (“-f": Follow. Mantiene el archivo abierto, útil cuando se actualiza constantemente”) [-file]`: Muestra las últimas líneas de un archivo. Por defecto son las últimas 10 líneas.
- `tty`: Ver la terminal virtual a la que se encuentra conectado en ese momento el usuario.
- `env`: Muestra las variables de entorno. También permite ejecutar un programa con variables de entorno modificadas.
- `printenv`: Muestra las variables de entorno. A diferencia de "env", este comando puede solicitar el valor de variables individuales, por ejemplo: "printenv TERM".
- `set`: Muestra una lista de todas las variables Shell, de entorno, locales y funciones del shell.
- `export`: Permite crear y modificar variables de entorno, para que los procesos hijo de un programa puedan acceder a él, por ejemplo: "export PATH=$PATH:[new_route]", es importante resaltar el orden en que se define PATH, ya que el sistema operativo consulta las rutas de izquierda a derecha y una vez encontrado el binario, el sistema deja de buscar en el resto de rutas, lo que se podría generar un conflicto cuando exista una situación donde un programa tenga un binario tenga más de una ruta, pero cada ruta tenga una versión diferente de dicho binario.
- `source ["~/.zshrc": Path]`: Volver a leer las configuraciones de cierto archivo.
- `pwd`: Print Working Directory. Muestra la ruta donde se encuentra actualmente.
- `w`: Muestra los usuarios que se encuentran logueados al sistema, respecto al comando "who", muestra más información.
- `who`: Muestra la lista de usuarios que están conectados en ese momento.
- `finger`: Muestra la información de un usuario.
- `id`: Muestra los ID que tenga el usuario actual, como: UID, GID y GID de los grupos a los cuales pertenece.
- `groups`: Muestra en qué grupos se encuentra el usuario.
- `whoami`: Muestra el nombre (login) del usuario.
- `users`: Muestra la lista de usuarios que están conectados.
- `hostname`: Nombre del equipo dentro de una red.
- `whatis [keyboard]`: Busca y muestra la descripción del parámetro que se le haya pasado.
- `which ("-a": Lista todas las ubicaciones) [keyword]`: Localiza uan aplicación a partir del $PATH del usuario.
- `whereis [keybword]`: Localiza una aplicación verificando los directorios `bin` estándar.
- `locate [keyboard]`: Busca la ubicación de un archivo asociado con la palabra clave, a diferencia del comando “whereis” muestra más información. Y a su vez hace uso del comando 'updatedb' para realizar lás búsquedas, sin embargo si el archivo se creó despues de que "updatedb" se ejecutó dicho archivo no se va a encontrar en la búsqueda de "locate".
- `sudo updatedb`: Actualiza la base de datos en la cual busca el comando “locate”. esta actualización se lleva a cabo automáticamente a por la noche.
- `find [path] ("-mtime {number}": Modified Time. Busca en base a la fecha de moficación del archivo {number}) (“-iname: Indica el nombre del archivo, donde i es insensitive a mayúsculas ó minúsculas”) [file: Debe ir entre comillas simples] ("-type f": Tipo de archivo es file) ("-printf %f\t\%p\t%u\t%g\t%mn": Imprime el nombre del archivo donde f:archivos, p:ruta, u:usuario, g:grupo, y m:modo) ("-exec [command]": Ejecuta un comando, por ejemplo "grep")`: Busca un archivo dentro del equipo asociado a ese nombre.
- `file [file]`: Muestra que tipo de archivo es, él que se le ha pasado como parámetro.
- `test [ expression ]`: Permite ejecutar una serie de pruebas sobre archivos, strings, valores númericos y entorno de usuario. Retorna "0" cuando el valor es positivo y diferente de cero, en caso contrario, por ejemplo: `test [[ -f /etc/passwd ]]` devuelve "0", si "passwd" es un archivo, esto se puede comprobar con: `echo $?`.
- `grep ó egrep (“-i”: Ignora las distinciones entre mayúsculas y minúsculas, tanto en el patrón como en la entrada de archivos) (“-r”: Búsqueda de manera recursiva) (“-n:” Muestra la línea donde se encuentra la coincidencia) ("-v": Busca todo lo que no sea el patrón le ha indicado) [regular_expression:” Lo que se desea buscar debe ir entre comillas] [“.”: A partir de donde iniciará la búsqueda. En este caso el punto significa que iniciará desde el directorio actual]`: Permite la búsqueda de palabras o algún patrón en archivos.
- `sed [pattern] (file)`: Stream Editor. Permite buscar, sustituir, insertar, eliminar texto dentro de un archivo, mediante el uso de expresiones regulares. Se puede aplicar al STDIN, por ejemplo: `echo "Hello world" | sed 's/world/frienmd/'`.
- `cat /etc/passwd | awk 'BEGIN {print "Archivo Passwd"} {print "User Id"$3, $5 $NF; count++} END {print "Total users: " count}'` Donde "N" hace referencia a la variable que indica la N columna del "stdout" (archivo passwd), mientras es una variable que "NF" hace referencia al último elemento. Cuando no se especifíca el limitador para el stdout es el espacio ó tabulador. Sin embargo la opción "-F':'" establece el un limitador con ":". Y a su vez el contenido de "print" se puede concatenar ó realizar operaciones aritméticas, mientras que ";" se utiliza para separar sentencias como en Bash. "BEGIN" solo muestra un encabezado y "END" un pie de página.
- `ls ~/projects | fzf | xargs -I_ code ~/projects/_`: xargs permite que para cada argumente en la salida del primer comando ejecutar la acción del comando después de "xargs". En este se lista el contenido de la carpeta "~/projects" el cual es la entrada de fuzzy finder en donde se procesde a seleccionar una carpeta y el nombre de ésta a su vez en concatenada "~/projects" por medio de "xargs" mendiante la opción "-I" la cual concatena la ruta mediante el simbolo undescore "_" delante de la ruta "~/projects".
- `diff [file_1] [file_2]`: Compara archivos línea por línea.
- `sort [file]`: Ordena las líneas de texto dentro de un archivo. Por defecto en orden alfabético ascendente.
- `uniq [file]`: Muestra las líneas únicas de un archivo, quitan las líneas que se encuentran repetidas en un archivo.
- `cut [{“-d”: Delimiter. Establece un delimitador} {"Word": Palabra que delimita y va entre comillas, puede ser un espacio en blanco, un caracter, etc.}] (“-f1: Files. Indica que tomará el campo 1: A partir donde él delimitador que se estableció”) (“-s": Si no tiene valor no lo muestre. Ya sea qué se encuentre después o antes del delimitador) [file]`: Extrae líneas ó porciones de ellas en un archivo, mediante el uso de delimitadores, y muestra dicho contenido.
- `wc ("-l": Número de líneas), ("-w": Número de palabras) [file]`: Word Count. Se utiliza para contar líneas de un archivo, palabras, letras, bytes.
- `nl [file] (“-i: ”Flag para qué cuente de forma autoincremental)`: Número de líneas de un archivo.
- `date ({-d "+5 days"}: Toma el día actual e incrementa 5 días)`: Muestra la fecha y la hora.
- `cal ("mm yyyy": Muestra dicho mes)`: Muestra un calendario.
- `bc`: Calculadora.
- `man ascii`: Muestra la tabla de caracteres ASCII en octal, hexadecimal y decimal.
- `echo ("-e": Habilita la interpretación de backslash escapes "\", como "\n": nueva línea) [string]`: Muestra los argumentos que recibe en la salida estándar.
- `ffmpeg ["-i": Input file] (input_file.avi) (output_file.pm4)`: Convierte un archivo del formato AVI al formato MP4.
- `nano`: Editor de texto en la terminal. Qué puede ser llamado con el comando “pico”.
- `nslookup [domain_name]`: Permite saber información relacionada los DNS, por ejemplo: si el servidor está resolviendo correctamenta la dirección IP y los nombres de dominio.
- `dig [domain_name]`: Realiza solicitar información a los servidores DNS. Reemplazará a `nslookup`.
- `whois [domain]`: Permite ver la información sobre quién es el propietario del dominio.
- `ifconfig`: Muestra información de la configuración de red del equipo.
- `rfkill ["list all": Lista todas las conexiones inlámbricas] ["unblock all": desbloquea todas las conexiones inalámbricas]`.
- `netstat ("-nr" donde "r" representa las tablas de ruteo y "n" indica que no resuelva, es decir, que no convierte direcciones de hosts o números de puertos a nombres, por lo cual el comando es más rápido) ("-i": Muestra estadísticas sobre las interfaces de red) ("-a": All. Muestra todo) ("-tu": Para las conexiones TCP, mientras que "u" para las conexiones UDP) ("-p": Muestra las estadísticas acerca del protocolo) ("-l": Muestra todos los sockets en escucha)`: Network Statics. Muestra las conexiones entrantes/salientes de red, tablas de enrutamiento y otras características de interfaz de red.
- \-\- Linux `ss`: Permite obtener información sobre conexiones de red, estadísticas de protocolos de red y conexiones de socket. Reemplazará a `netstat`.
- `curl (“-o: Descargar”) [url]`: Cliente URL.
- `traceroute [URL ó ip_address]`: Muestra la ruta que sigue un paquete del usuario al host de destino solicitando a cada uno de los enrutadores por donde pase dicho paquete información como: dirección ip, nombre de dominio, y tiempo de conexión entre el equipo del usuario y cada uno de los nodos en el camino.
- `ping [ip_address]`: Envía una petición de escucha a esa dirección ip.
- `tcpdump (-i”: interface de red, donde “any”: Cualquier interface) [any: Nombre de la interfaz] ("host public_ip_addrees": Apunta a un host) ("-p tcp": Protocolo que va a utilizar) (“-nn”: No resuelve, un solo "n" no resolverá los nombres de hosts, el "nn" no resolverá ni los nombres de hosts ni de puertos) (“port 8080”: Puerto en el que escucha)`: Captura y muestra los paquetes transmitidos y recibidos en una red.
- `nc ("-vz": donde "v" muestra información de la conexión y "z" especifíca que debe escuchar en busca de demonios sin mandarles ningún dato) ("-l": Listening mode. Se utiliza para indicar que debe escuchar una conexión entrante, en lugar de iniciar una conexión a un host remoto) ("-n": Indica que no realice búsquedas de DNS ó servicios en direcciones, hostnames ó puertos especificados) ("-p": Puerto) [URL ó ip_address]`: "NetCad" Permite acceder a los puertos TCP o UDP ya sea de la máquina local o de manera remota, y quuedar en escucha del puerto pasado com parámetro.
- `lsof ("-i :{port_number}": Lista los archivos abiertos por puerto) [user | process_id]`: List Open Files. Lista los archivos que están siendo utilizados por difrentes tipos de procesos como, procesos de usuario, procesos que escuhan en un puerto.
- `sudo passwd [user]`: Se utiliza modificar o agregar la contraseña de usuario.
- `sudo: [command]`: "Super User Do". Ejecuta un comando como administrador. Y pedira la contraseña de administrador, despúes ésta se guardará en memoria por una cantidad de tiempo que al pasar y posteriormente ejecutar algún otro comando con "sudo", volverá a solicitar la contraseña de administrador.
- `su ("-": Configura las variables de entorno y de sistema para el usuario que se indique. Es decir, inicia una nueva instancia de shell) (user)`: Substitute User. Cambia de usuario sin tener que cerrar la sessión, otorgando shell y los permisos del usuario indicado, por lo cual deberá conocer la contraseña de éste último. Sin embargo se mantendrá en el mismo directorio de trabajo. Si no se indica algún usuario toma el actual, con los privilegios de superusuario.
- `sudo ("-l": Muestra una lista de los comandos que puede ejecutar el usuario actual) ("-k": Dejar de tener privilegios de administrador) ("-u [user]": Ejecuta comandos del usuario que se le indica) ("-e [file]": Si el usuario tiene los respectivos privilegios de administrador en el archivo "/ect/sudoers", mediante esta opción puede editar archivos del sistema como: "/etc/hosts". Está opción equivaale al comando: "sudoedit") [command]`: Ejecuta dicho comandos de Super Usuario.
- `sudo su`: Lanza la petición para cambiar al usuario root, pero utilizando la contraseña del usuario actual.
- `sudo -i`: Lanza la petición para cambiar al usuario root con la contraseña del usuario actual. Pero abandonando el entorno del usuario y creando un nuevo entorno para el usuario root.
- `sudo -s`: Lanza la petición para cambiar al usuario root con la contraseña del usuario actual. Proporcionando una shell como usuario root y aunque trabaja en el entorno de root, los permisos no son totales. Equivale a ejecutar: "sudo /bin/bash".
- `sudo visudo`: Permite al usuario obtener los privilegios de administrador y modificar el archivo "/etc/sudoers". Invoncando al editor por defecto genralmente "vim", a su vez éste comando bloquea el archivo para que nadie más lo pueda modificar, esto alguien más con privilegios de administrador pudiera sobreescribir los cambios ya hechos. También éste comando al guardar los cambios, verifica la sintaxis y/o integridad del archivo.
- `chmod [octal: (655) ó por letra: (u+x) (g-w) (o-w) (a-x) (+w)] [file]`: Change Mode. Cambiar los permisos de un archivo o carpeta.
- `chown ("--reference file1 to file": Copia los permisos de file1 en file2) (“-R”: Permite cambiar de manera recursiva) [“new_user:new_group” También permite usar el nombre de usuario y el nombre de grupo al que pertenece separado por dos puntos y su vez estos pueden ser sustituidos en vez de letras por números “0:0” Mediante el identificador numérico del usuario ó UID y el identificador número de grupo ó GID, y sí el nombre del grupo se deja en blanco se asume que será al mismo grupo al que pertenece ese usuario] [file]`: Change Owner. Permite cambiar al propietario de un directorio ó archivo.
- `chgrp ("-R": Recursivo, cambiar el directorio y todos los archivos que se encuentren dentro de él) [new_group] [file]`: Cambia de grupo un archivo.
- `chsh ["-s": Indica la shell a utilizar] [/bin/(shell): Ruta absoluta de la shell] (user)`: Cambia la shell de inicio de sesión al usuario que se le ha pasado como parámetro.
- `chfn [options] [user]`: Agrega o cambia la propiedades de la información de usuario como: full_name, home_phone, room_number, work_phone, and other. Campos que son presentados cuando se agrega un usuario con el comando "useradd". En BSD estos campos son: location, authname y newshell.
- `ps [“-e": Muestra los procesos de todos los usuarios que se están ejecutando] [“-f": Muestra el formato en forma de árbol] ["-t": Muestra infromación sobre los precesos conectados a la TTY que se le pase como parámetro] ["-a": Lista todos los procesos, excepto los de sesión] ["-x": Muestra los procesos con el estilo BSD]`: Visualizar los procesos que están corriendo, solo en el momento en el que se ejecutó dicho comando.
- `top (| less)`: Muestra los procesos que actualmente se están ejecutando en el equipo, es dinámico, es decir que la información se está actualizando constantemente a diferencia del comando “ps” que es como si este tomará un snapshot del momento en que se ejecutó. Donde "| less": redireccionara la salida de "top" a la entrada de comando "less", con esto la salida siempre será visible y se podrá ver el historial de todos los procesos ejecutados. Con la tecla "?" muestra la ayuda con las shorcuts disponibles.
Con "Shift + P" ordena los procesos por uso de CPU y con "Shift + M", los ordena por el uso de memoria.
- `dmesg`: Diagnostic Message. Muestra los avisos guardados en el buffer en formato humano y contiene los avisos más importantes que se generarón durante el inicio del sistema o durante su funcionamiento generados por el kernel.
- `pgrep ("-a": Muestra todos los procesos) ("-u": Muestra todos los procesos asociados a un usuario) [process_name/user]`: Al pasarle un nombre de proceso, por ejemplo: "pgrep firefox" devuelve su PID.	
- `kill ("-9": Obliga al propio sistema operativo a matar el proceso) ("-1": Envía una señal SIGHUP: "Signal Hang Up". Cierra el terminal donde se ejecutó ésta señal) [process_id]`: Termina con el proceso asociado al id que se le indica.
- `killall [process_name]`: Mata todos los procesos relacionados al nombre pasado como parámetro.
- `sleep [seconds ó {1m}]`: Suspende la ejecución por el intervalo de tiempo pasado como parámetro.
- `jobs`: Muestra los procesos que se encuentran en segundo plano.
- `fg ("%1": La tarea 1)`: Background. Trae al primer plano un proceso que se está ejecutando en segundo plano.
- `bg [job]`: Foreground. Reanuda las tareas suspendidas. El número de trabajo se denomina: %number.
- `nohup [command]`: Permite mantener la ejecución de un comando, pese a salir de la terminal (logout). También permite pasar ejecutar un comando y enseguida "&", lo cual va a generar una salida llamada "nohup.out" y en dicha salida mediante un "cat", permitirá ver toda la información de lo que realizó dicho comando.
- `screen ("-ls": Muestra todas las terminales abiertas) ("-r PID": Restore. Entra nuevamente a la sesión que se le está indicando)`: Multiplexa terminales. Para salir de una terminal sin finalizar la sesión: `^ + A, D`
- `reset`: Vuelve a inicializar la terminal. Útil cuando la ejecución de un proceso deja en estado incovniente la terminal.
- `exit`: Salir del terminal.
- `fdisk ["/dev/disk{n}"]`: Sirve para administrar particiones.
- `df (“-h: Leer las cosas de forma humana”)`: Disk Free. Sirve para mostrar el espacio libre en el disco duro, en las diferentes particiones que están montadas.
- `du (“-h: Leer las cosas de forma humana”), (“-a: Muestra la información para cada archivo dentro de un directorio”), (“-s: Muestra un resumen”)`: Disk Usage. Sirve para mostrar el uso del disco duro. Complementa al comando “df”.
- `dd if=[/dev/sda1] of=[/dev/sdb1] ("bs=[1M]": Block, permite mediante ésta opción que tanto la escritura como la lectura se haga en bloques de 1 Megabyte)`: Dataset Definition. Su nombre proviene de duplicador de datos, pues permite copiar datos. La diferencia con "cp" ó "rsync" es que pueden ser dispositivos como: HDD, disketts, USB, particiones, ó imagenes de disco, pero no carpetas. Además realiza está operación a nivel de bites, y resulta útil especialmente cuando se desea clonar un HDD o crear una imágenes de bloque (file.img) ó ISO de un volumen.
- `stat [directory]`: Muestra estadísticas sobre un archivo a diferencia de `ls` muestra información como espacio, directorio donde se encuentra, permisos, último acceso, fecha de modificación, fecha de cambio.
- `tar ["-xvf": Donde "x" signfica Extract el erchivo, "v" viende Verbose, mostrando el progreso de extracción, y "f" indica el nombre del archivo] [file.tar] ("-C {path}": Donde "C" viene de cambiar el directorio donde se deseaa extraer los archivos)`: Permite comprimir/descomprimir archivos en el directorio actual.
- `tar ["-tf": Donde "t" es tabla de contenidos y "f" indica el nombre del archivo] [file.tar]`: Muestra el contenido del Tarball.
- `tar ["-cvf":Donde "c" viene de Create, "v", viene de Verbose muestra el progreso de creación y "f" muestra el nombre del archivo] [file]`: Crea un archivo .tar. Tar tiene una compresión en relación al 50%. Y los permisos y propiedades de los archivos se mantienen intactos.
- `tar ["-xvjf": Extract, Verbose, "j" vienne de archivo compresion Bzipped2, Filename] [file.bz2]`: Descomprime un archivo Bzipped2.
- `tar ["-xzvf" Extract, "z" viene de archivo GZIP, Verbose, filename] [file.tar.gz]`: Descomprime una archivo TGZ. Estos archivos se empaquetarón primero en formato "tar" y posteriormente se comprimierón con Gzip, de hahí la extensión "tar.gz"
- Los archivos contenidos en el archivo comprimido se empaquetan primero en un archivo TAR y posteriormente se comprimen utilizando el programa GZIP
- `gzip [file]`: Comprime un archivo y lo renombra como "file.gz". Gzip posee una algoritmo de compresión más eficiente, manteniendo la marca de tiempo y demás propiedades intactas, sim embargo se desaconseja su uso en archivos con formato: mp4, mp3, jpg, y otros archivos multimedia, que ya se encuentran comprimidos.
- `gunzip ["-c"] [file.gz]`: Muestra el contenido del archivo "gz" sin descomprimirlo.
- `gzip ["-d": Decompress] [file.gz]`: Descomprime un archivo "gz".
- `bzip2 [file]`: Crea un archivo con la extensión "bz2". En Bzipped2 cada archivo se sustituye por una versión comprimida de si mismo, reemplazando al archivo original.
- `bzcat [file.bz2]`: Mostrar el contenidos del archivo.
- `bzip2 ["-d": Decompress] [file.bz2]`: Descomprime al archivo "bz2".
- `zip ("-r": Recursivamente) [file.zip] [path]`: Crear un directorio comprimido ZIP.
- `zipinfo [file]`: Muestra los archivos que se encuentran dentro del comprimido.
- `unzip [file.zip]`: Descomprime el archivo zip en el directorio actual.
- `reboot`: Reinicia el dispositivo.
- `halt`: Apaga la computadora de forma forzada.
- `shutdown ("-h": Linux se apaga en un minuto por defecto, dicho flag significa lo mismo) ("-r": Flag que indica reiniciar) ("now": Realizar la instrucción inmediatamente)`: Apaga o reinicia la computadora dependiendo del parámetro. A diferencia del comando “halt” avisa a las aplicaciones que se deben cerrar para apagar/reiniciar.

## Símbolos especiales

- `0: Input ó stdin, 1: Output ó stdout, 2: Error ó stderror`: Cada valor número representa los respectivos flujos.
- `comand_1; comand_2 ; ... ; command_n`: Cuando se quiere ejecutar una de serie de de diversos comandos en una sola línea.
- `*`: Es un comodín, su significado es todos.
- `#`: Al anteceder este simbolo en el prompt se interpretará como un comentario, pero se guarda en el historial. así mismo también se puede uti;izar para recortar una variable string
- `<`: Redirecciona la entrada estándar. Sobreescribiendo cualquier información previa.
- `<<`: Redirecciona la entrada estándar. Agregando información en caso de que exista alguna previamente.
- `>`: Redirecciona la salida estándar. Sobreescribiendo cualquier información previa.
- `>>`: Redireciona la salida estándar. Agregando información en caso de que exista alguna previamente.
- `|`: Pipe. Permite concatenar la salida de un comando a como argumento en la entrada de otro comando u archivo. Ejemplo: `history | less`.
- `&`: Entrada, salida y error. Al utlizar después de un comando siginifica que dicha ejecución del comando será envíada al background. Por ejemplo: `top &`. También permite redireccionar la salida estándar y el error, por ejemplo: `ls -l > files.txt 2>&1`, donde `&1` significa: el mismo lugar que la salida estándar (1). Una forma abreviada de lo anterior es: `ls -l >& files.txt`.
- `&&`: Se utiliza para concatenar comandos siempre y cuando ninguno tenga como salida error, se ejecutarán. Por ejemplo: `apt update && apt upgrade`.
- `||`: OR. A diferencia de `&&`, permite ejecutar el siguiente comando en caso de que el comando anterior presente una salida de error. Por ejemplo: `curl ifconfig.me || ifcongif`.
- `!`: Operador NOT, ejecuta cualquier instrucción que no lleve `!`, por ejemplo: `rm -r! (*. html)`.
- `\`: Backslash. Caracter de escape, permite permite conservar el valor literal del caracter delante de él, excepto cuando se trate de una nueva línea(`\n`), por ejemplo: `echo \\Smith`, la salida será "\\Smith". También permite escapr "backspace" mediante "\ ", útil cuando se desea ir a un directorio que en su nombre contenga espacio, por ejemplo: "cd Visor\ Lite".
- `![numero_comando_ejecutado_con_history]`: Ejecuta dicho comando.
- `![command]:p`: Verifica el historial de bash, pero evitando ejecutar dicho comando.
- `!*`: Utiliza todos los parámetros del comando que se ejecuto anteriormente.
- `!![:n Representa un número entero, que indica el número de parámetro correspondiente del comando ingresado]`: Devuelve el último comando ingresado en el Terminal.
- `sudo !!`: Ejecuta el comando anteriormente ingresado como administrador.
- `!$`: Contiene el último argumento del comando que se ejecutó anteriormente.
- `$_`: Representa el último argumento del último comando ejecutado. la difrencia respecto a `!$` es que este token no se guarda en el historial.
- `$(command) ó ’command’ {Sustitución de Comandos}`: Permite que la salida de un comando reemplace al comando en sí. Toma el comando entre paréntesis, lo ejecuta y luego toma la salida (salida estándar) de dicho comando y la reemplaza en esa parte de la cadena de comandos. A diferencia de `’command’`, `$(command)` permite sustituciones anidadas, por ejemplo: `$(ls /home/$(whoami))`.
- `?`: Representa la incógnita de un caracter al ser usado en un texto, por ejemplo: `ls $$file.txt`.
- `%`: Cuando se abre un Prompt secundario y no se encuentre la etiqueta "%" se espera la continuación del mensaje.
- `$?`: Contiene el valor que devolvió el comando ejecutado más recientemente.
- `()`: Operador de procedencia, por ejemplo: `(commandx1 && commandx2) || (commandy1 && commandy1)`.
- `{}`: Permite agrupar un conjunto de parámetros para evitar repetir instrucciones, por ejemplo: `cp ../{fileA, fileB, fileC} ~/Desktop` ó `mv some/deeply/nested/thing/{old,new}.txt` que remonbrará el archivo rápidamente sin necesidad de escribir toda la ruta.

## Variables especiales

- `$1, $2, $3, ..., $n`: Representan parámetros de línea de comandos, donde "n" representa la posición del argumento que se le pasa a un script desde el intérprete de comandos.
- `S*`: Contiene todos los argumentos posicionales del Shell en un solo valor de cadena.
- `$0`: Muestra el nombre de la "SHELL" ó el nombre del script en uso.
- `$TERM`: Especifica el tipo de terminal a emular cuando se ejecuta el Shell.
- `$SHELL`: Muestra la ruta del intepréte de comandos o Shell.
- `$PS1`: Contiene la cadena de caracteres que representa el Prompt principal.
- `$PATH`: Muestra el contenido de la variable de entorno PATH.
- `$LOGNAME`: Contiene el valor del usario registrado actualmente en el sistema.
- `$USER`: Contiene el nombre de usuario, la diferencia es que LOGNAME es heredada de System Unix V, mientras que USER se comenzo a utilizar con BSD.
- `$HOME`: Contiene el valor de la ruta del directorio home.
- `$PWD`: Contiene la ruta actual.
- `$OLDPWD`: El directorio de trabajo anterior, mediante el comando "cd -".
- `$UID`: Contiene el UID del usuario actual.
- `$$`: Contiene el ID del proceso actual.
- `$$PID`: Contiene el valor del padre del proceso actual.

## Delimitadores

- `IFS`: Internal Field Separator. Variable de shell que permite separar campos que no sean espacios, actuando como delimitador.
- `EOF`: End Of File. Este opoerador indica el fin de in archivo.

## Shorcuts

- `Tab`: Tabular una vez permite autocompletar lo que se esté escribiendo cuando solo existe una opción ó tabular 2 veces para navegar entre las posibles opciones a elegir.
- `^ + A`: Mueve el cursor al principio de la línea.
- `^ + C`: Mata cualquier proceso que se este ejecutando.
- `^ + D`: Fin de la transmisión, equivalente a "EOF" ó "exit", termina la sesión del usuario.
- `^ + E`: Mueve el cursor al final de la línea.
- `Opt + Right arrow ó -- Linux ^ + Right arrow`: Mover una palabra hacia adelante el cursor.
- `Opt + Left arrow ó -- Linux ^ + Left arrow`: Mover una palabra hacia atrás el cursor.
- `^ + L ó clear`: Limpiar la terminal.
- `^ + R`: Inicia una búsqueda del último comado que haya sido ejecutado y cumpla con los parámetros que sean ingresados.
- `^ + T`: Intercambia los dos últimos caracteres, donde se haye pocisionado el cursor.
- `^ + U`: Se borra la línea completa, independientemente donde esté el cursor.
- `^ + W`: Elimina una palabra en la línea actual.
- `^ + Z: ó bg`: Envía el proceso que se está ejecutando a segundo plano.
- `Esc + T`: Imtercambia las dos últimas palabras donde, se haye pocisionado el cursor.
- \-\-Only Linux `^ + Opt + FunKey(1-6) ó chvt N`: Change Foreground Virtual Terminal, Es usado para cambiar entre diferentes terminales TTY.

## Files

- `~/`: Home.
- `/dev/null`: "Null Device File" este archivo descartará todo lo que se le haya escrito y devolverá un carácter de fin de línea "EOF" al leerlo. Es decir áctua como un vació que absorbe cualquier cosa que se le pase.
- `/dev/zero`: Es un archivo especial que porvee tantos caracteres null: 0x00, como se leean de él. Se utiliza principalmente para sobreescribir información ó crear ficheros de determinado tamaño.
- `echo '' /dev/tcp/[127.0.0.1]/[30000] && echo "[+] Opened port" || echo "[x] Closed port"`: Simple Bash scan ports.
- `cat /proc/sys/vm/swappiness`: Muestra el valor de la memoria swap.
- `cat /proc/cpuinfo`: Muestra la información referente al CPU(s) del equipo.
- `cat /proc/loadavg`: Mostrar Load Average, el cúal es la carga promedio del sistema. A grandes rasgos permite saber si un servidor/host se encuentra sobrecargado si su valor es mayor ó igual a \[cantidad de CPU(s)\].
- `/etc/fstab`: Contiene la lista de discos y particiones disponibles, en él se indica como montar cada dispositivo y que configuración utilizar.
- `sudo cat /etc/paswd`: Contiene toda la información sobre las cuentas de usuario registradas, así mismo determinando quién puede acceder al sistema y las acciones que pueden realizarse dentro de éste.
- `sudo cat /etc/passwd`: Almacenan los hash de las contraseñas y brinda información sobre la caducidad y vigencia de la cuenta.
- `/etc/sudoers`: En este archivo se define una lista de qué usuarios pueden obtener privilegios de administrador, mediante el uso del comando "sudo". El símbolo "%" en este archivo significa que el nombre que le sucede es el identificador de un grupo.
- `sudo cat /etc/group`: Se encuentran todos los grupos creados en el sistema.
- `sudo cat /etc/gshadow`:  Se encuentran almacenadas los hash de las contraseñas de grupos.
- `(cd /tmp && [command])`: Va a direcotrio "tmp", ejecuta el comando dado allí y posteriormente regresa al directorio desde el que se lanzó el comando, esto resulta útil cuando se desea realizar pruebas dentro de un entorno controlado.

## Services

- `sudo service [“service”: Nombre del servicio por ejemplo: apache2] [“acción”: Acción a realizar, por ejemplo: start]`: Opera en los archivos de configuración localizados en la ruta /etc/init.d y se usó este comando junto con el antiguo sistema de inicio.
- `sudo systemctl [“acción”: Por ejemplo: status, ("enable": Esta opción mantendrá el proceso ejecutándose incluso des[úes de reiniciar el servidor), start, reload, stop] [“service”: Nombre del servicio, por ejemplo: nginx]`: Opera sobre los archivos de configuración ubicados en "/lib/systemd". Si existe allí un archivo, lo usará para realizar la acción requerida sobre ese servicio. En caso de no hallar el archivo de configuración, entonces lo buscará en la ruta "/etc/init.d".
- `etc/init.d/[service] [action]`: Ejecuta la acción indicada sobre el servicio descrito.
- `init 0`: Apagar el sistema inmediatamente

### Alias

- `> (file_name) << "END" Linea(s) de texto END`: Crea a "file_name" le pasa un stream de texto de múltples lineas.
- `>> (file_name)`: Crea "file_name", permitiendo agregar un texto de múltiples lineas y se deberá pulsar ^ + d, para terminar con la escritura. Donde el doble “>>” significa que en dicho texto se agregará las líneas al final en caso que el archivo ya contenga texto.
- `cat << END Linea(s) de texto END`: Visualizar desde un script bash al terminal el texto que sea ingresado en una o múltiples lineas.
- `cat > file.[extension] {Linea(s) de texto} Ctrl + D`: Editor de texto con "cat".
- `ffmpeg -f x11grab -s wxga -r 25 -i :0.0 -someq /tmp/out.mpg`: Graba la pantalla del escritorio.
- `ls ~/projects | fzf | xargs -I_ code ~/projects/_`: 

## Mac Commands

- `open`: Abre con el programa por defecto que tiene el sistema operativo para abrir el archivo que se le pase como parámetro y solo esta presente en Unix - Mac.
- `pbcopy`: Copia la salida éstandar al portapapeles.
- `say`: Leé el texto ingresado.
- `pbpaste`: Pega el contenido del portapapeles.
- `defaults [parameter]`: Permite establecer propiedades en los archivos de configuración "plist".
- `defaults write com.apple.finder AppleShowAllFiles TRUE`: Muestra los dotfiles en el Finder.
- `diskutil list`: Muestra la lista de unidades o dispositivos.
- `diskutil mountDisk /dev/disk[n]`: Monta la unidad que se le esta indicando.
- `diskutil unmountDisk /dev/disk[n]`: Desmonta la unidad que se le esta indicando.
- `sudo verifydisk [drive_identifier]`: Permite verificar el estado de un disco.
- `sudo diskutil repairvolume [drive_identifier]`: Una vez que se el disco se haya analizado, permite reparar dicho volumen.
- `softwareupdate --all --install --force`: Permite actualizar el sistema operativo, similar a "apt full-upgrade" en Linux.
- `xcode-select --install`: Instala la CLI de Xcode.

## Ubuntu/Linux Commands

- `tac`: Muestra el contenido de un archivo en orden inverso.
- `mvdir [directory_origin_path] [directory_destiny_path]`: Mueve o renombra directorios.
- - `chattr [{(+/-":Agregar/quitar") a": Append only. Agrega nuevas líneas, pero conservando siempre el contenido previo} {"+i": Immutable. Solo lectura}] [file]`: En los sistemas de archivos ext2..ext4. Permite cambiar atributos especiales en el archivo, para por ejemplo no pueda ser borrado, incluso desde el usuario "root".
- `lsattr`: Permite listar las propiedas de un archivo protegido con "chttr".
- `sudo dpkg ("-l": Muestra los paquetes instalados) ["-i": Install] [packge.deb]`: Instalar un paquete ".deb".
- `apt ("moo": Easter egg de cow) (“search: Buscar un paquete”), (“install: Instalar paquete” {Cuando se instala con “sudo” el comando mostrará una pregunta diciendo si esta seguro de instalar dicho paquete normalmente muestra las opciones “Y/n”, si no se ingresará nada y solo se hiciera Enter tomará la letra por defecto que es la que esta en mayúscula en este caso la opcion “Y”})`: Gestor de paquetes.
- `sudo apt update && sudo apt upgrade -y && sudo apt dist-upgrade -y && sudo apt autoremove -y && sudo apt autoclean -y`: Alias para realizar todo el proceso de actualización del sistema.
- `lsb_release (-a: All)`: Información específica respecto a la distribución Linux.
- `lsusb`: Muestra todos los dispositivos USB conectados a la computadora.
- `lsblk`: Muestra las unidades de almacenamiento en el dispositivo así como sus particiones.
- `lscup`: Muestra la información del procesador.
- `lspci`: Muestra todos los dispositivos PCI en la computadora.
- `lshw`: Muestra toda la información del hardware.
- `free ({"-m": Muestra la cantidad de memoria en Megabytes} {"-g": Muestra la cantidad de memoria en Gigabytes})`: Muestra la memoria disponible en el host.
- `watch free [“-h”: En formato humano]`: Permite ver la memoria libre, por defecto la muestra en bytes.
- `sudo mount {"-n -o remount, rw": "-n" Indica montar sin escribir en "/etc/mtab", necesario para un sistema de solo lectura,  "-o" indica opción que indica volver a montar dicha partición como solo de lectura y escritura, esto es útil para recuperar contraseña} ("-t {"vfat":FAT ó "ntfs-3g": NTFS, ó "ext4"}": Indica el sistema de archivos) [/dev/sd{a}{n}] [/{media/mnt}/{usb}]`: Permite montar dispositivos.
- `sudo umount ("-a": Permite desmontar todas las unidades) ("–t {vfat FAT}": Indica desmontar todas las unidades de tipo ) [/dev/sda{n}]`: Permite desmontar un sistema de archivos montado previamente.
- `pstree`: Muestra un árbol de como están relacionados todos los procesos.
- `pwdx [PID]`: Lista la ruta o directorio donde se está ejecutando cada proceso.
- `sudo useradd ("-m": Este flag indica que debe ser creado el directorio "home" del usuario) [user]`: Agrega un usuario a bajo nivel. A difencia del script de Perl `adduser`. Y cada campo de la cuenta debe ser agregado por separado, mediante comandos como: "paswd" y "usermod". Algo similar a "dscl" en Mac OS, donde mediante este comando se agrega: contaseña, directorio home, shell, es decir los campos que componen la cuenta en el archivo "/etc/passwd". Además de agregar el usuario en el archivo "/etc/sudoers", para que pueda obtener privilegios de administrador.
- `sudo usermod ("-l [new_name]": Cambiar el nombre de usuario) ("-aG": Append, pues si no se usará ésta opción se agregaría a; grupo indicado, pero eliminando al usuario de los demás grupos a los que pertenece, Group. Añade el usuario al grupo) ["group_name": Nombre del grupo. Para agregar al grupo de administrador en distribuciones basadas en Debian es "sudo", mientras que para basadas en RedHat es "wheel"] [user] ("--shell [/bin/bash]": Asigna una shell al usuario)`: Permite realizar cambios en la cuenta del usuario, algunas opciones son: nombre, directorio home, agregar a otros grupos, establecer fecha de expiración para la cuenta, bloqueo de la contraseña de usuario, así como desbloqueo.
- `sudo userdel ("-r": Borra el directorio "home" del usuario con su contenido y la cola de su email) ("-f": Forza la eliminación de los archivos) [user_name]`: Permite eliminar la cuenta del usuario que se le esté indicando.
- `sudo groupadd ("-g": Asigna un GID, el cual puede se un valor númerico entero mayor a 99 y único) [group_name]`: Agregar un nuevo usuario al sistema.
- `sudo gpasswd [group]`: Permite listar, agregar, eliminar usuarios de un grupo, establecer una contraseña de grupo.
- `sudo groupdel [group_name]`: Elimina el grupo indicado. No tiene ninguna opción (flags).
- `sudo adduser [user_name]`: Agrega un nuevo usuario creando de forma automática la carpeta “home”. Y pide información del usuario como: password, nombre, habitación, teléfonos y otros.
- `sudo deluser ("--remove-home": Borra el directorio home del usuario y la cola de su email) ("--remove-all-files": Remueve cualquier archivo que le pertenezca al usuario) ("--backup-to [path]": Realiza una copia de los archivos del usuario en la ruta indicada) [user_name]`: Al igual que el comando "adduser", es un script en Perl, que utiliza "userdel" y "groupdel" para eliminar cuentas de usuario y grupos del sistema.
- `sudo addgroup ("--system": Crea un grupo del sistema) [group_name]`: Script en Perl con una interfaz que por detrás hace uso de programas de bajo nivel como "groupadd".Crea un nuevo grupo.
- `sudo delgroup ("-only-if-empty": No se elimina el grupo en caso de todavía contenga algún miembro) [group_name]`: Script en Perl que permite eliminar un grupo con una interfaz sencilla. También este comando no eliminará al grupo primario de un usuario existente.
- `iproute2`: Es una suite de comando para administrar interfaces de red. Por ejemplo, `ip`, que desplegará toda la información relacionada con las interfaces de red. Reemplazará a "ifconfig".
    - `ip {link (l)}`: Esta opción muuestra y permite modificar las interfaces de red.
    - `ip ("-4": Muestra todas las interfaces de tipo IPv4){address (addr, a)}`: Muestra y permite modificar las direcciones IP.
    - `ip {route (r)}`: Muestra y permite modifica la tabla de enrutamiento.
    - `ip {neigh (n)}`: Muestra y permite manipular los objetos vecinos de la tabla ARP.
- `iwconfig`: Muestra la información de la configuración de red inalámbrica del equipo.
- `wget ("-c": Continúa una descarga detenida en caso de que ésta haya perdido la conexión), ("-r": Recursivamente), ("-t": Cuántas veces debe intentar, en caso de perder la conexión) [URL/file]`: Descarga los archivos de dicha URL.

## Programs

- `tldr [command]: Significa`: "Too Long; Didn’t Read" y permite resumir el manual ("man") del comando que le sea pasado como argumento, mediante ejemplos prácticos.
- `rename [original_file] [renamed_file]`: Rename files.
- `lsd`: Repositorio de GitHub, el cual mejora el output del comando "ls" estéticamente.
- `Supercat`: Es una utilidad que muestra en un formato "más amigable" la salida de cat.
- `bat`: Repositorio de GitHub, el cual mejora el ouput del comando "cat" estéticamente. además cuenta con extensiones: "bat-extras".
- `vim`: Editor de texto en la terminal que tiene múltiples modos. Qué puede ser llamado con el comando “vi”.
- `tree [“-a”: Muestra todos los archivos] [“-f”: Muestra los archivos con su ruta respectiva] [-C: Si la variable LS_COLORS esta configurada, ésta opción la salida de "tree" muestra el árbol de directorios con colores]`: Es un programa que permite muestrar los directorios en forma de árbol.
- `pv`: Permite ver el progreso de los datos a tráves de una tubería (Pipe), brindando información del tiempo transcrurrido, así como una barra de progreso.
- `aptitude ("moo", "-v", "-vv", "-vvv", "-vvvv", "-vvvvv", "-vvvvvv": Easter eggs)`. Sistema de gestión de paquetes.
- `htop`: A diferencia del comando "top", con esta herramienta se puede interactuar.
- `BpyTOP`: Es un monitor de recursos escrito en Python.
- `jp2a`: Conveierte una imagen JPG a formato ASCII.
- `UFW`: Firewall.
- `Telnet`: Aunque "SSH"es más seguro que telnet. Permite realizar conecxiones remotas sin cifrar.
	- `telnet towel.blinkenlights.nl`: Ver StartWars en fomato ASCII.
- `GNU Awk`: Implementacíon GNU del lenguaje de programación para procesamiento de texto AWK.
- `eXtended ARGuments`: Se utiliza para construir comandos desde la entráda estándar. Permitiendo que comandos como "cp" puedan tomar la entrada estándar de la salida estandar de otro comando, algo que con solo pipes "|" no es posible.
- `nmap [host_ip_address]`: Network Mapper. Permite ver los puertos abiertos en un host.

## Terminal's Funny
- https://www.emezeta.com/articulos/20-curiosidades-geeks-para-terminales-linux
