# Decision Log


## Tools and Technologies

- **Ansible**: Chosen for automating server setup and app deployment. It's lightweight, easy to read, and widely supported.  
- **Ubuntu 20.04+**: Standard Linux environment that's stable and well-documented. Works smoothly with Ansible.  
- **Docker**: Used for containerizing the sample app. Makes deployments predictable across environments.  
- **SSH Key Authentication**: More secure than passwords and required by Ansible for automated SSH access.

---

## Project Structure

- **Roles under `playbooks/roles/`**: Keeps all playbooks and roles in a single location, easier to manage.  
- **Inventory in `ansible/hosts.ini`**: Centralized place to define servers. Simple and straightforward.  
- **Variables in `ansible/vars/`**: Stores reusable variables for the playbooks. Makes updates and scaling easier.

---

## Security

- **Private key permissions (`chmod 600`)**: Ensures only the owner can read the key.  
- **Sudo user for automation**: Needed for installing packages and configuring the server.

---

## Logging and Monitoring

- **Idempotency:**: /tests/ contains the output of the playbook runs  
- **Server checks with Ansible ping module**: Quick way to confirm servers are reachable.

