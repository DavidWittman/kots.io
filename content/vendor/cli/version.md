---
date: 2019-10-09
linktitle: "Version"
title: "Version"
weight: 90150
---

Opens a proxy so you can connect to the admin console from your machine. Additionally, you may use `kots admin-console upgrade` to upgrade the admin console to the latest version. Requires a running KOTS application with the Admin Console (kotsadm).

### Usage
```bash
kubectl kots admin-console [flags]
kubectl kots admin-console upgrade [flags]
```

* _If `upgrade` is not specified, this command opens a proxy to the admin console. Otherwise, it upgrades the admin console to the latest version._

| Flag                 | Type | Description |
|:----------------------|------|-------------|
| `-h, --help`   |  |          help for admin-console |
| `--kubeconfig` | string |  the kubeconfig to use _(default is $KUBECONFIG. If unset, then $HOME/.kube/config)_ |
| `-n, --namespace` | string |   the namespace where the admin console is running _(default "default")_ |

### Examples
```bash
kots admin-console --namespace kots-sentry
kots admin-console upgrade --namespace kots-sentry
```