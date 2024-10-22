# Filtrado de datos


- [ ] Ejercicio 1:
    - Desde su Usuario, Con tecnicas de Herr-Doc generar un archivo (owner=root) con la siguiente informacion.
    ```sh
    A1  A2  A3
    B1,B2,B3
    C1  C2,C3
    D1  D2 D3 D4 D..n
    ```

- [ ] Ejercicio 2:
    - Usando los comandos `grep` y `awk`
        - Filtrar para que solamente se muestre el texto de la columna 2 de la linea 1
        - Filtrar para que solamente se muestre el texto de la columna 2 de la linea 2
        - Filtrar para que solamente se muestre la palabra C2
        - Mostrar todas las columnas de la linea D descartando la 1er columna (hacer de cuenta que se desconoce la cantidad de columnas que existen..)


<details>
    <summary>&emsp; <Mostrar/Ocultar> - <b>!!! Spoiler Alert !!!</b>  ...Pistas...</summary>
    <div>
        Los siguientes Comandos están relacionados con la resolución de los Ejercicios:
        <ul style="padding-left: 20px; font-style: italic;">
            <li>Comandos: `grep`, `awk`, `tee`, `sudo`</li>
        </ul>
    </div>
    <div>
        <ul style="padding-left: 40px; font-style: italic;">
            <li>Con awk se puede asignar un valor a una columna</li>
            <li>Para separar acciones dentro del awk se puede usar ;</li>
            <li>Ejemplo: awk '{Accion1 ; Accion2}'</li>        
        </ul>
    </div>
</details>

