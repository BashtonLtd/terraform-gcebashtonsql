# terraform-gcebashtonsql

This is based on the core [Terraform](https://github.com/hashicorp/terraform/tree/master/builtin/providers/google) Google provider. I've extracted the SQL Instance resource to make fixes and be used as a provider plugin. 

## Installation

### Getting the executable

#### Binary download (amd64 only)

Simply clone the repository and link the precompiled binary into your `$PATH`. Assuming you have `~/bin` in your `$PATH`:

```
$ cd
$ git clone git@github.com:BashtonLtd/terraform-gcebashtonsql.git
$ ln -s ~/terraform-gcebashtonsql/terraform-gcebashtonsql ~/bin/terraform-gcebashtonsql
```

#### Build from source

You need golang 1.7 installed. You need a working `$GOPATH`, typically this is having a `gocode` folder in your `$HOME` directory with the following declared:
```
export GOPATH=$HOME/gocode
export PATH=$PATH:$GOPATH/bin
```

You should now be able to download, compile and place the resultant binary in your `$PATH`:
```
$ go get -v github.com/BashtonLtd/terraform-gcebashtonsql
```

### Configuration

Ensure `terraform-gcebashtonsql` is in your `$PATH`. You will need the following in `~/.terraformrc`:

```
providers {
  gcebashtonsql = "terraform-gcebashtonsql"
}
```
