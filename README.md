# Arch-Linux

## Cambiar el lenguaje del sistema 

Pasar del default (EN) al latinomericano (LATAM)

```bash
sudo nano /etc/locale.gen
```
Al ejecutar el anterior comando va aparecer una lista en la que se debera desmarcar la opcion **es_AR.UTF-8 UTF-8** .
Luego hay que actualizar las configuraciones regionales con el siguiente comando.

```bash
locale-gen
```

Despues se debe definir la configuracion regional de todo el sistema con la variable LANG en /etc/locale.conf .

```bash

sudo nano /etc/locale.conf

```
Y hacemos un copy/paste de lo siguiente : **LANG=es_AR.UTF-8** 


### Configuracion del teclado

Debemos establecer la distribucion del teclado  en la ruta /etc/vconsole.conf

```bash
sudo nano /etc/vconsole.conf
```
Y hacemos un copy/paste de lo siguiente : **KEYMAP=la-latin1**

Por ultimo hacemos la configuracion del teclado para Xorg.

```bash
sudo localectl set-x11-keymap latam
```


## Audacious

Reproductor de musica ligero

```bash
sudo pacman -S audacious mpg123

```

