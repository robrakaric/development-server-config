# development-server-config

My `ansible` configuration for a development server

## How to Run

To execute the playbook using your inventory and the `site.yml` playbook, run the following command from the base of the repository:

```sh
ansible-playbook -i ansible/inventories/hosts \
  --private-key YOUR_PRIVATE_KEY \
  -u YOUR_SSH_USER \
  ansible/site.yml \
  --ask-become-pass
```

- Replace `YOUR_PRIVATE_KEY` with your SSH private key path.
- Replace `YOUR_SSH_USER` with the SSH username for your target hosts.

This will apply the `development-server` roles to all hosts defined in your inventory.

## Development

```
pip install -r requirements.txt
```