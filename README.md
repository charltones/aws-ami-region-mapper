# AWS AMI Region Mapper
This script will help you search for Amazon Web Services Machine Images (AMIs) and build region maps suitable for including in Cloudformation Templates.

## Usage
You will need credentials configured for the AWS
```
usage: aws_ami_region_mapper [-h] [-a | -w | -d DESCRIPTION] [-l | -j | -y]

Find AWS AMIs and build region maps

optional arguments:
  -h, --help            show this help message and exit
  -a, --amazon-linux    Get latest Amazon Linux AMI
  -w, --windows-2012    Get latest Windows Server 2012 AMI
  -d DESCRIPTION, --description DESCRIPTION
                        Filter based on description
  -l, --list            output a list of matching AMIs
  -j, --json            output a json region map
  -y, --yaml            output a yaml region map
```

## How to get it
`pip install aws-ami-region-mapper`