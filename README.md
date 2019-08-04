# API Gateway CF

## Problems Observed
- DynamoDB was configured to use a hard-coded table instead of the one with variable.
- Lambda function wasn't given permission to access DynamoDB

## Nice to have
- Security token to be included in request
- Data objects to validate inputs

## CloudFormation Deployment
```
aws cloudformation deploy --stack-name test --template-file ./cf-template.yaml --parameter-overrides MyName=ray --capabilities CAPABILITY_IAM
```

## Local Test with Curl
```
curl -i -X POST https://2pbs4pojll.execute-api.ap-southeast-2.amazonaws.com/v1/add_new \
-H "Content-Type: application/json" \
-d '{ "team_country":"au", "team_name":"test", "team_desc":"test", "team_rating":"a" }'
```
