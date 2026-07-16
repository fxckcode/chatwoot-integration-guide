This guide will deploy chatwoot on a single VM in Azure. For a cloud native deployment, use our [helm charts](https://github.com/chatwoot/charts) with Azure Kubernetes Service(AKS).

This guide is a work in progress and your mileage may vary.

## Create a Virtual Machine

1. Login to the Azure portal and choose Virtual Machines.
2. Select create a VM from scratch.
3. In the Basics tab, create a subscription and a new resource group.
4. Name the virtual machine as `chatwoot` and select your preferred region.
5. Select `Ubuntu 20.04 LTS - Gen2` as the image.
6. For instance size, we recommend the type `Standard_D4s_v3` (4vCPU, 16GB RAM).
7. Under authentication, leave the defaults and create a new key pair if needed.
8. Allow HTTP, HTTPS and SSH under inbound port rules.
9. Click next and leave the defaults for Disks, Networking, Management, Advanced and Tags section.
10. Select `Review + create` to spin up the VM.
![azure-create-vm](https://mintcdn.com/chatwoot-447c5a93/0ZKii1AePO4f9gzo/self-hosted/images/azure.png?w=2500&fit=max&auto=format&n=0ZKii1AePO4f9gzo&q=85&s=2679d035c04dc9f8eb972a08b80ac61c)

azure-create-vm

## Install Chatwoot

1. SSH into the instance created from your local machine or create a bastion in azure to ssh via the browser.
2. Follow the [Linux VM instructions](https://developers.chatwoot.com/self-hosted/deployment/linux-vm).
3. Woot! Woot! Your Chatwoot Instance is ready and can be accessed at `http://<your-instance-ip>:3000`. Or if you completed the domain setup during the installation, chatwoot should be available at `https://<your-domain>`.

Browser access via port 3000 will only work if enabled under inbound rules.

## Configure Chatwoot

1. Follow the Chatwoot docs to configure your domain, email and other parameters you need. Refer to the [Linux VM environment configuration guide](https://developers.chatwoot.com/self-hosted/deployment/linux-vm#configure-the-required-environment-variables).