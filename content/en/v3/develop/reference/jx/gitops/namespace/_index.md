---
title: jx gitops namespace
linktitle: namespace
type: docs
description: "Updates all kubernetes resources in the given directory to the given namespace ***Aliases**: ns*"
aliases:
  - jx-gitops_namespace
---

### Usage

```
jx gitops namespace
```

### Synopsis

Updates all kubernetes resources in the given directory to the given namespace

### Examples

  ```bash
  # updates the namespace of all the yaml resources in the given directory
  jx-gitops namespace -n cheese --dir .
  
  
  # sets the namespace property to the name of the child directory inside of 'config-root/namespaces'
  # e.g. so that the files 'config-root/namespaces/cheese/*.yaml' get set to namespace 'cheese'
  # and 'config-root/namespaces/wine/*.yaml' are set to 'wine'
  jx-gitops namespace --dir-mode --dir config-root/namespaces

  ```
### Options

```
      --cluster-dir string        the directory to recursively look for the *.yaml or *.yml files
      --dir string                the directory to recursively look for the namespaced *.yaml or *.yml files to set the namespace on (default ".")
      --dir-mode                  assumes the first child directory is the name of the namespace to use
  -h, --help                      help for namespace
      --invert-selector           inverts the effect of selector to exclude resources matched by selector
  -k, --kind stringArray          adds Kubernetes resource kinds to filter on. For kind expressions see: https://github.com/jenkins-x/jx-helpers/tree/master/docs/kind_filters.md
      --kind-ignore stringArray   adds Kubernetes resource kinds to exclude. For kind expressions see: https://github.com/jenkins-x/jx-helpers/tree/master/docs/kind_filters.md
  -n, --namespace string          the namespace to modify the resources to
      --selector stringToString   adds Kubernetes label selector to filter on, e.g. --selector app=pusher-wave,heritage=Helm (default [])
      --selector-target string    sets which path in the Kubernetes resources to select on instead of metadata.labels.
```



### Source

[jenkins-x-plugins/jx-gitops](https://github.com/jenkins-x-plugins/jx-gitops)
