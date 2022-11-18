# 3dprinter-playbook

Ansible playbook to setup my 3dprinter server 🐙🖨️🌐

It setups [mjpg-streamer](https://github.com/jacksonliam/mjpg-streamer), [haproxy](https://www.haproxy.org/), [octoprint](https://octoprint.org/) and extensions

## Setup
- Install ansible `brew install ansible`
- Install ansible role dependencies `ansible-galaxy install -r requirements.yml`
- Setup ansible vault `ansible-vault new secret.yml`, check the **secret_example.yml** to know the secrets to add 
- Add the public ssh key to the server `ssh-copy-id user@host`

## Run
- Run the hole playbook `ansible-playbook run.yml`
- Run parts of the playbook `ansible-playbook run.yml -t <tag>`, check **run.yml** to know the available tags

