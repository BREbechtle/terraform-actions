# Terraform Projects in this directory will be automatically applied on push

Make sure your Terraform files in this directory are well configured.

The Storage Account and Container are already configured for usage with GitHub Actions.

No statefile key is set yet.

Suggested provider configuration to use your Azure Storage Account as backend:
```
terraform {
  required_providers {
    azurerm = {
      source = "hashicorp/azurerm"
    }
  }
  backend "azurerm" {
    key = "state.tfstate" # choose any name you like
  }
}
provider "azurerm" {
  resource_provider_registrations = "core"
  features {}
}
```

Once configured, push your project to this repository for automatic deployment.
