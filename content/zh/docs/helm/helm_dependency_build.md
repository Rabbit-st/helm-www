---
title: "Helm依赖构建"
---

## helm dependency build

基于Chart.lock文件重新构建charts/目录

### 简介

从Chart.lock构建输出到charts/目录

该构建是用来将chart的依赖项重建为锁定文件中的指定状态。就像'helm dependency update'一样并不会调整依赖状态。

如果没找到锁定文件，'helm dependency build'映射到'helm dependency update'

```shell
helm dependency build CHART [flags]
```

### 可选项

```shell
  -h, --help             help for build
      --keyring string   keyring containing public keys (default "~/.gnupg/pubring.gpg")
      --skip-refresh     do not refresh the local repository cache
      --verify           verify the packages against signatures
```

### 从父命令继承的命令

```shell
      --debug                       enable verbose output
      --kube-apiserver string       the address and the port for the Kubernetes API server
      --kube-as-group stringArray   group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --kube-as-user string         username to impersonate for the operation
      --kube-ca-file string         the certificate authority file for the Kubernetes API server connection
      --kube-context string         name of the kubeconfig context to use
      --kube-token string           bearer token used for authentication
      --kubeconfig string           path to the kubeconfig file
  -n, --namespace string            namespace scope for this request
      --registry-config string      path to the registry config file (default "~/.config/helm/registry/config.json")
      --repository-cache string     path to the file containing cached repository indexes (default "~/.cache/helm/repository")
      --repository-config string    path to the file containing repository names and URLs (default "~/.config/helm/repositories.yaml")
```

### 请参阅

* [helm dependency](helm_dependency.md) - 管理chart依赖
