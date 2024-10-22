# Bash Scripting
> Practica de bash-script. </br>
> Aplicando ejercicios anteriores.



- [ ] Ejercicio 1:
    - Crear el usuario `UserControl` 
    - Grupos Secundarios
        - `GrupoA` ,`GrupoB`, `GrupoC`
    - Directorio Base-Home `/export/home`
    > Eso quiere decir que el $HOME del usuario estara dentro de dicho directorio base. (ver man)

- [ ] Ejercicio 2:
    - Completar el siguiente script
    - El mismo recibira 3 parametros, como se describe dentro del template.
        - 1erParametro = Usuario al cual se le obtendran los grupos secundarios
        - 2doParametro = Path del Directorio Base para el Home del usuario
        - 3erParametro = Nombre del usuario que se creara
    
    - Tareas a realizar dentro del script:
        - Obtener Grupos Secundarios del usuario (1erParametro)
        - Crear usuario (3erParametro) con los mismos grupos Secundarios del usuario del (1erParametro)
    - Modo de ejecucion:
```sh
crea_user_mismos_grupos.sh  UserControl  /export/home  UserTest
```
<ul style="padding-left: 80px; font-style: italic;">
    <li>Script</li>
</ul>


```sh
cat < EOF | sudo tee /usr/local/bin/crea_user_mismos_grupos.sh

#!/bin/bash

#Recibo usuario al que le obtendre los grupos secundarios
USER_GET_GRUPOS=$1
#Recibo Directorio Base donde estaran los home de los usuarios
BASE_DIR=$2
#Usuario a crear
NEW_USER=$3


#---------- MODIFICAR ----------#
#Cargar el Listado de grupos secundarios del usuario pasado por parametro
LISTA_GRUPOS="Grupo_ejemplo1,Grupo_ejemplo2"
#---------- MODIFICAR ----------#


sudo useradd -m -s /bin/bash -b $BASE_DIR -G $LISTA_GRUPOS $NEW_USER

EOF
sudo chmod +x /usr/local/bin/crea_user_mismos_grupos.sh
```


<details>
    <summary>&emsp; <Mostrar/Ocultar> - <b>!!! Spoiler Alert !!!</b>  ...Pistas...</summary>
    <div>
        Los siguientes Comandos están relacionados con la resolución de los Ejercicios:
        <ul style="padding-left: 20px; font-style: italic;">
            <li>Comandos: `grep`, `awk`, `tee`, `sudo`, `sed`</li>
            <li>scripting: `if`, `for`</li>
        </ul>
    </div>
    <div>
        - Hay 4 formas de resolver el ejercicio:
        <ul style="padding-left: 40px; font-style: italic;">
            <li>Puedo usar un bucle `for` con un `if` para cargar el Listado</li>
            <li>Puedo usar solamente `awk` (ver sub y gsub dentro de awk)</li>
            <li>Puedo usar solamente `awk` (ver if y for dentro de awk)</li>
            <li>Puedo usar la combinacion de `awk` y `sed`</li>        
        </ul>
    </div>
</details>

