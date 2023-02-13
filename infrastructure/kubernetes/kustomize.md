# Kustomize Cheatsheet

Kustomize is a tool for customizing Kubernetes YAML configurations. It allows you to create complex and sophisticated manifests by combining and customizing existing Kubernetes components. This cheatsheet will provide you with a quick reference for the most common Kustomize operations.

## Installing Kustomize

Kustomize is distributed as a standalone binary and can be installed by downloading it from the official GitHub repository.

```Bash
# Download the latest version (As of 2022-02-13)
curl -LO https://github.com/kubernetes-sigs/kustomize/releases/download/v3.9.0/kustomize_3.9.0_linux_amd64

# Make the binary executable
chmod +x kustomize_3.9.0_linux_amd64

# Move the binary to a directory in your PATH
sudo mv kustomize_3.9.0_linux_amd64 /usr/local/bin/kustomize
```

### Creating a Kustomization

A Kustomization is a file that lists the resources to be included in a Kubernetes manifest, and any transformations to be applied to them. The file is named `kustomization.yaml` and must be placed in a directory with the resources to be customized.

```YAML
# Example kustomization.yaml file
resources:
  - deployment.yaml
  - service.yaml
```

### Applying a Kustomization

The `kustomize build` command is used to generate a customized Kubernetes manifest from a Kustomization.

```Bash
# Generate a customized Kubernetes manifest
kustomize build path/to/kustomization
```

### Adding Variables

Kustomize allows you to add variables to your Kustomization using the `patches` field. These variables can be replaced at build time using environment variables or command-line flags.

```YAML
# Example kustomization.yaml with a variable
patches:
  - path: environment.yaml
    target:
      kind: Deployment
      name: my-deployment
    data:
      - op: replace
        path: /spec/template/spec/containers/0/image
        value: "{{ .Env.IMAGE_TAG }}"
```

```Bash
# Build with a variable set to "v1.0.0"
IMAGE_TAG=v1.0.0 kustomize build path/to/kustomization
```

## Transforming Resources

Kustomize allows you to transform resources using functions. These functions can be used to generate new resources, modify existing ones, or perform other operations.

```YAML
# Example kustomization.yaml with a function
generators:
  - file: function.yaml
```

## Creating and Using Bases

Kustomize allows you to create and manage multiple bases, which are a collection of resources that can be customized and deployed together.

To create a new base, you can use the following command:

```bash
kustomize create base <base-name>
```

You can then add resources to your base by copying them into the `<base-name>/resources` directory, or by creating a new directory and adding a `kustomization.yaml` file with the following contents:

```yaml
resources:
  - <resource1.yaml>
  - <resource2.yaml>
```

Once you have created your base, you can deploy it using the following command:

```bash
kustomize build <base-name> | kubectl apply -f -
```

## Overriding Resources

Kustomize allows you to override resources in your base to make modifications without changing the original resource files.

To override a resource, you can create a new file in the `<base-name>/overlays/<overlay-name>/resources` directory with the desired changes. For example:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  replicas: 3
```

You can then apply the overlay to your base using the following command:

```bash
kustomize build <base-name>/overlays/<overlay-name> | kubectl apply -f -
```

## Patches

Kustomize also allows you to make changes to resources using patches, which are defined as JSON or strategic merge patches.

To create a patch, you can create a file in the `<base-name>/overlays/<overlay-name>/patches` directory with the desired changes. For example:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-deployment
spec:
  replicas: 3
```

You can then apply the patch to your base using the following command:

```bash
kustomize build <base-name>/overlays/<overlay-name> | kubectl apply -f -
```

## Conclusion

In this cheatsheet, we have covered the basics of using Kustomize to create and manage multiple bases, override resources, and make changes using patches. By using Kustomize, you can simplify your deployment process and make it easier to manage and maintain your Kubernetes resources.
