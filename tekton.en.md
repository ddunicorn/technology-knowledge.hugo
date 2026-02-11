---
title: "tekton"
draft: false
showToc: false
showReadingTime: false
showWordCount: false
ShowPostNavLinks: false
summary: "CI/CD pipelines as Kubernetes objects"
tags:
  - tekton
  - kubernetes
  - foss
---

[tekton](https://tekton.dev) implements CI/CD pipelines (triggered, sequential, conditional, and parametrized execution of containers) on Kubernetes. Tekton is abstract and flexible, pipelines and their building blocks can be re-used and [shared](https://github.com/tektoncd/catalog).

- Pipelines consist of Tasks (e.g. git clone) which define sequential Steps. Data can be passed between Steps and Tasks.
- A PipelineRun is one execution of a Pipeline and defines TaskRuns; it provides runtime dependencies (e.g. Kubernetes volumes and service accounts) to the Pipeline and Tasks; it has a state.
- EventListeners can create PipelineRuns and TaskRuns based on parametrized Templates. Bindings define how event data (e.g. from an HTTP request body) is used as Template arguments.

tekton is FOSS and a Graduated [Continuous Delivery Foundation](https://cd.foundation/) project.
