# S3-Create-React-App

A simple example of how to use AWS S3 to host your `create-react-app` application

Requirements:

__Node >=7.9__
__Python >=2.5__

To use this repo, follow the "first time setup" if you have never used the AWS CLI tool before. If you already have done this and have a bucket ready for hosting, just run the bash script noted at the bottom of the README anytime that you want to deploy changes.

* * *
## First Time Setup:

### Install the AWS CLI tools

`pip install --user --upgrade awscli`

### Enable communication with your S3 buckets via the CLI tool

`aws configure` << will prompt you for the following:

AWS Access Key ID [None]: SOMEASSORTMENTOFCHARS (required)
AWS Secret Access Key [None]: wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY (required)
Default region name [None]: us-west-2 (optional)
Default output format [None]: json (optional)

### Create your bucket and make it readable by all users
aws s3 mb s3://your_bucket_name --grants read=uri=http://acs.amazonaws.com/groups/global/AllUsers

### Install the necessary dependencies for this project

`npm install`

* * *
## Deployment Steps:

`sh deployToS3.sh your_bucket_name`



