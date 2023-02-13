# kubectl Cheatsheet

Kubectl is a command-line tool for managing Kubernetes clusters. The latest Long-Term Support (LTS) version is `1.21.0` as of 2023.

## Common Commands

### Cluster Management

- Get the status of a cluster:

  ```bash
  kubectl cluster-info
  ```

- Get the configuration details of a cluster:

  ```bash
  kubectl config view
  ```

- Switch context to a different cluster:

  ```bash
  kubectl config use-context <context_name>
  ```

### Namespaces

- Get a list of all namespaces:

  ```bash
  kubectl get namespaces
  ```

- Get details of a particular namespace:

  ```bash
  kubectl describe namespace <namespace_name>
  ```

- Create a new namespace:

  ```bash
  kubectl create namespace <namespace_name>
  ```

### Pods

- Get a list of all pods in a namespace:

  ```bash
  kubectl get pods --namespace <namespace_name>
  ```

- Get detailed information about a pod:

  ```bash
  kubectl describe pod <pod_name> --namespace <namespace_name>
  ```

- Delete a pod:

  ```bash
  kubectl delete pod <pod_name> --namespace <namespace_name>
  ```

### Services

- Get a list of all services in a namespace:

  ```bash
  kubectl get services --namespace <namespace_name>
  ```

- Get detailed information about a service:

  ```bash
  kubectl describe service <service_name> --namespace <namespace_name>
  ```

- Delete a service:

  ```bash
  kubectl delete service <service_name> --namespace <namespace_name>
  ```

### Deployments

- Get a list of all deployments in a namespace:

  ```bash
  kubectl get deployments --namespace <namespace_name>
  ```

- Get detailed information about a deployment:

  ```bash
  kubectl describe deployment <deployment_name> --namespace <namespace_name>
  ```

- Scale a deployment:

  ```bash
  kubectl scale deployment <deployment_name> --replicas <replica_count> --namespace <namespace_name>
  ```

- Delete a deployment:

  ```bash
  kubectl delete deployment <deployment_name> --namespace <namespace_name>
  ```

## Conclusion

This cheatsheet has covered some of the most commonly used commands in kubectl. For a comprehensive list of all available commands and options, refer to the official Kubernetes [kubectl documentation](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands).
