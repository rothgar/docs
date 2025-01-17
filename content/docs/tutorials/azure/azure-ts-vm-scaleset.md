---
title: "Azure VM Scale Sets"
---

<p class="mb-4 flex">
    <a class="flex flex-wrap items-center rounded text-xs text-white bg-blue-600 border-2 border-blue-600 px-2 mr-2 whitespace-no-wrap hover:text-white" style="height: 32px" href="https://github.com/pulumi/examples/tree/master/azure-ts-vm-scaleset" target="_blank">
        <span><i class="fab fa-github pr-2"></i> View Code</span>
    </a>

    <a href="https://app.pulumi.com/new?template=https://github.com/pulumi/examples/tree/master/azure-ts-vm-scaleset" target="_blank">
        <img src="https://get.pulumi.com/new/button.svg" alt="Deploy">
    </a>
</p>


This example provisions a Scale Set of Linux web servers with nginx deployed, configured the auto-scaling based on CPU load, puts a Load Balancer in front of them, and gives it a public IP address.

## Prerequisites

- [Node.js](https://nodejs.org/en/download/)
- [Download and install the Pulumi CLI](https://www.pulumi.com/docs/reference/install/)
- [Connect Pulumi with your Azure account](https://www.pulumi.com/docs/reference/clouds/azure/setup/) (if your `az` CLI is
      configured, this will just work)

## Running the App

1.  Create a new stack:

    ```
    $ pulumi stack init dev
    ```

1.  Configure the app deployment.

    ```
    $ pulumi config set azure:location westus    # any valid Azure region will do
    ```

    Optionally, configure the username and password for the admin user. Otherwise, they will be auto-generated.

    ```
    $ pulumi config set adminUser webmaster
    $ pulumi config set adminPassword <your-password> --secret
    ```

    Note that `--secret` ensures your password is encrypted safely.

1.  Login to Azure CLI (you will be prompted to do this during deployment if you forget this step):

    ```
    $ az login
    ```

1.  Restore NPM dependencies:

    ```
    $ npm install
    ```

1.  Run `pulumi up` to preview and deploy changes:

    ```
    $ pulumi up
    Previewing update:
    ...

    Updating:
    ...
    Resources:
        13 created
    Update duration: 2m19s
    ```

1.  Check the domain name of the PIP:

    ```
    $ pulumi stack output publicAddress
    dsuv3vqbgi.westeurope.cloudapp.azure.com
    $ curl http://$(pulumi stack output publicAddress)
    #nginx welcome screen HTML is returned
    ```

