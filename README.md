# Whizlabs Webinar | GitOps - Continuous and Progressive Deployment in AWS EKS | Sivamuthu Kumar

In this session, Let’s take a deep dive into Gitops in AWS EKS and how we can do continuous and progressive deployments in the kubernetes cluster. The key takeaways of the  session:

* Overview of GitOps
* GitOps operator in Kubernetes
* Fluxv2 - Continuous deployment of configuration and App.
* Flagger - Progressive delivery, automated canary deployments 

Slides - [GitOps - Continuous and Progressive Deployment in AWS EKS | Sivamuthu Kumar](./aws-eks-gitops.pdf)

Recorded Video - [GitOps - Continuous and Progressive Deployment in AWS EKS | Sivamuthu Kumar](https://www.youtube.com/watch?v=CWiEwvZ2D1o&list=PLgiSTnsNaZglnrY7zt804HAeELWUqqkFr)

# What is GitOps?

GitOps is the code-based infrastructure and operational procedures that rely on Git as a source control system.

# **GitOps Principles**

There are four key principles of GitOps that drive its implementation:

1. Describe the entire system declaratively
2. Version the canonical desired system state in Git
3. Automatically apply approved changes to the desired state
4. Ensure correctness and alert on divergence with software agents

# Reference

AWS EKS - [https://aws.amazon.com/eks/](https://aws.amazon.com/eks/)

EKSCTL - [https://eksctl.io](https://eksctl.io)

Flux v2 - [https://fluxcd.io/](https://fluxcd.io/)

Flagger - [https://flagger.app/](https://flagger.app/)

GitOps - [https://www.weave.works/technologies/gitops/](https://www.weave.works/technologies/gitops/)

EKSWorkshop - [https://www.eksworkshop.com/](https://www.eksworkshop.com/)

Whizlabs - [https://www.whizlabs.com](https://www.whizlabs.com/)

# Prerequisites

1. Install flux
```
brew install fluxcd/tap/flux
```

2. Install eksctl (to create cluster)
```
brew tap weaveworks/tap
brew install weaveworks/tap/eksctl
```

3. Install kubectl (to connect cluster)

Please verify their documentation to get updated instructions.
# Getting started

1. Create cluster
    ```
    eksctl create cluster -f cluster.yaml
    ```

2. Enable Flux in the EKSctl cluster
    ```
    eksctl enable flux -f cluster.yaml
    ``` 