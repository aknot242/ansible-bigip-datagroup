# Remote BIG-IP datagroup administration using Ansible in a Docker container

## Dependencies
- Ansible 2.5
- F5 Super NetOps Docker container https://hub.docker.com/r/f5usecases/f5-rs-container/

## Prerequisites
- Docker must be installed
- Your Docker container must be able to connect to a specified BIG-IP over TCP port 443
- The BIG-IP must already be configured with a management address, and must already have a strong password set if using BIG-IP v14+

## Usage
Update the [playbook.yml](playbook.yml), [inventory/hosts.yml](inventory/hosts.yml) file accordingly for your environment. Run `./init_docker_container.sh` first. Once the container is up, `cd ansible-bigip-datagroup` then run `ansible-playbook /home/snops/ansible-bigip-datagroup/playbook.yml` inside the container.
