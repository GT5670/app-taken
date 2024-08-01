# Trusted Application Pipeline Software Template

This application, **app-taken**, was created from a Trusted Application Pipeline Software Template.

The software templates create a new source and gitops deployment repositories with a sample source application. 

## Repositories

apiVersion: tekton.dev/v1
kind: PipelineRun
metadata:
  name: app-taken-on-push
  annotations:
    pipelinesascode.tekton.dev/on-event: "[push]"
    pipelinesascode.tekton.dev/on-target-branch: "[main]"
    pipelinesascode.tekton.dev/max-keep-runs: "2"
    pipelinesascode.tekton.dev/pipeline: "https://raw.githubusercontent.com/redhat-appstudio/tssc-sample-pipelines/main/pac/pipelines/docker-build-rhtap.yaml"
    pipelinesascode.tekton.dev/task-0: "https://raw.githubusercontent.com/redhat-appstudio/tssc-sample-pipelines/main/pac/tasks/init.yaml"
    pipelinesascode.tekton.dev/task-1: "https://raw.githubusercontent.com/redhat-appstudio/tssc-sample-pipelines/main/pac/tasks/git-clone.yaml"
    pipelinesascode.tekton.dev/task-2: "https://raw.githubusercontent.com/redhat-appstudio/tssc-sample-pipelines/main/pac/tasks/buildah-rhtap.yaml"
    pipelinesascode.tekton.dev/task-3: "https://raw.githubusercontent.com/redhat-appstudio/tssc-sample-pipelines/main/pac/tasks/acs-image-check.yaml"
  labels:
    argocd/app-name: app-taken
    janus-idp.io/tekton: app-taken
    backstage.io/kubernetes-id: app-taken
    backstage.io/kubernetes-namespace: rhtap-app
    app.kubernetes.io/part-of: app-taken
spec:
  params:
    - name: dockerfile
      value: docker/Dockerfile
    - name: git-url
      value: '{{repo_url}}'
    - name: image-expires-after
      value: 5d
    - name: output-image
      value: quay.io/rhdeveldocs/app-taken:{{revision}}
    - name: path-context
      value: .
    - name: revision
      value: '{{revision}}'



  This file is for tekton and it has links to multiple pipeline tasks, including

* docker-build-rhtap.yaml
* init.yaml
* git-clone.yaml
* buildah-rhtap.yaml
* acs-image-check.yaml
