# GitOpsDemo

![GitHub last commit](https://img.shields.io/github/last-commit/jesperberth/GitOpsDemo)

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/jesperberth/GitOpsDemo/build)

```bash

Create keypair

ssh-keygen -m PEM -t rsa -b 4096 -f ~/.ssh/webserver


Dosnt work
upload ssh key to Azure

az group create --name "webserver" --location "northeurope"

az sshkey create --location "northeurope" --public-key "@~/.ssh/webserver.pub" --resource-group "webserver" --name "webserverSshPublicKey"

```

```bash
ansible-playbook network.yml
ansible-playbook security.yml
ansible-playbook compute.yml
ansible-playbook loadbalancer.yml
ansible-playbook -i inv.azure_rm.yml install_compute.yml --key-file ~/.ssh/webserver -e "ansible_user=azureuser"

```

[https://nexxai.dev/store-a-private-key-in-azure-key-vault-for-use-in-a-logic-app/](https://nexxai.dev/store-a-private-key-in-azure-key-vault-for-use-in-a-logic-app/)

[https://docs.microsoft.com/en-us/azure/developer/github/github-key-vault](https://docs.microsoft.com/en-us/azure/developer/github/github-key-vault)

```bash
{
    "clientId": "<GUID>",
    "clientSecret": "<GUID>",
    "subscriptionId": "<GUID>",
    "tenantId": "<GUID>"
}

```
