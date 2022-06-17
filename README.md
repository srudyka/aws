the CloudFormation template is designed for creating the following resources:
- S3 bucket
- S3 bucket policy alowing only access for CloudFront
- CloudFront distribution
- Route 53 A record to CloudFront distribution


Examples of Execution:
1. with default params:
aws cloudformation create-stack --stack-name myteststack1 --template-body file://s3-cloudfront-route53.yaml
2. with params:
aws cloudformation create-stack --stack-name myteststack1 --template-body file://s3-cloudfront-route53.yaml --parameters ParameterKey=DomainName,ParameterValue=rudyka.org ParameterKey=HostedZoneId,ParameterValue=ZZZZZZZZZZZZZZZZZZZZZ ParameterKey=BucketName,ParameterValue=www.rudyka.org ParameterKey=CertificateArn,ParameterValue=arn:aws:acm:us-east-1:853416576884:certificate/ffae1a68-3b4a-43d7-8bf9-27cc27455358

