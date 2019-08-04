# API Gateway CF

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
