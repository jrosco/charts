# Kubernetes Secret Updater

This is used in conjunction with [Confidant](https://github.com/lyft/confidant), to update the secrets in k8s namespaces.
See the [k8s-secret-updater](https://github.com/fairfaxmedia/k8s-secret-updater) source code, and the [docker image](https://hub.docker.com/r/fairfaxmedia/k8s-secret-updater).

## Configuration Values

| Parameter                   | Default                            | Description |
| --------------------------- | ---------------------------------- | ----------- |
| `secretupdater.host`        | `"0.0.0.0"`                        | ..          |
| `secretupdater.port`        | `"80"`                             | ..          |
| `secretupdater.authMethod`  | `"saml"`                           | ..          |
|                             |                                    |             |
| `confidant.debug`           | `"false"`                          | ..          |
| `confidant.webhookUsername` | `"webhookusername"`                | ..          |
| `confidant.webhookPassword` | `"someSecretPasswordHere"`         | ..          |
| `confidant.serverAuthKey`   | `"some_key_here"`                  | ..          |
|                             |                                    |             |
| `saml.confidantUrlRoot`     | `"https://confidant.example.com/"` | ..          |
|                             |                                    |             |
| `awsDefaultRegion`          | `"ap-southeast-2"`                 | ..          |

### Generic

| Parameter              | Default | Description |
| ---------------------- | ------- | ----------- |
| `replicaCount`         | `1`     | ..          |
| `revisionHistoryLimit` | `5`     | ..          |

### Image

| Parameter          | Default                           | Description |
| ------------------ | --------------------------------- | ----------- |
| `image.repository` | `fairfaxmedia/k8s-secret-updater` | ..          |
| `image.tag`        | `latest`                          | ..          |
| `image.pullPolicy` | `Always`                          | ..          |

### Service

| Parameter               | Default          | Description |
| ----------------------- | ---------------- | ----------- |
| `service.name`          | `secret-updater` | ..          |
| `service.containerPort` | `80`             | ..          |

### Ingress

| Parameter               | Default                      | Description |
| ----------------------- | ---------------------------- | ----------- |
| `ingress.name`          | `secret-updater`             | ..          |
| `ingress.containerPort` | `80`                         | ..          |
| `ingress.host`          | `secret-updater.example.com` | ..          |
| `ingress.annotations`   | `{}`                         | ..          |
