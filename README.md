# Service Post

![version](https://img.shields.io/badge/version-1.0.3-blue) ![version](https://img.shields.io/badge/ubuntu-18.04.5LTS-red)   ![version](https://img.shields.io/badge/python-3.6-green) 

Este servicio pertenece a el módulo de inteligencia artificial, su función principal es gestionar las imágenes a la plataforma [SOLFIX Smart City](http://scityfrontend.azurewebsites.net).  

Para comenzar este módulo hace uso de librerías de python, entre ellas `multiprocessing` para las gestión y el procesado de las distintas imágenes de cada una de las cámaras, estas son subidas al gestor de archivos de azure haciendo uso de la librería `azure-storage-blob` en el que se consultan las imágenes y se visualizan en la plataforma mencionada anteriormente.

## Pre-requisitos
Esta version es compatible con Python 3.6 o superior, los requisitos para el correcto funcionamiento de este módulo son:
- requests 
- xmltodict 
- pyodbc 
- azure-storage-blob 
- python-dateutil

Tambien es necesario aclarar que el servicio de delete depende de otros scripts que no se encuentran en el directorio actual.

## Estructura del Proyecto

A continuacion esta la representacion de la estructura del proyecto y las rutas de los cuales depende el servicio de delete.

```
Inteligenciaartificial_py
├── config
│   └── config.py
├── funciones
│   ├── common
│   │   └── funciones.py
│   └── servicios
│       └── delete_funciones.py
├── servicios
│   ├── delete  <── directorio actual
│   │   ├── main.py  
│   │   ├── README.md
│   │   └── requirements.txt
│   ├── post
│   ├── report
│   ├── streaming
│   └── yolo
├── sql
│   ├── queries.py
│   └── service_queries.py  
├── test
├── .gitignore
└── README.md 
```
Para ver la estructura del completa puede volver a la [raiz del proyecto](https://gitlab.com/AirisDesarrollosColombia/smart-city/inteligenciaartificial_py/-/tree/Develop)

## Instalacion
Puede instalarlo a través de un solo comando, use:
```
pip install requests xmltodict pyodbc azure-storage-blob python-dateutil
```
También puede hacerlo usando el archivo de configuración, para eso antes debe estar en el directorio donde se encuentra este archivo, use el siguiente comando:

```
pip install -r requirements.txt
```
## Estado del proyecto
En proceso, actualmente funcionando [SOLFIX Smart City](http://scityfrontend.azurewebsites.net).
