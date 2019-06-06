# Creating dynamic environments with Helm and Kubernetes

> Code for my talk about dynamic testing environments with Kubernetes and Helm (Original application [here](https://github.com/khaosdoctor/event-sourcing-demo-app))

Link to the [Azure Devops Repository](https://dev.azure.com/lsantos-projects/helm-dynamic-envs/)

![](https://dev.azure.com/lsantos-projects/helm-dynamic-envs/_apis/build/status/Dynamic%20environment%20build)

## Summary

- [Creating dynamic environments with Helm and Kubernetes](#creating-dynamic-environments-with-helm-and-kubernetes)
  - [Summary](#summary)
  - [Usage](#usage)
  - [Charts](#charts)

## Usage

The `backend` and `frontend` folders are the application itself. They both have docker images in my Docker Hub:

- [Frontend image](https://cloud.docker.com/u/khaosdoctor/repository/docker/khaosdoctor/event-sourcing-frontend)
- [Backend image](https://cloud.docker.com/u/khaosdoctor/repository/docker/khaosdoctor/event-sourcing-backend)

You can download those and run separately (bear in mind the backend needs MongoDB in order to work), or, the easier way, run `docker-compose up`.

## Charts

The Helm charts can be used to deploy this application into a Kubernetes cluster with low to zero effort.
