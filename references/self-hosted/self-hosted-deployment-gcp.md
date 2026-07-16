This guide will deploy chatwoot on a single VM in GCP. For a cloud native deployment, use our [helm charts](https://github.com/chatwoot/charts) with Google Kubernetes Engine(GKE).

This guide is a work in progress and your mileage may vary.

## Create Compute Engine (VM)

1. Navigate to VM > Compute Engine window.
2. Create an instance with a minimum of 4vCPU and 8GB RAM.(N2 General-Purpose)
3. Make sure to select the correct region you want to deploy.
4. Choose `Ubuntu 20.04` as your OS with a 120GB disk.
5. Click create.
![gcp-create-compute-engine](https://mintcdn.com/chatwoot-447c5a93/qGPxFBLJOb0CiH-G/self-hosted/images/gcp.png?w=2500&fit=max&auto=format&n=qGPxFBLJOb0CiH-G&q=85&s=8a0bd83e0e1ac3909a395173fc076d9c)

gcp-create-compute-engine

## Install Chatwoot

1. SSH into the instance created.
2. Follow the [Linux VM instructions](https://developers.chatwoot.com/self-hosted/deployment/linux-vm).
3. Woot! Woot! Your Chatwoot Instance is ready and can be accessed at `http://<your-instance-ip>:3000`. Or if you completed the domain setup during the installation, chatwoot should be available at `https://<your-domain>`

## Configure Chatwoot

1. Follow the Chatwoot docs to configure your domain, email and other parameters you need. Refer to the [Linux VM environment configuration guide](https://developers.chatwoot.com/self-hosted/deployment/linux-vm#configure-the-required-environment-variables).