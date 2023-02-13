# Cloud-init Cheatsheet

## Introduction

cloud-init is a popular open-source tool for handling initial server configuration. It is used by most cloud providers, including AWS, Google Cloud, and Microsoft Azure, to configure virtual machines and containers. It can perform tasks such as setting the hostname, installing packages, and writing files.

## Basic Usage

Here is an example of how to use cloud-init in an AWS EC2 instance. This will install the `nginx` package and start the service.

```Bash
#cloud-config

package_update: true

packages:
  - nginx

runcmd:
  - service nginx start
```

## Modules

cloud-init supports a variety of modules to perform different tasks. Some of the most commonly used modules are:

### Package Management

cloud-init supports both `apt` and `yum` package managers.

```Bash
#cloud-config

package_update: true

packages:
  - nginx
```

### File Writing

You can write files to disk using the `write_files` module.

```Bash
#cloud-config

write_files:
  - path: /etc/nginx/nginx.conf
    content: |
      server {
        listen 80;
        location / {
          root /var/www/html;
          index index.html index.htm;
        }
      }
```

### Command Execution

You can run commands using the `runcmd` module.

```Bash
#cloud-config

runcmd:
  - service nginx start
```

## Conclusion

cloud-init is a powerful tool for automating initial server configuration. With its variety of modules, you can perform a wide range of tasks such as package installation, file writing, and command execution. Whether you are using a cloud provider or managing your own infrastructure, cloud-init can save you time and make your life easier.
