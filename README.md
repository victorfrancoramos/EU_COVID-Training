# EU_COVID-Training

Entrenamiento de modelo de detección de COVID

Renombrar extensión de .JPEG a .JPG (Linux): 

`rename -v -n .jpeg .jpg *.jpeg` _#Visualizar antes de ejecutar_

`rename -v .jpeg .jpg *.jpeg` _#Ejecutar_

Para hacerlo de forma recursiva:

`shopt -s globstar`

`rename -v .jpeg .jpg **` _#Visualizar antes de ejecutar_

`rename -v -n .jpeg .jpg **` _#Ejecutar_

Cambiar formato de archivos de PNG a JPG usando magick (herramienta gratuita de Linux):

`for image in *.png; do magick "$image" "${image%.*}.jpg"; done`

Esta utilidad también se puede utilizar para escalar todas la imágenes para que tengan un mismo tamaño:
[Command-line Tools: Convert](https://imagemagick.org/script/convert.php)

`magick mogrify -resize 800x700 *.jpg`
