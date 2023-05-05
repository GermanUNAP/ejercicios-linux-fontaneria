# ejercicios-linux-fontaneriaEn una versión de Linux, pruebe cada uno de los comandos explicados anteriormente.
1. En una versión de Linux, pruebe cada uno de los comandos explicados anteriormente.
    ❯ echo hola>archivo1
    ❯ date>>archivo
    ❯ more archivo1
    hola
    ❯ mail usuario1<mensaje
    zsh: no such file or directory: mensaje
    ❯ mail usuario1<"mensaje"
    zsh: no such file or directory: mensaje
    ❯ echo "construcciond e bloque de comandos PIPES"
    construcciond e bloque de comandos PIPES
    ❯ echo hola | mail user2
    ❯ mail suer2<archivo2
    zsh: no such file or directory: archivo2
    ❯ echo hola>archivo2
    ❯ mail suer2<archivo2
    ❯ mail user2<archivo2
    ❯ car mensaje ; ls
    zsh: command not found: car
    README.md  archivo  archivo1  archivo2
    ❯ cat mensaje ; ls
    cat: mensaje: No such file or directory
    README.md  archivo  archivo1  archivo2
    ❯ car mensaje
    zsh: command not found: car
    ❯ cat mensaje
    cat: mensaje: No such file or directory
    ❯ cat archivo1
    hola
    ❯ cat archivo1; ls
    hola
    README.md  archivo  archivo1  archivo2
    ❯ ls /nuevo && more archivo2
    ls: cannot access '/nuevo': No such file or directory
    ❯ mkdir nuevo
    ❯ ls /nuevo && more archivo2
    ls: cannot access '/nuevo': No such file or directory
    ❯ ls
    README.md  archivo  archivo1  archivo2  nuevo
    ❯ ls /nuevo || more archivo1
    ls: cannot access '/nuevo': No such file or directory
    hola
    ❯ ls nuevo || more archivo1
    ❯ ls nuevo && more archivo2
    hola
    ❯ ls dev>archivo6 &
    [1] 1258
    ls: cannot access 'dev': No such file or directory
    [1]  + 1258 exit 2     ls --color=tty dev > archivo6
    ❯ m,kdir dev
    ^[[Azsh: command not found: m,kdir
    ❯ mkdir dev
    ❯ ls dev>archivo6 &
    [1] 1267
    [1]  + 1267 done       ls --color=tty dev > archivo6
    ❯ ls archivo[3]
    zsh: no matches found: archivo[3]
    ❯ vi archivo3
    ❯ ls
    README.md  archivo  archivo1  archivo2  archivo6  dev  nuevo
    ❯ toush archivo3
    zsh: command not found: toush
    ❯ touch archivo3
    ❯ ls archivo[3]
    archivo3
    ❯ ls archivo[1-3]
    archivo1  archivo2  archivo3
    ❯ ls archivo[!1]
    ❯ ls archivo[git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k]
    zsh: bad pattern: archivo[git
    ❯ ls archivo[git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k]
    zsh: bad pattern: archivo[git
    ❯ ls archivo[!1-3]
    ❯ ls archivo[git clone --depth=1 https://github.com/romkatv/powerlevel10k.git]
    zsh: bad pattern: archivo[git
    ❯ ls arc*
    archivo  archivo1  archivo2  archivo3  archivo6
    ❯ ls archivo?
    archivo1  archivo2  archivo3  archivo6
    ❯ echo prueba >archivo3
    ❯ echo prueba2>archivo4
    ❯ diff archivo3 archivo4
    1c1
    < prueba
    ---
    > prueba2
    ❯ grep "pr" archivo4
    prueba2
    ❯ cat
        HOla
    HOla
    Como
    Como
    Estas
    Estas
    ❯ cat archivo1 archivo2>archivo3
    ❯ cat archivo3
    hola
    hola
    ❯ sort
        durazno
    aceituna
    queso
    leche
    naranja
    harina
    aceituna
    durazno
    harina
    leche
    naranja
    queso
    ❯ vi archivo3
    ❯ sort archivo3
    hola
    hola
    ❯ cat archivo3
    hola
    hola
    ❯ vi archivo3
    ❯ vat acrhivo3
    zsh: command not found: vat
    ❯ cat archivo3
    hola
    hola
    ❯ german>>archivo3
    zsh: command not found: german
    ❯ echo german >>archivo3
    ❯ cat acrhivo3
    cat: acrhivo3: No such file or directory
    ❯ cat archivo3
    hola
    hola
    german
    ❯ sort archivo3
    german
    hola
    hola
    ❯ sort archivo3 || >>archivo2
    german
    hola
    hola
    ❯ cat archivo2
    hola
    ❯ sort archivo3 | >>archivo2
    ❯ cat archivo2
    hola
    german
    hola
    hola
    ❯ echo Puno>>archivo3
    ❯ echo Puno>>archivo3
    ❯ unic archivo3
    zsh: command not found: unic
    ❯ uniq archivo3
    hola
    german
    Puno
    ❯ echo Num1>>archivo3
    ❯ echo Num1>>archivo3
    ❯ echo Num1>>archivo3
    ❯ cat archivo3
    hola
    hola
    german
    Puno
    Puno
    Num1
    Num1
    Num1
    ❯ uniq archivo3
    hola
    german
    Puno
    Num1
    ❯ uniq archivo3 -c
        2 hola
        1 german
        2 Puno
        3 Num1
    ❯ uniq archivo3 -u
    german
    ❯ uniq archivo3 -d
    hola
    Puno
    Num1
    ❯ gre Puno archivo3
    zsh: command not found: gre
    ❯ grep Puno archivo3
    Puno
    Puno
    ❯ wc  -l archivo3
    8 archivo3
    ❯ wc  -w archivo3
    8 archivo3
    ❯ wc  -c archivo3
    42 archivo3
    ❯ du archivo3
    0       archivo3
2. Realice las siguientes peticiones como parte de la calificación de esta práctica:
    2.1. Cree redireccionando la salida del comando ls los siguientes archivos del directorio Documents o Documentos en un archivo de nombre practica:
    pract01, pract02, pract03, practica, pract01ica, pract02ica, pract03ica
    [Tip. Asegúrese de tener los archivos mensionado antes del redireccionamiento]
        ❯ cd documents
        ❯ touch pract01 pract02 pract03 pract01ica pract02ica pract03ica
        ❯ cd ..
        ❯ ls Documents && cat pract01 pract02 pract03 pract01ica pract02ica pract03ica >> practica
        pract01  pract01ica  pract02  pract02ica  pract03  pract03ica
    2.2. Adicione al final de practica la salida del comando date.
        ❯ date >> practica
        ❯ cat practica
        pract01 pract02 pract03 pract01ica pract02ica pract03ica
        Fri May  5 13:55:32 +13 2023
    2.3. Enviar un mensaje a un usuario utilizando bloques de comandos.

    2.4. Colocar los archivos cuyo nombre empiece con c del directorio /usr/bin en un archivo llamado binlistado. Utilice redireccionamiento.
        ls bin && ls c* > practica 
        (por revisar)
    2.5. Comparar los archivos pract03 y practica, y coloque el resultado en un archivo llamado practica25.
        ❯ diff pract03 practica > practica25
        ❯ cat practica25
        0a1
        > pract01 pract02 pract03 pract01ica pract02ica pract03ica
    2.6. Buscar “pr” en el archivo pract02
        ❯ grep "pr" pract02
    2.7. Guardar en un archivo practica27 todos los nombres de los archivos que inician con pract0
        ❯ ls pract0*>practica27
        ❯ cat practica27
        pract01
        pract01ica
        pract02
        pract02ica
        pract03
        pract03ica
        practica
        practica25
    2.8. Guardar en un archivo practica28 todos los nombres de los archivos que empiezan con pract0 y son de 7 letras.
        ❯ ls pract0[1-9a-zA-Z]>practica28
        ❯ cat practica28
        pract01
        pract02
        pract03
        pract0B
        pract0a
    2.9. Guardar en un archivo practica29 todos los nombres de los archivos que en la posición 7 tienen el carácter 1 o 2.
        ❯ ls ??????[12]>practica29
        ❯ cat practica29
        pract01
        pract02
    2.10. En un archivo practica210 coloque el calendario de este mes. Use el comando cal.
        ❯ cal > practica210
        ❯ cat practica210
            May 2023
        Su Mo Tu We Th Fr Sa
            1  2  3  4  5  6
        7  8  9 10 11 12 13
        14 15 16 17 18 19 20
        21 22 23 24 25 26 27
        28 29 30 31
    2.11. En un archivo llamado practica211 coloque la fecha de hoy.
        ❯ date>practica211
        ❯ cat practica211
        Fri May  5 23:02:29 +13 2023
    2.12. Busque la palabra “oc” en el archivo practica210
        ❯ grep "oc" practica210
        ❯ cat practica210
            May 2023
        Su Mo Tu We Th Fr Sa
            1  2  3  4  5  6
        7  8  9 10 11 12 13
        14 15 16 17 18 19 20
        21 22 23 24 25 26 27
        28 29 30 31
    2.13. Cree el directorio DIR1 en su home y luego haga un listado del contenido de su home en una sola línea de comando. [Utilice ;].
        ❯ mkdir DIR1; ls -a
        .      Documents  archivo3    binlistado1  pract02     pract0a      practica25  practicademo
        ..     README.md  archivo4    dev          pract02ica  pract0aa     practica27  practicademo2
        .dist  archivo    archivo6    nuevo        pract03     practica     practica28
        .git   archivo1   bin         pract01      pract03ica  practica210  practica29
        DIR1   archivo2   binlistado  pract01ica   pract0B     practica211  practica9
    2.14. Listar el contenido del directorio DIR2 en su home y luego hacer un listado del contenido de su home en una solo línea de comando. [Utilice &&]
        ❯ mkdir DIR2 && cd DIR2 && ls -l && cd .. && ls
        total 0
        DIR1       archivo1  bin          pract01     pract03ica  practica210  practica29
        DIR2       archivo2  binlistado   pract01ica  pract0B     practica211  practica9
        Documents  archivo3  binlistado1  pract02     pract0a     practica25   practicademo
        README.md  archivo4  dev          pract02ica  pract0aa    practica27   practicademo2
        archivo    archivo6  nuevo        pract03     practica    practica28
    2.15. Listar el contenido del directorio DIR3 en su home y luego hacer un listado del contenido de su hombre en una sola línea de comando. [Utilice ||]
        ❯ mkdir DIR3 || cd DIR3 || ls || cd .. || ls
    2.16. En segundo plano coloque en un archivo practica216 el contenido del directorio raíz (carpetas y archivos).
        ❯ sudo ls -a /root > practica216
        ❯ cat practica216
        .
        ..
        .bash_history
        .bashrc
        .config
        .docker
        .local
        .npm
        .profile
        .viminfo
    2.17. Crear con cat el archivo practica217 con los siguientes datos: Uno, Dos, Tres, Cuatro, Cinco.
        ❯ cat > practica217
        Uno, dos, tres, cuatro, cinco
    2.18. Crear con cat el archivo practica218 con los siguientes datos: 12, 15, 20, 40.
        ❯ cat > practica218
        12, 15, 20, 40
    2.19. Concatene los dos archivos anteriores en un archivo llamado practica219.
        ❯ cat practica217 practica218 > practica220
        ❯ cat practica220
        Uno, dos, tres, cuatro, cinco
        12, 15, 20, 40
    2.20. Ordene el archivo practica217 y coloque el resultado en el archivo practica220.
        ❯ sort practica217>practica220
        ❯ cat practica220
        Uno, dos, tres, cuatro, cinco
    2.21. Ordene el archivo practica218 y muestre el contenido.
        ❯ sort practica218
        12, 15, 20, 40
    2.22. Busque la palabra “ar” en todos los archivos de su home.
        grep -r "ar" /home
    2.23. Muestre el números de líneas, palabras, y caracteres del archivo practica220.
        ❯ wc -l -w -c practica220
        1  5 30 practica220
    2.24. Busque el archivo: bash_profile
        ❯ find bash_profile
        find: ‘bash_profile’: No such file or directory
    2.25. Busque el archivo: bash_logout
        ❯ find bash_logout
        find: ‘bash_logout’: No such file or directory
    2.26. En el caso de que en el punto 2.11 tenga un mensaje de error por no poseer los derechos, redireccione el mensaje de error al archivo
    /dev/practica226.
        #No se posee el error
        #opcional error
        ❯ write usuario1 2> archivo226
        ❯ cat archivo226
        write: usuario1 is not logged in
    2.27. Visualice todos los archivos de su directorio home que hayan sido modificados en los últimos 10 días.
        ❯ find * -mtime +9 -ls
    2.28. Cree un archivo llamado practica228 con los siguientes datos: Ana, Ana, Lourdes, Javier, Maria, Maria, Marcos, Sara, Vanesa.
        ❯ cat >practica228
        Ana, Ana, Lourdes, Javier, Maria, Maria, Marcos, Sara, Vanesa
    2.29. En un archivo llamado practica229 coloque aquellos nombres que no se repiten del archivo practica228.
        ❯ uniq practica228>practica229
    2.30. Muestre el contenido del archivo practica229.
        ❯ cat practica229
        Ana,
        Lourdes,
        Javeir,
        Maria,
        Marcos,
        Sara,
        Vanesa
    2.31. En un archivo llamado practica231 coloque aquellos nombres que se repiten del archivo practica228.
        ❯ uniq -d practica228>practica231
    2.32. Muestre el contenido del archivo practica231
        ❯ cat practica231
        Ana,
        Maria,
    2.33. Muestre el tamaño del archivo practica228 en líneas.
        ❯ wc -l practica228
        13 practica228
        #el archivo es el siguiente
        Ana,
        Ana,
        Lourdes,
        Javeir,
        Maria,
        Maria,
        Marcos,
        Sara,
        Vanesa



        sasas
    2.34. Muestre el tamaño del archivo practica228 en megas.
        ❯ du -m practica228
        0       practica228
    2.35. Usando cat ingrese los siguientes datos al archivo practica235, Peru, Tunez, Mexico, Salvador, Argentina, Colombia
    2.36. Verifique que realiza el siguiente comando: $ls |sort –r |head -l
    2.37. Halle dos equivalencias al comando anterior.
    2.38. Agregue al archivo practica228 el archivo practica235