# qiot-helm-charts

This Repository contains all necessary helm charts to install the whole qiot covid19 project onto your own Kubernetes / OpenShift Server.

This is currently work in progress. So please stay tuned.

## Content
Right now this repository contains only files to install the openshift-pipelines and openshift-gitops operator plus the pipelines from the qiot-project/qiot-covid19-datahub-pipelines repository

## Installation
To test and install this Helm Chart your user must have operator installation rights in the OpenShift cluster (otherwise the two Operators are not able to be installed).

Then create a new project where you want the Chart to be installed in and execute the following steps:

```bash
$> oc login -u kubeadmin ... 
$> oc new-project qiot-covid19
$> git clone ...
$> helm install qiot-covid19-datahub ./qiot-helm-charts --values ./qiot-helm-charts/values.yaml


```
