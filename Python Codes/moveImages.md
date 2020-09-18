---
sort: 1
---
# Move Images from a folder

## 1. Librerías

Al momento de realizar el codigo se debe primero llamar a las librerías, en este caso se utilizará
la librería OS, SYS y Pandas.

```
import os
import sys
import pandas as pd
```

## 2. Leer el archivo

Luego se debe leer el archivo por medio del **pd.read** para así, luego utilizar como un dataframe.
```
data = pd.read_csv('/home/longino/Documents/DATA/faltantes.csv')
```

## 3. Seleccionar datos específicos del dataframe

```
datos = data.loc[data.ID.astype(str).str.contains('1')].nombre
```

## 4. Convertir los datos en una lista

```
images = datos.tolist()

source = '/home/longino/Documents/DATA/TodoenUNOSinPelo/'

destination = '/home/longino/Documents/DATA/TodoenUNOSinPelo1/'


for img in images:
    #os.rename(source+"mask_"+img, destination+"mask_"+img)
    os.rename(source+img, destination+img)
    #os.rename(source+img+".png", destination+img+".png")
    
print("Dataset folders successfully created by breed name and copied all images in corresponding folders")
```
Documentando, en proceso.
