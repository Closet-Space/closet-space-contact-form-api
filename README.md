# Closet Space contact form API
## Prerequisites
* AWS SAM
* Python 3.8
* S3 bucket created for deploy (we need a centralized account)

## Deploy
```bash
sam build

sam package --s3-bucket <NAME OF DEPLOY S3 BUCKET> --output-template-file out.yaml --region us-east-1

sam deploy --template-file out.yaml --stack-name ClosetSpaceContactForm --region us-east-1 --no-fail-on-empty-changeset  --capabilities CAPABILITY_NAMED_IAM