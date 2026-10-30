# Two-Day Assignment: Automated Portfolio Website Deployment Using Ansible Roles

## Objective
Create a static portfolio website using HTML/CSS and automate its deployment to a Linux server using Ansible roles and Nginx.

## Day 1 — Setup and implementation
### Member 1: Inventory and Nginx installation
- Configure the inventory using `inventory.ini.example`.
- Verify SSH connectivity to the target host.
- Implement package installation in `roles/nginx/tasks/main.yml`.

### Member 2: Nginx service configuration
- Ensure Nginx is enabled and running.
- Add a handler if a configuration change requires an Nginx reload/restart.
- Keep changes repeatable and idempotent.

### Member 3: Portfolio pages and deployment
- Review the provided HTML/CSS starter files.
- Implement `roles/portfolio/tasks/main.yml` to deploy all required files to the configured web root.
- Ensure file permissions are suitable for Nginx to serve the files.

### Member 4: Integration and testing
- Review the playbook and task requirements.
- Prepare a test checklist and help integrate the roles.
- Check HTTP access and links between pages.

## Day 2 — Integration and validation
- Run the playbook against the target Linux host.
- Verify Nginx is active and enabled.
- Open the website using the server's IP address.
- Check Home, About, Projects, and Contact navigation.
- Run the playbook again and check idempotency.
- Fix errors and update README with exact setup/run commands and test results.

## Acceptance criteria
1. The main playbook runs successfully against the intended test host.
2. Nginx is installed and enabled/running.
3. All four HTML pages and `style.css` are deployed to the web root.
4. The homepage loads over HTTP and navigation links work.
5. A second playbook run makes no unnecessary changes.
6. Documentation explains prerequisites, inventory setup, execution, and validation.

## Safety
- Do not commit private SSH keys, passwords, tokens, or real personal information.
- Use a disposable lab server and restrict inbound HTTP access to the required audience.
- Do not change production servers without explicit authorization.
