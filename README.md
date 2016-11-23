This is based on the core [Terraform](https://github.com/hashicorp/terraform/tree/master/builtin/providers/google) Google provider. I've extracted the SQL Instance resource to make fixes and be used as a provider plugin. To install check the code out to `$GOPATH/src/github.com/BashtonLtd/terraform-gcebashtonsql` then run `go install github.com/BashtonLtd/terraform-gcebashtonsql`. You will need the following in `~/.terraformrc`:

```
providers {
  gcebashtonsql = "terraform-gcebashtonsql"
}
```
