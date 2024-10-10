---
title: jx admin stop
linktitle: stop
type: docs
description: "stops the currently running boot Job ***Aliases**: suspend*"
aliases:
  - jx-admin_stop
---

### Usage

```
jx admin stop
```

### Synopsis

Stops the currently running boot Job. 

It works by setting spec.suspend=true in the job.

### Options

```
  -b, --batch-mode         Runs in batch mode without prompting for user input
  -h, --help               help for stop
      --log-level string   Sets the logging level. If not specified defaults to $JX_LOG_LEVEL
  -n, --namespace string   the namespace where the boot jobs run. If not specified it will look in: jx-git-operator and jx
  -s, --selector string    the selector of the boot Job pods (default "app=jx-boot")
      --verbose            Enables verbose output. The environment variable JX_LOG_LEVEL has precedence over this flag and allows setting the logging level to any value of: panic, fatal, error, warn, info, debug, trace
```



### Source

[jenkins-x-plugins/jx-admin](https://github.com/jenkins-x-plugins/jx-admin)
