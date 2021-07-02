# Create web site hosting for a static website

The `web.yml` creates an AWS SSL Certificate, S3 bucket, and CloudFront distribution for a static website.

Replace `YOUR_DOMAIN_NAME` with your domain name in AWS Route 53.  
`HostedZoneId` must be your AWS Route 53 Hosted Zone Id.

````
aws cloudformation create-stack --stack-name domain-web --template-body file://./web.yml --parameters \
ParameterKey=DomainName,ParameterValue=YOUR_DOMAIN_NAME.com \
ParameterKey=HostedZoneId,ParameterValue=XXXXXXXXXXX```
````
