# .dotfiles

Mis archivos de configuración del sistema personalizados.

## Dependencias

- Git

## Uso

En primer lugar incorporamos el siguiente alias al shell que estemos usando:

`alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'`

Clonamos como *bare repository* (bare flag activada) el repositorio.

`git clone --bare https://github.com/joseantoniols1212/dotfiles.git $HOME/.dotfiles`

Hacemos una copia de seguridad de los archivos de configuración por defecto y hacemos *checkout* para desplegar nuestros archivos de configuración.

`dotfiles checkout`

Finalmente ejecutamos el siguiente comando para evitar que *Git* nos informe delos archivos sin seguimiento:

`dotfiles config --local status.showUntrackedFiles no`

## TODO

[] Scrip de instalación
[] Hacer que el scrip de instalación haga copia de seguridad de los archivos de configuración por defecto
[] Documentar todos los programas y dependencias
