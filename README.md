# Kubernetes Installation with Ansible

This project provides Ansible playbooks and roles to automate the installation and configuration of a Kubernetes cluster.

## Features

- Automated setup of Kubernetes control plane and worker nodes
- Idempotent playbooks for consistent, repeatable deployments
- Customizable variables for cluster configuration
- Modular roles for easier maintenance and extension

## Prerequisites

- Supported Linux distribution: **Ubuntu**
- Python 3 must be installed on all target nodes

## Usage

1. Clone this repository:
    ```bash
    git clone https://github.com/rahulitpro/k8s_install.git
    cd k8s_install
    ```

2. Update the `inventory.ini` file with your server details (IP addresses or hostnames).

3. Customize variables in `external_vars.yml` as needed for your environment.

4. Run the main playbook:
    ```bash
    ansible-playbook -i inventory.ini main.yml
    ```

## Directory Structure

```
k8s_install/
├── external_vars.yml                   # Variable definitions for groups/hosts
├── tasks/                              # Ansible tasks for Kubernetes components
├── inventory.ini                       # Inventory file listing your nodes
├── main.yml                            # Main playbook entry point
├── metallb/                            # MetalLB config and template
├── nfs-subdir-external-provisioner/    # NFS Provisioner config and template
└── README.md                           # Project documentation
```

## License

MIT License

## Contributing

Contributions are welcome! Please open issues or submit pull requests.
