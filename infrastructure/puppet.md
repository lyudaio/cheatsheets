# Puppet Cheatsheet (LTS version: 6.19.0)

Puppet is an open-source configuration management tool that enables you to automate the management of your infrastructure as code.

## Basic Usage

### Running Puppet

To run Puppet, you can use the following command:

```bash
puppet apply /path/to/manifest.pp
```

The `apply` subcommand takes the path to a Puppet manifest, which is a script that specifies the desired state of your infrastructure.

### Declaring Resources

A Puppet resource represents a component of your infrastructure, such as a file, a user, or a service.

To declare a resource, you use the following syntax:

```puppet
resource_type { 'resource_title':
  attribute1 => 'value1',
  attribute2 => 'value2',
  ...
}
```

For example, the following code declares a file resource:

```puppet
file { '/tmp/hello.txt':
  ensure => 'present',
  content => 'Hello, world!',
}
```

This resource ensures that the file `/tmp/hello.txt` exists and has the specified content.

### Modules

Puppet modules are collections of Puppet code that can be used to manage different types of resources.

You can install modules from the Puppet Forge, which is the official repository of Puppet modules.

To install a module, you can use the following command:

```bash
puppet module install puppetlabs-ntp
```

This installs the `puppetlabs-ntp` module, which manages the Network Time Protocol (NTP) service.

## Advanced Usage

### Classes

Puppet classes are reusable components that can be declared and invoked in your manifests.

To declare a class, you use the following syntax:

```puppet
class class_name {
  attribute1 => 'value1',
  attribute2 => 'value2',
  ...

  resource_type { 'resource_title':
    ...
  }
}
```

For example, the following code declares a class that installs and configures the NTP service:

```puppet
class ntp {
  package { 'ntp':
    ensure => 'installed',
  }

  service { 'ntp':
    ensure => 'running',
    enable => true,
  }

  file { '/etc/ntp.conf':
    ensure  => 'present',
    content => template('ntp/ntp.conf.erb'),
  }
}
```

To invoke a class, you use the following syntax:

```puppet
include class_name
```

For example, the following code invokes the `ntp` class:

```puppet
include ntp
```

## Hiera

Hiera is a configuration data management tool that allows you to manage your configuration data in a centralized and structured way. You can use Hiera to store data in a YAML file, and reference that data in your Puppet code.

Here's an example of how you can use Hiera in your Puppet code:

```Bash
# Puppet code that references Hiera data
$username = hiera('username')

user { $username:
  ensure => present,
}
```

And here's an example of a Hiera YAML file that provides the data for the above code:

```YAML
# hiera.yaml
---
username: 'admin'
```

### Using Hiera in Modules

You can use Hiera in your modules to manage the configuration data for your module. To do this, you can create a Hiera data file for your module and store it in the `data` directory of your module.

Here's an example of a Hiera data file for a module:

```YAML
# data/common.yaml
---
module::setting1: 'value1'
module::setting2: 'value2'
```

And here's an example of how you can use the Hiera data in your module's code:

```Bash
# Puppet module code that references Hiera data
$setting1 = hiera('module::setting1')
$setting2 = hiera('module::setting2')

# Use the settings in your code
file { '/tmp/setting1':
  content => $setting1,
}

file { '/tmp/setting2':
  content => $setting2,
}
```

## Modules Modules Continued

Modules are a way to organize and reuse your Puppet code. They allow you to encapsulate a complete configuration for a specific aspect of your infrastructure.

Here's an example of how you can create a module:

```Bash
# Create a directory for your module
$ mkdir /etc/puppet/modules/mymodule

# Create a file for your module's code
$ vi /etc/puppet/modules/mymodule/manifests/init.pp

# Define a class in your module's code
class mymodule {
  file { '/tmp/myfile':
    content => 'Hello, world!',
  }
}
```

You can then include the module in your main Puppet code:

```Bash
# Main Puppet code that includes a module
include mymodule
```

## Classes Continued

Classes are a way to group resources and definitions in your Puppet code. They allow you to encapsulate a complete configuration for a specific aspect of your infrastructure.

Here's an example of how you can create a class:

```Bash
# Define a class in your Puppet code
class myclass {
  file { '/tmp/myfile':
    content => 'Hello, world!',
  }
}
```

You can then include the class in your main Puppet code:

```Bash
# Main Puppet code that includes a class
include myclass
```

## Resources Continued

In Puppet, resources are the building blocks that describe the desired state of your systems.

A resource declaration has three parts:

- The resource type (e.g., `file`, `service`, `package`)
- The title (a unique identifier for the resource)
- One or more attributes that specify the desired state for the resource

### File Resource

The `file` resource type is used to manage files and directories.

```puppet
file { '/path/to/file':
  ensure => present,
  mode   => '0644',
  owner  => 'root',
  group  => 'root',
  source => 'puppet:///modules/mymodule/myfile',
}
```

### Package Resource

The `package` resource type is used to manage packages.

```puppet
package { 'nginx':
  ensure => installed,
}
```

### Service Resource

The `service` resource type is used to manage services.

```puppet
service { 'nginx':
  ensure => running,
  enable => true,
}
```

## Conclusion

Puppet is a powerful infrastructure management tool that enables you to automate the management and configuration of your infrastructure. With the knowledge of this cheatsheet, you should be able to quickly get started using Puppet and take advantage of its features.

As with any tool, it's important to learn and experiment with Puppet, in order to fully understand its capabilities and limitations. Remember to keep referring to the official documentation and to experiment with different configurations to find the best setup for your infrastructure.
