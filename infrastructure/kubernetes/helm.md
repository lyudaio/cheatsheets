# Helm Cheatsheet - Latest LTS

Helm is a popular open-source package management tool for Kubernetes. It allows users to easily manage and deploy applications in a Kubernetes cluster.

## Installing Helm

- Download the latest version of Helm from the [Official Website](https://helm.sh/docs/intro/install/)

- Install Helm using the following command:

```bash
curl https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3 | bash
```

## Initializing Helm

Initialize Helm on your local machine by running the following command:

```bash
helm init
```

## Creating a Chart

Create a new directory for your chart:

```bash
mkdir mychart
cd mychart
```

Use the following command to create a new chart:

```bash
helm create chart
```

## Deploying a Chart

Deploy a chart to your Kubernetes cluster by running the following command:

```bash
helm install --name myrelease mychart
```

## Upgrading a Chart

Upgrade an existing release by running the following command:

```bash
helm upgrade myrelease mychart
```

## Deleting a Chart

Delete a release by running the following command:

```bash
helm delete myrelease
```

For more information on using Helm, visit the [Official Documentation](https://helm.sh/docs/)
