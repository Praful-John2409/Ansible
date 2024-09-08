# Ansible Deployment and Undeployment

## Overview

This repository contains Ansible playbooks for deploying and undeploying a web server using Apache. The primary goal of this assignment is to demonstrate the ability to automate the setup and teardown of web servers using Ansible.

## Repository Contents

- `deploy_webserver1.yml`: Ansible playbook for deploying Apache web server with a custom HTML page.
- `deploy_webserver2.yml`: Another playbook for deploying Apache web server with additional configurations.
- `undeploy_webserver.yml`: Ansible playbook for undeploying the Apache web server, removing custom configurations, and cleaning up.

## Playbooks Description

### `deploy_webserver1.yml`

- **Purpose**: Deploy Apache web server, create a custom HTML page, and ensure the server is up and running.
- **Configuration**: Configures Apache to listen on port 8080 with a custom HTML page.

### `deploy_webserver2.yml`

- **Purpose**: Enhanced deployment playbook with additional configurations.
- **Configuration**: Similar to `deploy_webserver1.yml`, but includes more extensive setup steps.

### `undeploy_webserver.yml`

- **Purpose**: Undeploy the Apache web server, remove custom HTML files, and clean up configurations and logs.
- **Configuration**: Stops the Apache service, uninstalls the package, and removes configuration and log files.

## Setup Instructions

1. **Clone the Repository**
   Since cloning is not supported, you will need to download or manually copy the files from the repository.

2. **Prepare Your Environment**
   Ensure you have Ansible installed on your local machine or control node. Follow the installation guide from the [Ansible documentation](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html).

3. **Update the Inventory File**
   Edit the `inventory` file to include your target hosts. Ensure that the hosts are reachable and have SSH access configured.

4. **Run the Deployment Playbook**
   ```sh
   ansible-playbook -i inventory deploy_webserver1.yml
   ```

5. **Run the Additional Deployment Playbook (if needed)**
   ```sh
   ansible-playbook -i inventory deploy_webserver2.yml
   ```

6. **Run the Undeployment Playbook**
   ```sh
   ansible-playbook -i inventory undeploy_webserver.yml
   ```

## Artifacts

Due to repository constraints, direct cloning is not available. However, the artifacts related to the assignment include the playbooks and configuration files used for deployment and undeployment. Please refer to the respective files for detailed implementations and configurations.

## Troubleshooting

- **Service Failures**: If you encounter issues with starting or stopping the Apache service, use the `systemctl` and `journalctl` commands to diagnose the problem.
- **Configuration Errors**: Verify the playbook syntax and ensure that the paths and file names match your setup.

## Contact

For any questions or issues, please contact [Praful John](https://github.com/Praful-John2409).
