# AWS Cli

## Setup Credentials

``` bash
aws configure
```

## Working with profiles

``` bash
# Configures a profile
aws configure --profile proftwo

# List Current Config
aws configure list

# Get info of user
aws sts get-caller-identity

# Get info of user for the profile
aws sts get-caller-identity --profile profone

# Look at profiles
cat ~/.aws/config

# Look at credentials
cat ~/.aws/credentials

# A profile for the session (wont need to use --profile in all commands)
export AWS_PROFILE=my-thegud

#Default region
export AWS_DEFAULT_REGION=us-east-1
```

Boas práticas:
* Não deixar um profile default
* usar a export AWS_PROFILE=<profile> para não ter que colocar em todos os comandos

