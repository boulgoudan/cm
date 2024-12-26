# Manage a MacOS host with Ansible

## Prerequisities

### Install brew

```
% /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

The Xcode Command Line Tools will be installed.

Run these commands in your terminal to add Homebrew to your PATH

```
% echo >> /Users/moustapha/.zprofile
% echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/moustapha/.zprofile
```
         
Verify Homebrew installation

```
% brew doctor
Your system is ready to brew.
```

### Verify that python3 in installed (comes with Xcode CLT) 

```
% python3 --version
Python 3.9.6
```

### Install ansible

```
% brew install ansible
```

### Install git

```
% brew install git
```

## Check Ansible configuration

```
% ansible-playbook playbook.yml -i inventory/inventory.ini  --check
```

## Apply Ansible configuration

```
% ansible-playbook playbook.yml -i inventory/inventory.ini
```
