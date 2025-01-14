# JumpCloud Terraform Provider

## Requirements

- [Terraform](https://www.terraform.io/downloads.html) 0.13+
- [Go](https://golang.org/doc/install) 1.21 (to build the provider plugin)

## Building The Provider

Clone repository to: `$GOPATH/src/github.com/cheelim1/terraform-provider-jumpcloud`

```sh
mkdir -p $GOPATH/src/github.com/cheelim1
cd $GOPATH/src/github.com/cheelim1
git clone git@github.com:cheelim1/terraform-provider-jumpcloud
```

Enter the provider directory and build the provider

```sh
cd $GOPATH/src/github.com/cheelim1/terraform-provider-jumpcloud
make build
```

## Using the provider

If you're building the provider, follow the instructions to [install it as a plugin.](https://www.terraform.io/docs/plugins/basics.html#installing-a-plugin) After placing it into your plugins directory,  run `terraform init` to initialize it.

The Jumpcloud API key needs to be set before using the provider. It can either be retrieved via the API or through the UI : When selecting a resource, the ID is part of URL.
Export `JUMPCLOUD_API_KEY` to set it.

The Jumpcloud "Organization ID" is optional as only needed for multi-tenant-setups.
Export `JUMPCLOUD_ORG_ID` to set it.


## Auto Update Docs
`go generate`

## Run tests
`ex: go test -v ./... -run TestAccDataSourceJumpCloudUserGroup_basic`

### OpenTofu
Link: https://github.com/opentofu/registry/tree/main/providers/c/cheelim1
<!-- BEGIN_TF_DOCS -->
## Requirements

No requirements.

## Providers

No providers.

## Modules

No modules.

## Resources

No resources.

## Inputs

No inputs.

## Outputs

No outputs.
<!-- END_TF_DOCS -->