---
title: "7. Tools"
weight: 7
sectionnumber: 7
---

In this Lab you are going to learn about different [application source tools](https://argoproj.github.io/argo-cd/user-guide/application_sources/).


## Tools

As mentioned in the [introduction](../) Argo CD supports many different formats in which the Kubernetes manifests can be defined:

* [kustomize](https://kustomize.io/) applications
* [helm](https://helm.sh/) charts
* [ksonnet](https://github.com/ksonnet/ksonnet) applications (deprecated)
* [jsonnet](https://jsonnet.org/) files
* Plain directory of YAML/json manifests
* Any custom config management tool configured as a config management plugin

So far you have been using **plain YAML** manifest in the previous labs.

{{% alert title="Warning" color="secondary" %}}
Argo CD provides a mechanism to override the parameters of Argo CD applications. [The Argo CD parameter overrides](https://argoproj.github.io/argo-cd/user-guide/parameters/) feature is provided mainly as a convenience to developers and is intended to be used in dev/test environments, vs. production environments.

Many consider this feature as anti-pattern to GitOps. So only use this feature when no other option is available!
{{% /alert %}}

You are now going to deploy an application in the different formats.

You can also find additional examples [here](https://github.com/argoproj/argocd-example-apps).
