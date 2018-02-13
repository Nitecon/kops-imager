# kops-imager
Repository to facilitate building kubernetes based images that are used by kops.

# TLDR Envars set whats the command
To run the building and push the image once you have your environment variables set run:
`packer aws-stretch.json` 

This will build the image on AWS for use in kops installations.

# AWS

Setting up in AWS requires that some environment variables are set prior to running packer and a specific image type

* AWS Key / Secret must be set up in order to continue, please see [How to create key/secret](https://aws.amazon.com/blogs/security/wheres-my-secret-access-key/) and [Setup AWS Environment Variables.](https://docs.aws.amazon.com/cli/latest/userguide/cli-environment.html)

* VPC and Subnet ID envars so we can spin up an image to build the required AMI's

```
export VPC_ID="vpc-YOURVPCID"
export SUBNET_ID="subnet-YOURSUBNETID"
```

