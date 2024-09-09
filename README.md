# `awsctx`: Power tool for aws cli

![Proudly written in Bash](https://img.shields.io/badge/written%20in-bash-ff69b4.svg)

## What is `awsctx`?

`awsctx` is a tool to manage profile switching while using [aws cli](https://docs.aws.amazon.com/cli/v1/userguide/cli-configure-files.html#cli-configure-files-using-profiles).

A quick `awsctx` demo:

### Examples

```sh
# pre work: login the sso session to enable
$ aws sso login

# list all profiles configured
$ awsctx
rualab
czdev
czhom
czpro

# set a profile configured in aws credentials file
$ awsctx rualab
Active profile is "rualab".

# execute aws cli commands with rualab profile
$ aws s3 ls
# it will execute the command using the profile configuration of rualab profile

# switch to another profile
$ awsctx czdev
Active profile is "czdev".

# switch back to the previous profile
$ awsctx -
Active profile is "rualab".
```

-----

## Installation

Stable version of `awsctx` is a bash script.

### Instalation options

- [mannually on MacOS and Linux](#manual-installation-macos-and-linux)

> **Note:** *Other installation options are in the roadmap.*

### Manual Installation (macOS and Linux)

The power tool is a bash script that you need to clone and make it avaliable somewhere in your PATH.

``` bash
sudo git clone https://github.com/jorgerua/awsctx.git /opt/awsctx
sudo ln -s /opt/awsctx/awsctx /usr/local/bin/awsctx
```
