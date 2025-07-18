# open5gs-sepp

![Version: 2.3.0](https://img.shields.io/badge/Version-2.3.0-informational?style=flat-square) ![AppVersion: 2.7.5](https://img.shields.io/badge/AppVersion-2.7.5-informational?style=flat-square)

Helm chart to deploy Open5gs SEPP service on Kubernetes without TLS.

**Homepage:** <https://github.com/gradiant/5g-charts>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| cgiraldo | <cgiraldo@gradiant.org> |  |

## Source Code

* <http://open5gs.org>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | common | 1.x.x |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| args | list | `[]` |  |
| command | list | `[]` |  |
| commonAnnotations | object | `{}` |  |
| commonLabels | object | `{}` |  |
| config.logLevel | string | `"info"` |  |
| config.sbi.client.nrf.enabled | bool | `false` |  |
| config.sbi.client.nrf.uri | string | `""` |  |
| config.sbi.client.scp.enabled | bool | `true` |  |
| config.sbi.client.scp.uri | string | `""` |  |
| config.sbi.server | string | `nil` |  |
| containerPorts.n32 | int | `7443` |  |
| containerPorts.sbi | int | `7777` |  |
| containerSecurityContext.enabled | bool | `true` |  |
| containerSecurityContext.runAsNonRoot | bool | `true` |  |
| containerSecurityContext.runAsUser | int | `1001` |  |
| customLivenessProbe | object | `{}` |  |
| customOpen5gsConfig | object | `{}` |  |
| customReadinessProbe | object | `{}` |  |
| customStartupProbe | object | `{}` |  |
| dbURI | string | `""` |  |
| extraDeploy | list | `[]` |  |
| extraEnvVars | list | `[]` |  |
| extraEnvVarsCM | string | `""` |  |
| extraEnvVarsSecret | string | `""` |  |
| extraVolumeMounts | list | `[]` |  |
| extraVolumes | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.imagePullSecrets | list | `[]` |  |
| global.imageRegistry | string | `""` |  |
| global.storageClass | string | `""` |  |
| hostAliases | list | `[]` |  |
| image.debug | bool | `false` |  |
| image.digest | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.pullSecrets | list | `[]` |  |
| image.registry | string | `"docker.io"` |  |
| image.repository | string | `"gradiant/open5gs"` |  |
| image.tag | string | `"2.7.2"` |  |
| initContainers | list | `[]` |  |
| kubeVersion | string | `""` |  |
| lifecycleHooks | object | `{}` |  |
| livenessProbe.enabled | bool | `true` |  |
| livenessProbe.failureThreshold | int | `5` |  |
| livenessProbe.initialDelaySeconds | int | `600` |  |
| livenessProbe.periodSeconds | int | `10` |  |
| livenessProbe.successThreshold | int | `1` |  |
| livenessProbe.timeoutSeconds | int | `5` |  |
| mongodb.auth.enabled | bool | `false` |  |
| mongodb.enabled | bool | `false` | set to 'false' to disable automatically deploying dependent charts |
| nameOverride | string | `""` |  |
| namespaceOverride | string | `""` |  |
| nodeAffinityPreset.key | string | `""` |  |
| nodeAffinityPreset.type | string | `""` |  |
| nodeAffinityPreset.values | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| podAffinityPreset | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podAntiAffinityPreset | string | `"soft"` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.enabled | bool | `true` |  |
| podSecurityContext.fsGroup | int | `1001` |  |
| priorityClassName | string | `""` |  |
| readinessProbe.enabled | bool | `true` |  |
| readinessProbe.failureThreshold | int | `5` |  |
| readinessProbe.initialDelaySeconds | int | `30` |  |
| readinessProbe.periodSeconds | int | `5` |  |
| readinessProbe.successThreshold | int | `1` |  |
| readinessProbe.timeoutSeconds | int | `1` |  |
| replicaCount | int | `1` |  |
| resources.limits | object | `{}` |  |
| resources.requests | object | `{}` |  |
| schedulerName | string | `""` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.automountServiceAccountToken | bool | `true` |  |
| serviceAccount.create | bool | `false` |  |
| serviceAccount.name | string | `""` |  |
| services.n32.annotations | object | `{}` |  |
| services.n32.clusterIP | string | `""` |  |
| services.n32.externalTrafficPolicy | string | `"Cluster"` |  |
| services.n32.extraPorts | list | `[]` |  |
| services.n32.loadBalancerIP | string | `""` |  |
| services.n32.loadBalancerSourceRanges | list | `[]` |  |
| services.n32.nodePorts.n32 | string | `""` |  |
| services.n32.ports.n32 | int | `7443` |  |
| services.n32.sessionAffinity | string | `"None"` |  |
| services.n32.sessionAffinityConfig | object | `{}` |  |
| services.n32.type | string | `"ClusterIP"` |  |
| services.sbi.annotations | object | `{}` |  |
| services.sbi.clusterIP | string | `""` |  |
| services.sbi.externalTrafficPolicy | string | `"Cluster"` |  |
| services.sbi.extraPorts | list | `[]` |  |
| services.sbi.loadBalancerIP | string | `""` |  |
| services.sbi.loadBalancerSourceRanges | list | `[]` |  |
| services.sbi.nodePorts.sbi | string | `""` |  |
| services.sbi.ports.sbi | int | `7777` |  |
| services.sbi.sessionAffinity | string | `"None"` |  |
| services.sbi.sessionAffinityConfig | object | `{}` |  |
| services.sbi.type | string | `"ClusterIP"` |  |
| sessionAffinity | string | `"None"` |  |
| sidecars | list | `[]` |  |
| startupProbe.enabled | bool | `false` |  |
| startupProbe.failureThreshold | int | `5` |  |
| startupProbe.initialDelaySeconds | int | `600` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `5` |  |
| tolerations | list | `[]` |  |
| topologySpreadConstraints | list | `[]` |  |
| updateStrategy.type | string | `"RollingUpdate"` |  |

