# Ansible Directory Structure

├── ansible/ # All Ansible-related files
│ ├── playbooks/ # Playbooks and supporting components
│ │ ├── site.yml # Main playbook
│ │ ├── rollback.yml # Rollback playbook
│ │ ├── roles/ # Reusable Ansible roles for modular tasks
│ │ │ ├── build_image/ # Builds docker image
│ │ │ ├── detect_vuln/ # Detects vulnerabilities and defines if upgrade is required
│ │ │ ├── run_container/ # Deploys containers
│ │ │ ├── nginx_temp_switch/ # Patches nginx upstream to temporary container 5001
│ │ │ ├── nginx_switch_to_new/ # Patches nginx upstream to production container 5000
│ │ │ └── finalize_deployment/ # Finalizes deployment and cleanup
│ │ ├── handlers/ # Includes handler tasks that are only run when notified by other tasks
│ │ │ └── main/ # Reloads Nginx
