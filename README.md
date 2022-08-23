# linux-client-ansible
## Description
This repository give you the option to install and configure your linux client with ansible.

## Scope
This repo should help you to manage your linux client with ansible. All is optional - nothing is duty. 
Feel free to add new software and configuration to the repo. 

## Usage
```bash
# clone the project
git clone https://git.mms-support.de/crgr/linux-client-ansible.git

# switch to the project folder
cd linux-client-ansible/

# define what you want to install
cat <<EOF > vars/main.yml
---
install_vscode: true
install_ferdium: true

packages:
  - git

EOF

# make setup.sh executable
chmod +x setup.sh

# excute setup.sh to configure your linux-client
./setup.sh
```

## Variables
| Variable                                   | Required | Default                | Description
|--------------------------------------------|----------|------------------------|------------
| install_vscode | no | false | install vscode
| install_zsh | no | false | install zsh
| install_ferdium | no | false | install latest release of ferdium
| install_docker | no | false | install docker
| packages | no | ["git"] | install a list of packages
| packages_activate_wakemeops_repo | no| false | activate the WakeMeOps repo<br>install packages over variable packages<br>see also: https://docs.wakemeops.com/packages/

## Author Information
* Christopher Grau
* Daniel Uhlmann

## License

GPLv3
