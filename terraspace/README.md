# Terraspace Project

This is a Terraspace project. It contains code to provision Cloud infrastructure built with [Terraform](https://www.terraform.io/) and the [Terraspace Framework](https://terraspace.cloud/).

## Deploy

To deploy all the infrastructure stacks:

    AWS_PROFILE=<profile> AWS_REGION=<region> TS_ENV=<environment> bundle exec terraspace all up
    terraspace all up

To deploy individual stacks:

    AWS_PROFILE=<profile> AWS_REGION=<region> TS_ENV=<environment> bundle exec terraspace up shared
    AWS_PROFILE=<profile> AWS_REGION=<region> TS_ENV=<environment> bundle exec terraspace up indexing
    AWS_PROFILE=<profile> AWS_REGION=<region> TS_ENV=<environment> bundle exec terraspace up peer
    AWS_PROFILE=<profile> AWS_REGION=<region> TS_ENV=<environment> bundle exec terraspace up peer-kubernetes-components
    terraspace up shared                     # where shared is app/stacks/shared
    terraspace up indexing                   # where indexing is app/stacks/indexing
    terraspace up peer                       # where peer is app/stacks/peer
    terraspace up peer-kubernetes-components # where peer-kubernetes-components is app/stacks/peer-kubernetes-components

## Terrafile

To use more modules, add them to the [Terrafile](https://terraspace.cloud/docs/terrafile/).