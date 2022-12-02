# 3dprinter-playbook

Ansible playbook to setup my 3dprinter server 🐙🖨️🌐

It setups [mjpg-streamer](https://github.com/jacksonliam/mjpg-streamer), [haproxy](https://www.haproxy.org/), [octoprint](https://octoprint.org/) and extensions

## Requirements 
- Computer with **Ubuntu server** installed 
## Setup
- Install ansible `brew install ansible`
- Install ansible role dependencies `ansible-galaxy install -r requirements.yml`
- Establish `ssh` connection with your **Ubuntu server**
- Add the public ssh key to the server `ssh-copy-id user@host`
- Setup ansible vault:
  - Rename `secret_example.yml` to `secret.yml` and fill it with real data
  - Encrypt it with `ansible-vault encrypt secret.yml`

## Run
- Run the hole playbook `ansible-playbook run.yml`
- Run parts of the playbook `ansible-playbook run.yml -t <tag>`, check **run.yml** to know the available tags

