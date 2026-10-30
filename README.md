# Automated Portfolio Website Deployment Using Ansible Roles

## Project duration
2 days | Team size: 4 members

## Objective
Use Ansible roles to install and configure Nginx on a Linux target and deploy a static portfolio website built with HTML and CSS.

## Website pages
- Home: `index.html`
- About: `about.html`
- Projects: `projects.html`
- Contact: `contact.html`
- Shared styling: `style.css`

## Planned workflow
1. Configure the Ansible inventory and SSH access to a target Linux server.
2. Implement the `nginx` role to install Nginx and ensure its service is enabled and running.
3. Implement the `portfolio` role to deploy the HTML/CSS files to the configured web root.
4. Run `site.yml` and verify the website in a browser using the target server's IP address.

## Prerequisites
- Ansible installed on the control node
- A supported Linux target with SSH access
- A user with appropriate privileges to install packages and write to the Nginx web root
- Network access to the web server's HTTP port (usually TCP/80)

## Starter repository note
This is a task starter, not a completed solution. Ansible tasks contain TODO markers for team members to implement. The team should test the playbook on a lab server before using it elsewhere.

## Expected outcome
- Nginx is installed, enabled, and running.
- The four portfolio pages and CSS are deployed.
- The homepage and page navigation work in a browser.
- Running the playbook a second time does not report unnecessary changes.
