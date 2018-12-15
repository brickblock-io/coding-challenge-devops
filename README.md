# Brickblock Coding Challenge - DevOps

Please complete one of the following tasks. Each task should take you no more than 2 hours.

## Option 1

### The Task

Your task is to hack the bank.

1. Visit [Bobby Tables Bank](https://bobby-tables.brickblock.sh). This is a fake insecure bank
1. Register your account with a username and password
1. Finish with your bank balance above €100
1. Document how you increased you balance
1. Document how you would secure this bank in the future

**Bonus**

1. Transfer all the funds from all the accounts into your own
1. Document how you were able to steal all of the money in the bank
1. Provide any code that you required to accomplish this task

## Option 2

### The Task

Your task is to provide a `git` repository that will contain the code to build a Kubernetes cluster on Google Kubernetes Engine with the following specifications:

1. The cluster will have 7 to 12 worker nodes
1. The workers will have:
    1. 2 non-preemptible full nodes of type `n1-standard-2` (no autoscaling)
    1. 3 preemptible nodes of type `n1-standard-2` (can autoscale to 6)
    1. 2 preemptible nodes of type `n1-standard-4` (can autoscale to 4)
1. The cluster will have 1 admin user (`admin`) and 20 regular users (`user-1`, `user-2`, etc.)
1. The cluster will have 23 namespaces
    1. `default`
    1. `backend`
    1. `frontend`
    1. `user-1`
    1. `user-2`
    1. etc.
1. The admin user will have `read` and `write` permissions for all the namespaces
1. `user-1` will have `read` permissions for the cluster and `write` permissions for the `user-1` namespace
1. Similarly, `user-2` will have `read` access to the cluster and `write` access to the `user-2` namespace
1. The cluster will have 1 secret that is synchronized across all namespaces `dockerhub-credentials` that provides image pull secrets to the cluster
1. The cluster should also have credentials to a service account that has the following abilities:
    1. create databases on CloudSQL
    1. encrypt/decrypt secrets with Google KMS
    1. create and destroy buckets on Google Cloud Storage
1. The cluster should have an ingress controller that will create DNS records on either Google DNS or Cloudflare automatically
1. The cluster should take care of SSL termination (through LetsEncrypt or other means)
1. Create a `README.md` that provides instructions on how to use your repository

You may choose any freely available tools that you feel will be helpful in the tasks above. If you choose to do the above task on AWS instead, please translate the requirements to AWS equivalents

### Acceptance criteria

* You must provide your code in full so we can replicate your cluster
* You must use either Google Cloud or AWS to build the above cluster (you do not need to provide access to the cluster, only to the code)
* Your code is clean and readable
* You must document any steps that are not automated in the `README.md`

## Option 3

### The Task

Your task is to provide a `git` repository that will contain the code to build a [Kubernetes Operator](https://coreos.com/operators/) that does the following:

  1. Tweets or sends a slack message or somehow tells the world `hello world from $name` when a custom resource with `$name` specified in the `spec` is created
  1. Tweets or sends a slack message or somehow tells the world `things have changed, $name` when the above custom resource is modified
  1. Tweets or sends a slack message or somehow tells the world `goodbye world from $name` when the above custom resource is deleted

You may use any language and/or toolset to achieve the above as long as they are freely available.

### Acceptance criteria

  * Your code is clean and readable
  * You have a `README.md` that explains how to use your operator
  * You provide deployment instructions (ideally manifests or a Helm chart to deploy your operator to a cluster)
  * Provide some rationale for your design choices (I used `$language` because..., I used `$library` because..., etc. )
