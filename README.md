# terraform-backend-cfn-template

Terraformに必要なS3とDynamoDBを初期化するためのテンプレートです

1. 以下を踏む

https://ap-northeast-1.console.aws.amazon.com/cloudformation/home?region=ap-northeast-1#/stacks/create/review?templateURL=https://raw.githubusercontent.com/ispec-inc/terraform-backend-cfn-template/master/cfn.yaml&stackName=TerraformInit&param_AppName=`Your App Name`

2. aws cliで作成
```
aws cloudformation create-stack --template-body https://raw.githubusercontent.com/ispec-inc/terraform-backend-cfn-template/master/cfn.yaml \
 --stack-name TerraformInit \
 --parameters ParameterKey=AppName,ParameterValue=`YourAppName`
```
