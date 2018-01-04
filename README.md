# AWS AMI Region Mapper
This script will help you search for Amazon Web Services Machine Images (AMIs) and build region maps suitable for including in Cloudformation Templates.

## Usage
You will need credentials configured for the AWS CLI or Boto3.

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

## Sample output
This run shows how to get a region mapper for the latest Amazon Linux in json:

```
$ aws_ami_region_mapper -a -j
Creating region map for...
2018-01-03T19:04:51.000Z	ami-5583d42f	amzn-ami-hvm-2017.09.1.20180103-x86_64-gp2	Amazon Linux AMI 2017.09.1.20180103 x86_64 HVM GP2
{
    "AWSRegionToAMI": {
        "ap-northeast-1": {
            "AMI": "ami-19910c7f"
        },
        "ap-northeast-2": {
            "AMI": "ami-7bef4f15"
        },
        "ap-south-1": {
            "AMI": "ami-4c045023"
        },
        "ap-southeast-1": {
            "AMI": "ami-1c99ee60"
        },
        "ap-southeast-2": {
            "AMI": "ami-33996b51"
        },
        "ca-central-1": {
            "AMI": "ami-e5cc4981"
        },
        "eu-central-1": {
            "AMI": "ami-06a83869"
        },
        "eu-west-1": {
            "AMI": "ami-075eca7e"
        },
        "eu-west-2": {
            "AMI": "ami-63243c07"
        },
        "eu-west-3": {
            "AMI": "ami-8715a2fa"
        },
        "sa-east-1": {
            "AMI": "ami-9582c1f9"
        },
        "us-east-1": {
            "AMI": "ami-5583d42f"
        },
        "us-east-2": {
            "AMI": "ami-e81b308d"
        },
        "us-west-1": {
            "AMI": "ami-2f99984f"
        },
        "us-west-2": {
            "AMI": "ami-a142e9d9"
        }
    }
}
```

And for the latest Windows Server 2012 AMI in Yaml format:

```
$ aws_ami_region_mapper -w -y
Creating region map for...
2017-12-13T21:47:36.000Z	ami-e443379e	Windows_Server-2012-R2_RTM-English-64Bit-Base-2017.12.13	Microsoft Windows Server 2012 R2 RTM 64-bit Locale English AMI provided by Amazon
AWSRegionToAMI:
  ap-northeast-1:
    AMI: ami-e95ad78f
  ap-northeast-2:
    AMI: ami-a83492c6
  ap-south-1:
    AMI: ami-34fab25b
  ap-southeast-1:
    AMI: ami-4bcaaa37
  ap-southeast-2:
    AMI: ami-21e31543
  ca-central-1:
    AMI: ami-21b30945
  eu-central-1:
    AMI: ami-8c57dce3
  eu-west-1:
    AMI: ami-811a9ef8
  eu-west-2:
    AMI: ami-217b6245
  eu-west-3:
    AMI: ami-8750e7fa
  sa-east-1:
    AMI: ami-eb91d787
  us-east-1:
    AMI: ami-e443379e
  us-east-2:
    AMI: ami-c24e66a7
  us-west-1:
    AMI: ami-fc2e2a9c
  us-west-2:
    AMI: ami-aca706d4
```
