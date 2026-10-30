# Testing checklist

- [ ] Inventory host is reachable with Ansible ping.
- [ ] Nginx package is installed.
- [ ] Nginx service is enabled and active.
- [ ] All four HTML pages and `style.css` exist in the configured web root.
- [ ] Homepage returns HTTP 200.
- [ ] Navigation links between pages work.
- [ ] A second playbook run reports no unnecessary changes.
- [ ] The README contains tested setup and execution commands.

Suggested checks (run from the control node):
- `ansible web_servers -m ping`
- `ansible-playbook site.yml --syntax-check`
- `ansible-playbook site.yml --check` (where supported; package and service checks can vary)
- `curl -I http://TARGET_SERVER_IP/`

Replace `TARGET_SERVER_IP` with the authorized lab host's IP address.
