# Mac Development Ansible Playbook
This playbook installs and configures most of the software I use on my Mac for web and software development.

## Installation

Run the installer script...

```shell
curl -fsSL https://raw.githubusercontent.com/hendriknielaender/ansible/master/install | bash
```

The installer script installs Apple's command line tools , Homebrew, Python Pip, Ansible and finally it downloads and runs this playbook

## Alternative 

  1. Ensure Apple's command line tools are installed (`xcode-select --install` to launch the installer).
  2. [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/index.html):

     1. Run the following command to add Python 3 to your $PATH: `export PATH="$HOME/Library/Python/3.8/bin:/opt/homebrew/bin:$PATH"`
     2. Upgrade Pip: `sudo pip3 install --upgrade pip`
     3. Install Ansible: `pip3 install ansible`

  3. Clone or download this repository to your local drive.
  4. Run `ansible-galaxy install -r requirements.yml` inside this directory to install required Ansible roles.
  5. Run `ansible-playbook main.yml --ask-become-pass` inside this directory. Enter your macOS account password when prompted for the 'BECOME' password.

## ToDo
 - [x] Mac setup
 - [ ] Unix setup (e.g: Pop!_OS)
 - [ ] Windows setup

### Inspired by
[geerlingguy/mac-dev-playbook](https://github.com/geerlingguy/mac-dev-playbook)
[bmacauley/ansible-playbook-mac-dev](https://github.com/bmacauley/ansible-playbook-mac-dev)
