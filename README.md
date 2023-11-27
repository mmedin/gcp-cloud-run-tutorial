Español? [Aquí](README.es.md)

# GCP Cloud Run tutorial

Deploy a Node.js service to Cloud Run

## Pre-requisites

We need the Google Cloud command line tool `gcloud`, available for installation at https://cloud.google.com/sdk/docs/install.

If not already done, it may be necessary to initialise such a tool:

```bash
gcloud init
```

It is recommended to create a new project within GCP, as at the end of these tests it is easier to clean up all the resources created by simply deleting the project. It is more difficult to clean up if we work on a project that has other resources that we cannot delete.

Once created, point `gcloud` to such a project:

```bash
gcloud config set project PROJECT_ID
```

## The application

This repository contains a basic "hello world" application, for the purposes of testing deployment and execution on Cloud Run. It is a NodeJS app, but it is not necessary to have Node, NPM or any related tool installed locally, as the build process happens thanks to services within GCP.

## Deployment

Once the present repository has been cloned, located inside the project folder, run the following command:

```bash
gcloud run deploy
```

This is all it takes to prepare a container that includes the application and its dependencies, upload the container to the registry and finally deploy it to Cloud Run. As part of the process you will need to answer the questions that `gcloud` will present to you.

## Cleanup

Simply delete the project created at the beginning.
