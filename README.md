# Creating a mock Terraform provider

- NOTE: Provider is for testing purposes only!

## Steps to build executable

Once provider and resource functions are created:

- `go mod init`
- `go fmt`
- `go mod tidy`
- `go build -o terraform-provider-example`


Copy provider binary into plugins directory:

- `~/.terraform.d/plugins/terraform-example.com/exampleprovider/example/1.0.0/darwin_amd64/terraform-provider-example`

- `mkdir -p ~/.terraform.d/plugins/terraform-example.com/mockprovider/mock/1.0.0/darwin_amd64`

- `cp terraform-provider-mock ~/.terraform.d/plugins/terraform-example.com/mockprovider/mock/1.0.0/darwin_amd64`


- Generate provider docs using `tfplugindocs generate`
