# jenkins-gitops-k8s

This project is the second part of a CI/CD pipeline based on the guide ["Building a Robust CI/CD Pipeline with Jenkins, Docker, Kubernetes, and ArgoCD"](https://sameeradissanayaka.medium.com/building-a-robust-ci-cd-pipeline-with-jenkins-docker-kubernetes-and-argocd-bdcc15a31a2f) by Sameera Dissanayaka. It defines the second pipeline, which is responsible for updating the Kubernetes deployment manifest with the new Docker image tag.

## Differences from the Original Guide

While the original guide provides a comprehensive walkthrough, the `Jenkinsfile` in this repository was slightly modified to handle escaping characters properly. This adjustment ensures the pipeline runs without errors during execution.

## Notes

- Follow the original guide for the overall setup, but refer to this README for any adjustments specific to this repository.
- Ensure the second pipeline is named `updatemanifest` in Jenkins, as required by the first pipeline.

By following these steps, you can successfully implement the second part of the CI/CD pipeline on macOS.

Please refer to the original guide for a complete understanding of the project and the expansion
of the argoCD pipeline.


Id like to note that the original guide just said 
```
Get ArgoCD services: Kubectl get svc -n argocd.
```

With out further explanation, this command will only work if argocd is already installed, you can install argocd using the following command:
```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

After this you can continue with the original guide.

Your argo monitor should look like this
![argo](./img/Screenshot%202025-05-12%20at%205.02.07 PM.png)