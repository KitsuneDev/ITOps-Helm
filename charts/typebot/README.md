# typebotio

A Helm chart for typebotio

## Installing the Chart

To install the chart with the release name `my-release`:

```bash
# Standard Helm install
$ helm install  my-release typebotio

# To use a custom namespace and force the creation of the namespace
$ helm install my-release --namespace my-namespace --create-namespace typebotio

# To use a custom values file
$ helm install my-release -f my-values.yaml typebotio
```

See the [Helm documentation](https://helm.sh/docs/intro/using_helm/) for more information on installing and managing the chart.

## Configuration

The following table lists the configurable parameters of the typebotio chart and their default values.

| Parameter                                                  | Default                        |
| ---------------------------------------------------------- | ------------------------------ |
| `typebot_builder.imagePullPolicy`                          | `IfNotPresent`                 |
| `typebot_builder.replicas`                                 | `1`                            |
| `typebot_builder.repository.image`                         | `baptistearno/typebot-builder` |
| `typebot_builder.repository.tag`                           | `latest`                       |
| `typebot_builder.serviceAccount`                           | ``                             |
| `typebot_db.imagePullPolicy`                               | `IfNotPresent`                 |
| `typebot_db.persistence.db_data.accessMode[0].value`       | `ReadWriteOnce`                |
| `typebot_db.persistence.db_data.enabled`                   | `true`                         |
| `typebot_db.persistence.db_data.size`                      | `1Gi`                          |
| `typebot_db.persistence.db_data.storageClass`              | `-`                            |
| `typebot_db.replicas`                                      | `1`                            |
| `typebot_db.repository.image`                              | `postgres`                     |
| `typebot_db.repository.tag`                                | `16`                           |
| `typebot_db.serviceAccount`                                | ``                             |
| `typebot_redis.imagePullPolicy`                            | `IfNotPresent`                 |
| `typebot_redis.persistence.redis_data.accessMode[0].value` | `ReadWriteOnce`                |
| `typebot_redis.persistence.redis_data.enabled`             | `true`                         |
| `typebot_redis.persistence.redis_data.size`                | `1Gi`                          |
| `typebot_redis.persistence.redis_data.storageClass`        | `-`                            |
| `typebot_redis.replicas`                                   | `1`                            |
| `typebot_redis.repository.image`                           | `redis`                        |
| `typebot_redis.repository.tag`                             | `alpine`                       |
| `typebot_redis.serviceAccount`                             | ``                             |
| `typebot_viewer.imagePullPolicy`                           | `IfNotPresent`                 |
| `typebot_viewer.replicas`                                  | `1`                            |
| `typebot_viewer.repository.image`                          | `baptistearno/typebot-viewer`  |
| `typebot_viewer.repository.tag`                            | `latest`                       |
| `typebot_viewer.serviceAccount`                            | ``                             |


