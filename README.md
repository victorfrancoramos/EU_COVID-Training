# EU_COVID-Training

Entrenamiento de modelo de detección de COVID

COVIDx Dataset: [https://github.com/lindawangg/COVID-Net/blob/master/docs/COVIDx.md](https://github.com/lindawangg/COVID-Net/blob/master/docs/COVIDx.md)

El conjunto de datos COVIDx actual puede descargarse del siguiente sitio de código abierto:
* https://www.kaggle.com/andyczhao/covidx-cxr2?select=competition_test

O puede construirse manualmente utilizando los siguientes conjuntos de datos de radiografía de tórax de código abierto:
* https://github.com/ieee8023/covid-chestxray-dataset
* https://github.com/agchung/Figure1-COVID-chestxray-dataset
* https://github.com/agchung/Actualmed-COVID-chestxray-dataset
* https://www.kaggle.com/tawsifurrahman/covid19-radiography-database
* https://www.kaggle.com/c/rsna-pneumonia-detection-challenge (original en: https://nihcc.app.box.com/v/ChestXray-NIHCC)
* https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=70230281
* https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=89096912
* https://bimcv.cipf.es/bimcv-projects/bimcv-covid19/

* Renombrar extensión de .JPEG a .JPG (Linux): 

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
