---
title: jx gitops helm mirror
linktitle: mirror
type: docs
description: "Mirror a helm repository"
aliases:
  - jx-gitops_helm_mirror
---

### Usage

```
jx gitops helm mirror
```

### Synopsis

Mirrors a set of remote Helm repositories specified locally in charts/repositories.yml to a remote git repository

### Examples

  ```bash
  # Mirror all Helm repositories defined in charts/repositories.yml to a default github pages branch
  jx-gitops mirror --url=https://github.com/example/charts.git --no-push=false
  
  # Run the mirror command, ignoring unused repositories
  %!s(MISSING) mirror --url=https://github.com/example/charts.git --no-push=false --exclude=bitnami

  ```
### Options

```
  -b, --branch string         the git branch to clone the repository (default "gh-pages")
  -d, --dir string            the directory which contains the charts/repositories.yml file (default ".")
  -x, --exclude stringArray   the helm repositories to exclude from mirroring (default [jenkins-x,jx3])
      --git-kind string       the kind of git server to connect to
      --git-server string     the git server URL to create the scm client
      --git-token string      the git token used to operate on the git repository. If not specified it's loaded from the git credentials file
      --git-username string   the git username used to operate on the git repository. If not specified it's loaded from the git credentials file
  -h, --help                  help for mirror
  -m, --message string        the commit message (default "chore: upgrade mirrored charts")
      --no-push               disables pushing changes back to the git repository (default true)
  -u, --url string            the git URL of the repository to mirror the charts into
```



### Source

[jenkins-x-plugins/jx-gitops](https://github.com/jenkins-x-plugins/jx-gitops)
