# development-server-config

My `ansible` configuration for a development server

## How to Run

To execute the playbook using your inventory and the `site.yml` playbook, run the following command from the base of the repository:

```sh
export PRIVATE_KEY = "/path/to/your/private/key"
export SSH_USER = "your_ssh_username"

ansible-playbook \
site.yml \
--private-key $PRIVATE_KEY \
--user $SSH_USER \
--ask-become-pass
```

## Development

### local

```sh
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### devcontainer

Devcontainer will bind your current local user's `.ssh` directory to `/root/.ssh` in the devcontainer using `ghcr.io/ansible/community-ansible-dev-tools:latest` image.

```sh
"source=${localEnv:HOME}/.ssh,target=/root/.ssh,type=bind"
```

## Ansible

### collection index

https://docs.ansible.com/ansible/latest/collections/index.html