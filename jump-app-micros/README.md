# Jump App Micros Chart

## Introduction

*Jump App Micros* chart deploys Jump App's microservices in a specific namespace generating the following elements:

- Deployments
- Services
- Routes
- Service Mesh Objects when this feature is activated (Gateways, VirtualServices, DestinationRules, etc)

On the other hand, it is possible to manage multiple microservices versions in order to integrate blue-green deployment strategy.

## Install

- Install Helm Chart

```$bash
$ helm install jump-app-dev-1 . --namespace jump-app-dev --create-namespace
$ helm install jump-app-pre-1 . --namespace jump-app-pre --create-namespace
$ helm install jump-app-pro-1 . --namespace jump-app-pre --create-namespace
```

- Install Helm Chart applying objects in kubernetes

```$bash
$ helm template . --debug | oc apply -f -
```

## Local Tests

- Lint

```$bash
$ helm lint
```

- Dry run installations

```$bash
$ helm install jump-app-test-1 . --dry-run --debug --namespace test-dev --create-namespace
```

- Render templates Locally

```$bash
$ helm template . --debug
```

## Author Information

Asier Cidon

asier.cidon@gmail.com