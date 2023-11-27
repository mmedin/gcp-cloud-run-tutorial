Español? [Aquí](README.es.md)

# GCP Cloud Run tutorial

Desplegar un servicio Node.js en Cloud Run

## Pre-requisitos

Necesitamos la herramienta de línea de comandos de Google Cloud `gcloud`, disponible para instalar en https://cloud.google.com/sdk/docs/install.

Si no fue hecho ya, puede ser necesario inicializar tal herramienta:

```bash
gcloud init
```

Es recomendable crear un proyecto nuevo dentro de GCP, ya que al final de estas pruebas es más fácil limpiar todos los recursos creados mediante la sencilla eliminación del proyecto. Es más dificultosa la limpieza si trabajamos sobre un proyecto que tienen otros recursos que no podemos eliminar.

Una vez creado, apuntar `gcloud` a tal proyecto:

```bash
gcloud config set project PROJECT_ID
```

## La aplicación

Este repositorio contiene una aplicación "hola mundo" básica, a los efectos de probar el despliegue y ejecución de la misma en Cloud Run. Se trata de una app NodeJS, pero no es necesario tener Node, ni NPM ni ninguna herramienta relacionada instalado localmente, ya que el proceso de build sucede gracias a servicios dentro de GCP.

## Despliegue

Una vez clonado el presente repositorio, ubicados dentro de la carpeta del proyecto ejecutamos el siguiente comando:

```bash
gcloud run deploy
```

Esto es todo lo que hace falta para preparar un container que incluya la aplicación y sus dependencias, subir el container a la registry y finalmente desplegarlo en Cloud Run. Es por ello que tampoco es necesario contar con Docker localmente. Como parte del proceso habrá que contestar las preguntas que `gcloud` vaya presentando.

## Limpieza

Sencillamente eliminar el proyecto creado al principio.
