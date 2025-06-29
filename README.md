# development-server-config

My `ansible` configuration for a development server

## How to Run

To execute the playbook using your inventory and the `site.yml` playbook, run the following command from the base of the repository:

```sh
export PRIVATE_KEY = "/path/to/your/private/key"
export SSH_USER = "your_ssh_username"

ansible-playbook \
site.yml \
--inventory-file ansible/inventories/hosts \
--private-key $PRIVATE_KEY \
--user $SSH_USER \
--ask-become-pass
```

## Development

```
pip install -r requirements.txt
```