<h2 id="titulo">Ejercicios sistemas Linux 100 primeros</h2>

<p>A continuacion podremos ver resueltos los siguientes comandos:</p>

<ol>
<li> ls /bin</li>
<li>ls /tmp</li>
<li>ls -dr /etc/t*</li>
<li> ls /dev/tty??</li>
<li>ls /dev/tty*[1-4]</li>
<li>ls /dev/t*C1</li>
<li>ls -a /</li>
<li>ls -d /etc/[^t]* </li>
<li>ls -R /usr</li>
<li>cd /tmp</li>
<li>pwd</li>
<li>date +"%A %D - %r" || simplemente DATE</li>
<li>cd /HOME </li>
<li>pwd </li>
<li>ls -i </li>
<li><p>mkdir PRUEBA<p> 
<p>touch PRUEBA/{.f_hidden1,.f_hidden2,.f_hidden3}</p>
<p>touch PRUEBA/{file1,file2,file3}</p>
 <p> mkdir PRUEBA/{dir1,dir2,dir3}</p>
<p>rm -rf PRUEBA/*<p> </li>
<li><p>mkdir PRUEBA/{ dir1,\</p>
 <p>dir1/dir11,\</p>
 <p>dir2,\</p>
 <p>dir3,\</p>
 <p>dir3/dir31,\</p>
 <p>dir3/dir31/dir311,\</p>
 <p>dir3/dir31/dir312}</p></li>
<li>cp /etc/motd ./PRUEBA</li>
<li>cd PRUEBA<p>
<p>cp mensaje dir1/mensaje && cp mensaje dir2/mensaje && cp mensaje dir3/mensaje<p></li>
<li>ls -R PRUEBA</li>
<li>cp -r /etc/rc.d dir3</li>
<li>cp -r /bin/?a?? PRUEBA/dir3/dir31/dir311</li>
<li><p>sudo cp -r ../user_other PRUEBA/dir1/dir11<p>
<p>$ cp -r ../user PRUEBA/dir1/dir11<p></li>
<li> mv PRUEBA/dir3/dir31 PRUEBA/dir2</li>
<li>ls -R $HOME</li>
<li>mv PRUEBA/dir3/mensaje PRUEBA/dir3/.mensaje</li>
<li>rm -rf PRUEBA/dir1</li>
<li>ls /dev/t???[a*b]</li>
<li>find dir312 -type f -regex ".* ???q[^b$]" -exec rm -r {} \;</li>
<li> mv PRUEBA/dir2/dir31/dir312 PRUEBA/dir3</li>
<li>ln -s /home/usuario1/PRUEBA/dir1 PRUEBA/dir3/enlacedir1</li>
<li><p>cd PRUEBA/dir3</p>
<p>mkdir enlacedir1/nuevo1</p></li>
<li>cp -r /bin/u* enlacedir1/nuevo1/</li>
<li><p>ln fich1 dir1/enlace</p>
<p>ln fich1 dir2/enlace</p></li>
<li><p>rm fich1</p>
<p>cp dir1/enlace dir3/</p>
<p>ln -s /home/usuario1/PRUEBA/dir2/enlace /home/usuario1/PRUEBA/dir1/enlafich1</li>
<li>ln -s dir2/enlace dir1/enlafich1</li>
<li>
<p> cd dir1</p>
<p>dir1$ cp enlafich1 ../dir2/dir31/dir311/fich1</p></li>
<li>
dir1$ cat enlafich1</li>
<li>
PRUEBA$ rm dir2/fich1</li>
<li>
$ rm -r * </li>
<li>
$ mkdir dir1 dir2</li>
<li>
$ chmod = dir1</li>
<li>
$ chmod 751 dir2</li>
<li>
$ ls -la ./dir2</li>
<li>
<p>mkdir dir2/dir21</p>
 <p>no se puede crear</p></li>
<li>
<p>chmod 200 dir1</p>
<p>ls -l</p>
<p> mkdir dir1/dir21</p>
<p>mkdir: no se puede crear el directorio «dir1/dir21»: Permiso denegado</p> </li>
<li>
<p> touch dir1/{file1,file2,file3}</p>
<p>PRUEBA$ ls -l dir1</p> </li>
<li> <p>ls</p>
<p> dir1 dir2 dir3</p>
<p> mv dir1 dir3/</p>
<p> ls -lR</p>
<p> .:</p>
<p> ./dir2:</p>
<p> ./dir2/dir21:</p>
<p> ./dir3:</p>
<p> ./dir3/dir1:</p> </li>
<li>
./dir3: </li>
<li>
umask 0033 </li>
<li>
$ mkdir dira dirb dirc dird </li>
<li>
$ ls -l </li>
<li>
<p> touch uno</p>
<p> chmod a-r uno</p>
<p>ls -l</p>
<p> rm uno</p>
<p> _ </p> </li>
<li>
<p> chmod = dir2</p>
<p>chmod o=rwx dir2</p></li>
<li>
<p> mkdir carpeta1 carpeta2</p>
<p> chmod u=rwx,g=,o= carpeta1</p>
<p> chmod u=rwx,g=rx,o= carpeta2</p>
<p> ls -l</p>
<p> touch carpeta1/{fich1,fich2}</p>
<p> chmod = carpeta1/{fich1,fich2}</p>
 <p> chmod o=rw carpeta1/fich1</p>
<p> ls -l carpeta1</p>
<p> touch carpeta2/{file1,file2}</p>
<p> chmod = carpeta2/{file1,file2}</p>
<p> chmod u=rw,g=rw carpeta2/file1</p>
 <p> chmod u=rw,g=r carpeta2/file2</p>
<p> ls -l carpeta2</p> </li>

<li>
<p> su us3rlinux</p>
<p> Contraseña:</p>
<p>## carpeta1 ##</p>
<p># prueba de acceso</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA$ cd carpeta1</p>
<p> bash: cd: carpeta1: Permiso denegado</p>
<p># prueba de lectura</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA$ ls carpeta1</p>
<p> ls: no se puede abrir el directorio carpeta1: Permiso denegado</p>
<p>## carpeta2 ##</p>
<p># prueba de acceso</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA$ cd carpeta2</p>
<p># prueba de lectura</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ ls -l</p>
 <p>total 0</p>
 <p>-rw-rw---- 1 usuario1 usuario1 0 2009-12-08 09:41 file1</p>
<p> -rw-r----- 1 usuario1 usuario1 0 2009-12-08 09:41 file2</p>
<p># prueba de lectura</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ cat file1</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ cat file2</p>
<p># prueba de escritura</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ echo 'hola' > file1</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA/carpeta2$ echo 'hola' > file2</p>
<p>bash: file2: Permiso denegado</p>
<p>exit</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA$ whoami</p>
<p>us3rlinux</p>
<p>us3rlinux@equipo1:/home/usuario1/PRUEBA$ exit</p>
<p>exit</p>
<p>usuario1@equipo1:~/PRUEBA$ whoami</p>
<p>usuario1</p>
<p>usuario1@equipo1:~/PRUEBA$ </p> </li>
<li>
<p> pwd</p>
<p>/home/usuario1/PRUEBA</p>
<p> mkdir correo fuentes</p></li>
<li>
<p> cd fuentes</p>
<p> mkdir dir1 dir2</p></li>
<li>
<p>mkdir ../correo/menus</p></li>
<li>
<p> cd $HOME</p>
<p> find PRUEBA/fuentes -type d -name "*1" -exec rm -r {} \;</p></li>
<li>
<p> find PRUEBA/fuentes/* -type d -regex ".*[0,2,3,4,5,6,7,8,9]" -exec rm -r {} \;</p>
<p> find PRUEBA/fuentes/* -type d -regex ".*[^1]" -exec rm -r {} \;</p></li>
<li>
<p>ls -l /dev/tt*</p></li>
<li>
<p>find /usr/bin -type f</p></li>
<li>
<p> ls /</p>
<p> find / -maxdepth 1 -type d</p></li>
<li>
<p> find / -user root -type f</p></li>
<li>
<p> find /usr/include -type f -regex ".*.h"</p></li>
<li>
<p> ls /bin/ls*</p></li>
<li>
 find /home/us3rlinux -exec file --mime-type -0 '{}' \;</li>
<li>
<p> mkdir uno</p>
<p> chmod u=rw,g=rw,o= uno</p>
<p> ls -ld uno</p></li>
<li>
<p> chmod u=rwx,g=rwx,o= uno</p>
<p> mkdir uno/uno1</p>
<p> chmod u=rwx,g=,o=w uno/uno1</p>
<p> ls -ld uno/uno1</p></li>
<li>
<p>find /home/usuario1 -type f -regex ".*[0-9]" -exec cp -r '{}' PRUEBA/correo/menus/ \;</p></li>
<li>
$ sudo -s</li>
<li>
touch archivo_tamaño_cero</li>
<li>
<p> cat /etc/motd</p>
<p>0 packages can be updated.</p>
<p>0 updates are security updates.</p></li>
<li>
<p> who | grep $USER | sort -k 4 > persona</p></li>
<li>
<p> mkdir carpeta</p>
<p> chmod a-r carpeta</p>
<p> find ~ -type d > direc</p></li>
<li>
$ find ~ -type d 2> malo</li>
<li>
$ find /etc -type f >> direc</li>
<li>
<p> find ./ -type f -not -iname *ai* 1> nuevalista 2> malos</p>
<p>find ./ -type f -iname *ai* 1> nuevalista 2> malos</p></li>
<li>
<p> time `sleep 3`</p>
<p> time who -p %e </p></li>
<li>
$ ps -U root -u root u</li>
<li>
$ ps -U root -u root u | grep -v "`ls /dev`" </li>
<li>
$ echo "`date +"%A %D"` - `pwd`" >>nuevalista</li>
<li>
$ ps axu</li>
<li>
$ top -d .1 -n 10</li>
<li>______</li>
<li>
$ cat /etc/passwd | wc -l</li>
<li>
$ cat /etc/passwd | grep bash</li>
<li>
$ who -q</li>
<li>
<p> man gcc > gcc.man_page</p>
<p> cat gcc.man_page | sed -e 's/ //g' > file.filled</p>
<p> cat file.filled | grep ^[Ll]</p></li>
<li>
$ cat file.filled | grep ^[Ll] | wc -l</li>
<li>
$ cat /etc/passwd | cut -d ':' -f 1</li>
<li>
$ gawk -F: '{print $1, $7}' /etc/passwd</li>
<li>
<p> touch -t 9910011101 good</p>
<p> ls -l good</p>
<li>
$ md5sum good</li>
<li>
<p> md5sum good > good.MD5</p>
<p> echo hola >> good</p>
<p> md5sum -c good.MD5</p>
<p> md5sum good</p></li>
<li>
$ df -lh</li>
<li>
for x in `seq 1 10`; do ps -eo pid,pcpu,pmem,user,args | sort -r -k 2 | head -n 2; sleep 3; done</li>
<li>
<p>ps -eo pid,pcpu,pmem,user,args | grep bash</p>
<p> ps a | grep bash</p></li>
<li>
$ ps -eo args | cut -d ' ' -f 1 | grep ^g | wc -l </li>
