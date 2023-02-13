# Helm Cheatsheet - Latest LTS

Helm is a popular open-source package management tool for Kubernetes. It allows users to easily manage and deploy applications in a Kubernetes cluster.

## Installing Helm

- 1. Download the latest version of Helm from the [Official Website](https://helm.sh/docs/intro/install/>

- 2. Install Helm using the following command:

```bash
curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash
```

## Initializing Helm

- 1. Initialize Helm on your local machine by running the following command:

```bash
helm init
```

## Creating a Chart

- 1. Create a new directory for your chart:

```bash
mkdir mychart
cd mychart
```

- 2. Use the following command to create a new chart:

```bash
helm create chart
```

## Deploying a Chart

- 1. Deploy a chart to your Kubernetes cluster by running the following command:

```bash
helm install --name myrelease mychart
```

## Upgrading a Chart

- 1. Upgrade an existing release by running the following command:

```bash
helm upgrade myrelease mychart
```

## Deleting a Chart

- 1. Delete a release by running the following command:

```bash
helm delete myrelease
```

For more information on using Helm, visit the [Official Documentation](https://helm.sh/docs/)
