# HomeLab Kubernetes deployment with Ansible

## Description

Ansible resource to configure HomeLab server. It's designed to serve my needs, however you may find it useful for your individual application.

## Getting Started

### Prerequisites

- Python 3.11+

### Setting up a Python Virtual Environment

```bash
python3 -m venv .venv
source .venv/bin/activate
pip3 install -r requirements.txt
```

## Edit Ansible Vault secrets

```bash
EDITOR='code --wait' ansible-vault edit group_vars/cluster/vault.yml
```

## Deploy Kubernetes cluster

Check if Ansible can connect to k8s servers.

```bash
ansible all -m ping
```

Run Ansible playbook to create K8S cluster.

```bash
ansible-playbook playbooks/cluster.yml
```
