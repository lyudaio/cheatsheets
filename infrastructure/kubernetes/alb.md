# AWS Ingress Controller Cheatsheet for EKS

## Description

The AWS Load Balancer Controller is a Kubernetes ingress controller that makes it easy to set up Amazon Web Services (AWS) Load Balancers to route traffic to Kubernetes services running on Amazon Elastic Kubernetes Service (EKS). The controller automatically configures and manages the resources needed to route traffic, including Elastic Load Balancers, Target Groups, and listeners.

## Prerequisites

- Kubernetes 1.18 or later
- Amazon EKS cluster
- IAM permissions to create AWS resources

## Installation

1. Create an IAM OIDC provider and policy to allow Kubernetes to assume an IAM role.
2. Deploy the AWS Load Balancer Controller manifest:

```bash
kubectl apply -k "github.com/aws/eks-charts/stable/aws-load-balancer-controller//crds?ref=master"
kubectl apply -k "github.com/aws/eks-charts/stable/aws-load-balancer-controller//install?ref=master"
```

3. Create an IAM role for the AWS Load Balancer Controller to use:

```bash
$ eksctl create iamserviceaccount --name aws-load-balancer-controller \
--namespace kube-system --cluster my-cluster \
--attach-policy-arn arn:aws:iam::123456789012:policy/my-iam-policy \
--approve --override-existing-serviceaccounts
```

4. Update the `cluster-name` and `region` fields in the `aws-load-balancer-controller` deployment manifest.

5. Deploy the updated `aws-load-balancer-controller` deployment manifest:

```bash
kubectl apply -f aws-load-balancer-controller.yaml
```

6. Verify that the controller is running:

```bash
kubectl logs -n kube-system deployment/aws-load-balancer-controller
```

## Usage

1. Define an Ingress resource that specifies the rules for routing traffic to your Kubernetes services. Example:

```bash
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: my-ingress
  annotations:
    kubernetes.io/ingress.class: alb
    alb.ingress.kubernetes.io/scheme: internet-facing
    alb.ingress.kubernetes.io/target-type: ip
spec:
  rules:
  - host: my-domain.com
    http:
      paths:
      - path: /*
        pathType: Prefix
        backend:
          service:
            name: my-service
            port:
              name: http
```

2. Apply the Ingress resource to your Kubernetes cluster:

```bash
kubectl apply -f my-ingress.yaml
```

3. Verify that the Load Balancer has been created and is routing traffic to your service:

```bash
kubectl get ingress my-ingress
```

## Additional Resources

- [AWS Load Balancer Controller documentation](https://docs.aws.amazon.com/eks/latest/userguide/aws-load-balancer-controller.html)
- [AWS Load Balancer Controller GitHub repository](https://github.com/aws/eks-charts/tree/master/stable/aws-load-balancer-controller)
