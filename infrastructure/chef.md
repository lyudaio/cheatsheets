# Chef Cheatsheet - Latest LTS

## Introduction

Chef is a powerful automation platform that transforms infrastructure into code, ensuring that configurations are consistent, version-controlled, and manageable. It helps you automate everything from a single node to an entire data center with ease.

## Getting Started

Before using Chef, you'll need to install Chef Workstation. To do this, simply follow the instructions on the [Official Website.](https://downloads.chef.io/chef-workstation/)

## Basic Chef Concepts

- **Cookbook:** A cookbook is the fundamental unit of configuration and policy distribution. It consists of recipes, attributes, definitions, and files.
- **Recipe:** A recipe is the most fundamental configuration element within a cookbook. Recipes describe how to install and configure software on a node.
- **Attribute:** An attribute is a value that is associated with a node and can be used in recipes to determine the configuration.
- **Node:** A node is any machine that is under management by Chef.

## Chef CLI Commands

Here are some of the most common Chef CLI commands you'll use:

```Bash
# Use this command to view information about your node
$ chef-client -n node_name

# Use this command to view information about your cookbook
$ knife cookbook show cookbook_name

# Use this command to upload your cookbook to the Chef server
$ knife cookbook upload cookbook_name

# Use this command to view information about your role
$ knife role show role_name

# Use this command to upload your role to the Chef server
$ knife role from file role_file.rb
```

## Writing Chef Recipes

A Chef recipe is written in Ruby and follows a specific syntax. Here's an example of a basic recipe:

```Ruby
# This recipe installs the Apache web server
package 'httpd' do
  action :install
end

service 'httpd' do
  action [:enable, :start]
end
```

## Conclusion

That's it! You now have the basic knowledge to start using Chef to automate your infrastructure. For more information, including a full reference of the Chef DSL, visit the [Official Documentation.](https://docs.chef.io/)
