# <img valign="middle" src="https://www.vicchi.org/assets/images/avatar.jpeg" height="64" alt="Gary Gale">&nbsp;reverse-proxy

A Docker reverse proxy stack based on [Traefik](https://traefik.io/traefik/) with SSL certificate generation via [CloudFlare](https://www.cloudflare.com/en-gb/dns/) DNS-01 challenge and with [Portainer Agent](https://docs.portainer.io/start/install-ce); all deployable with [Ansible](https://docs.ansible.com/ansible/latest/getting_started/index.html).

## Here Be Dragons

This is a personal project and relies on my own, opinionated, setup that works for sites I maintain. It might be useful as an example of how to set up and deploy one or more web stacks with Docker and Ansible. Or not. YMMV.

## Configuration

Copy `.secrets.sample` and edit to your taste, including your CloudFlare account email and API token.

The default Ansible inventory, configured in `ansible.cfg`, lives in `./playbooks/inventory/hosts.yml`.

## Deploy

```
ansible-playbook playbooks.yml -K
```

## To Do

* Add Gitea and GitHub actions workflows for build and deployment
* Add Ansible Vault for deployment `sudo` authentication

## Colophon abnd Licence

This is a thing made by [Gary Gale](https://www.vicchi.org/pages/about/) and is licensed under the [BSD 3 Clause licence](./LICENCE).
