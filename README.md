# WarGames-Natas
Mis pasos en Wargames "Natas"

## Level 0:

Connet to:
http://natas0.natas.labs.overthewire.org/
User and password: natas0

Using the source code with right click in the browser we see in line 16 the password:
<!--The password for natas1 is g9D9cREhslqBKtcA2uocGHPfMZVzeFK6 -->

## Level 1:

http://natas1.natas.labs.overthewire.org/
User and password: natas1
Password : g9D9cREhslqBKtcA2uocGHPfMZVzeFK6

Its blocked rightclicking, but used DevTools in me you can see the code:

<!--The password for natas2 is h4ubbcXrWqsTo7GGnnUMLppXbOogfBZ7 -->


## Level 2:

http://natas2.natas.labs.overthewire.org/
User and password: natas2
Password : h4ubbcXrWqsTo7GGnnUMLppXbOogfBZ7

Usa la url como un directorio porque hay un archivo en localizacion /files/pixel.png pues navegas, hasta el y estara el fichero user.txt 
natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q

## Level 3:

http://natas3.natas.labs.overthewire.org/
User and password: natas3
Password : G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q

This have a comment about "No more information leaks!! Not even Google will find it this time…" 
Esto puede indicar que ha puesto una regla para que los robots de google no escaneen, por lo tanto miramos el archivo ubicado en Robots.txt, ya usando guia de comandos seria :

curl -u natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q  http://natas3.natas.labs.overthewire.org/robots.txt

Y muestra una carpeta llamada s3cr3t asi que :

curl -u natas3:G6ctbMJ5Nb4cbFwhpMPSvxGHhQ7I6W8Q  http://natas3.natas.labs.overthewire.org/s3cr3t/users.txt
natas4:tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm

## Level 4:

http://natas4.natas.labs.overthewire.org/
User and password: natas4
Password : tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm

curl -u natas4:tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm http://natas4.natas.labs.overthewire.org/ -H "host: http://natas5.natas.labs.overthewire.org/"

Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"

Using a curl mode, is -e for reference url, this is a solution:
xcurl -u natas4:tKOcJIbzM4lTs8hbCmzn5Zr4434fGZQm http://natas4.natas.labs.overthewire.org/ -e 'http://natas5.natas.labs.overthewire.org/'


Access granted. The password for natas5 is Z0NsrtIkJoKALBCLi5eqFfcRN82Au2oD
