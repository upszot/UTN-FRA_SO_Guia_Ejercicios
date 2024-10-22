# LVM

- [ ] Ejercicio 1:
    - Agregar 2 Discos (1G ,  3G  )
    -  Crear la estructura de directorios para los puntos de montaje con 1 solo comando
    - Crear los VG `vg_multimedia` `VG_datos`
    - Crear los siguientes LV dentro del VG anterior.

    | VG | LV | Tamaño | Punto de Montaje |
    | --- | --- | --- | --- |
    | vg_multimedia | lv_peliculas | 1G | /datos/peliculas |
    | vg_multimedia | lv_series | 1G | /datos/series |
    | vg_datos | lv_swap | 512M | Montar como swap |
    | vg_datos | lv_docker | 10M | /var/lib/docker |


- [ ] Ejercicio 2:
    - Ejecutar: `dd if=/dev/zero of=/datos/peliculas/peli_01.mkv bs=1M count=700`
    - Ejecutar: `dd if=/dev/zero of=/datos/peliculas/peli_02.mkv bs=1M count=500`
    - Analizar el error
    - Agrandar el `lv_peliculas` en 512M
    - volver a ejecutar el 2do dd
    - Validar Resultados

- [ ] Ejercicio 3:
    - Ejecutar `docker run hello-world` 
    - Solucionar los problemas que se presenten 


<details>
    <summary>&emsp; <Mostrar/Ocultar> - <b>!!! Spoiler Alert !!!</b>  ...Pistas...</summary>
    <div>
        Los siguientes Archivos y Comandos están relacionados con la resolución de los Ejercicios:
        <ul style="padding-left: 20px; font-style: italic;">
            <li>Archivos: `/dev/zero`, `/proc/swaps`, `/etc/fstab`</li>
            <li>Comandos: `fdisk`, `lvcreate`, `pvcreate`, `vgcreate`</li>
            <li>Comandos: `sudo`, `ls`, `dd`, `docker`</li>
            <li>Comandos: `du`, `df`, `lsblk`, `usermod`</li>
            <li>Comandos: `systemctl`, `mkdir`, `mkfs`, `mkswap`</li>
            <li>Comandos: `swapon`, `free`, `mount`, `partprobe`</li>
            <li>Comandos: `tee`, `journalctl`</li>
        </ul>
        Siempre es preferible la ejecución de un comando, por sobre la Modificacion manual de un archivo.
    </div>
</details>

