# nBOS Environment Configuration using Superlumic and Ansible

Superlumic is a utility wrapper around Ansible that simplifies the process of bootstrapping a new MacOS developer environment with the necessary tools and utilities used at Versent for the nBOS project.

## What will be installed?
The Superlumic utility will install the following utilities and Ansible roles prior to installing a user specific playbook
1. Homebrew Package Manager
2. Ansible
3. Sensible OSX Environment Defaults (Computer Name, Dock Size, Dock Position)
4. CLI Environment (Bash 4, Git, Git username and email configuration, CLI theme and bash completion)
5. Configurable role dependent package installation using Ansible

## Versent Confluence Guide

https://versent.atlassian.net/wiki/spaces/BR/pages/114556998/Development+Environment+Setup+with+Superlumic+and+Ansible

## Quick Start
1. Clone the Versent superlumic-config repository. This step can be skipped if the Versent superlumic-config repository is public or appropriate credentials are configured to clone the repository directly during bash script execution.
```sh
$ git clone git@github.com:Versent/superlumic-config.git
$ rm -rf .git
$ git init
$ git add .
$ git remote add origin remote repository URL
$ git push -u origin master
```
2. On the target developer machine, if the superlumic bash script doesn't exist, retrieve it from the Versent superlumic-config repository with curl.
```
$ curl -O https://raw.githubusercontent.com/Versent/superlumic-config/master/superlumic
```
3. Copy the contents of the `username.yml` template playbook and replace system dependent variables, renaming the template file to the current MacOS account username.  
4. Execute the superlumic bash script, referencing the cloned repository.
```
$ bash superlumic https://github.com/remote repository URL/superlumic-config.git
```
