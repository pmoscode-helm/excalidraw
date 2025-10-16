# excalidraw Helm Chart
![Version: 0.18.0](https://img.shields.io/badge/Version-0.18.0-informational?style=flat-square)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/excalidraw)](https://artifacthub.io/packages/search?repo=excalidraw)

From https://github.com/excalidraw/excalidraw:
> An open source virtual hand-drawn style whiteboard. Collaborative and end-to-end encrypted.

## Get Repo Info

    helm repo add my-excalidraw https://pmoscode-helm.github.io/excalidraw/
    helm repo update

## Install chart

    helm install [RELEASE_NAME] my-excalidraw/excalidraw

The command deploys excalidraw on the Kubernetes cluster in the default configuration.

See configuration below.

See [helm install](https://helm.sh/docs/helm/helm_install/) for command documentation.

## Uninstall Chart

    helm uninstall [RELEASE_NAME]

This removes all the Kubernetes components associated with the chart and deletes the release.

See [helm uninstall](https://helm.sh/docs/helm/helm_uninstall/) for command documentation.

## Upgrading Chart

    helm upgrade [RELEASE_NAME] [CHART] --install

See [helm upgrade](https://helm.sh/docs/helm/helm_upgrade/) for command documentation.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| collabServer.enabled | bool | `false` |  |
| collabServer.image.pullPolicy | string | `"IfNotPresent"` |  |
| collabServer.image.repository | string | `"pmoscode/excalidraw-collab-server"` |  |
| collabServer.image.tag | string | `"1.0.0"` |  |
| collabServer.podAnnotations | object | `{}` |  |
| collabServer.podSecurityContext | object | `{}` |  |
| collabServer.resources | object | `{}` |  |
| collabServer.securityContext | object | `{}` |  |
| collabServer.service.port | int | `3002` |  |
| collabServer.service.type | string | `"ClusterIP"` |  |
| excalidraw.customCollabServerURL | string | `"http://localhost:3002"` |  |
| excalidraw.hardCodedCollabServerURL | string | `"https://oss-collab.excalidraw.com"` |  |
| excalidraw.image.pullPolicy | string | `"IfNotPresent"` |  |
| excalidraw.image.repository | string | `"pmoscode/excalidraw"` |  |
| excalidraw.image.tag | string | `""` |  |
| excalidraw.ingress.annotations | object | `{}` |  |
| excalidraw.ingress.className | string | `""` |  |
| excalidraw.ingress.enabled | bool | `false` |  |
| excalidraw.ingress.host | string | `"chart-example.local"` |  |
| excalidraw.ingress.path | string | `"/"` |  |
| excalidraw.ingress.tls | object | `{}` |  |
| excalidraw.ingress.type | string | `"ImplementationSpecific"` |  |
| excalidraw.podAnnotations | object | `{}` |  |
| excalidraw.podSecurityContext | object | `{}` |  |
| excalidraw.resources | object | `{}` |  |
| excalidraw.securityContext | object | `{}` |  |
| excalidraw.service.port | int | `80` |  |
| excalidraw.service.type | string | `"ClusterIP"` |  |
| fullnameOverride | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| pmoscode | <info@pmoscode.de> | <https://pmoscode.de> |
