---
title: "tekton"
draft: false
showToc: false
showReadingTime: false
showWordCount: false
ShowPostNavLinks: false
summary: "CI/CD Pipelines als Kubernetes Objekte definieren"
tags:
  - tekton
  - kubernetes
  - foss
---

Tekton implementiert CI/CD-Pipelines (getriggerte, sequentielle, bedingte und parametrisierte Ausführung von Containern) auf Kubernetes. Tekton ist abstrakt und flexibel; Pipelines und ihre Bausteine können wiederverwendet und [geteilt](https://github.com/tektoncd/catalog) werden.

- Pipelines bestehen aus Tasks (z. B. git clone), die sequentielle Steps definieren. Daten können zwischen Steps und Tasks weitergegeben werden.
- Ein PipelineRun ist eine einzelne Ausführung einer Pipeline und definiert TaskRuns. Er stellt der Pipeline und den Tasks Laufzeit-Abhängigkeiten (z. B. Kubernetes Volumes und Service-Accounts) zur Verfügung und besitzt einen Zustand.
- EventListeners können PipelineRuns und TaskRuns aus parametrisierten Templates erstellen. Bindings definieren, wie Event-Daten (zB. aus einem HTTP-Request-Body) als Template-Argumente verwendet werden.

Tekton ist FOSS und ein Graduated project der Continuous Delivery Foundation.