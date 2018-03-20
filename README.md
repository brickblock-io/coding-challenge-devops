# Brickblock Coding Challenge - DevOps

## The Goal
Your task is to set up a Kubernetes cluster and deploy a REST API and a frontend that consumes the REST API into it.

## The Process
1. Set up a Kubernetes cluster. However you like. We're leaving this purposefully open for you to do your own research on how you want to go about it. You can roll your own cluster using, for example, [kops](https://github.com/kubernetes/kops) or you can leverage existing cluster services such as [AWS EKS](https://aws.amazon.com/eks/) or Google Cloud's [Kubernetes Engine](https://cloud.google.com/kubernetes-engine/). Or you can go really deep and [do it the hard way](https://github.com/kelseyhightower/kubernetes-the-hard-way) by manually bootstrapping it.
1. When you have a running cluster, deploy an API of your choice and a frontend application of your choice that consumes the API into the cluster. This can be a handwritten hello world application or any other ready-made docker images.
1. Document how to access and use the applications you deployed
1. Let us know you're ready to review by sending us documentation and access to the cluster via email to dev@brickblock.io

## Acceptance Criteria
* Your Kubernetes cluster is up and running
* Your frontend application is running and accessible under a domain of your choice
* The frontend displays data from the API
* The code you've written to create the cluster and deploy the applications is accessible, for example in a GitHub repo

## Bonus Round (not required, but nice-to-have)
* Your application is available via SSL
* Automate the cluster setup, e.g. through shell scripts or terraform etc.
* Your application is auto-scaling. Meaning when you put load on it (via Apache Workbench for example) it automatically auto-scales horizontally by adding more pods
* Your API is hooked up to a database (can be inside the cluster or outside)
* You have isolated staging and production environments for your application

## How we're evaluating the result
Prioritised from most important to least important, here are our evaluation criteria:

1. Feature Completeness: Does your cluster fulfil all acceptance criteria?
1. Code Quality: If you've written any code to achieve the task, is the code clean, well-structured and easy to understand?
1. Documentation: How good is the documentation?
1. The extra mile: Did you hit any bonus goals?

You do not need to hit all points, but obviously, the more the better :)