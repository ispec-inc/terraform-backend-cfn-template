# terraform-backend-cfn-template

Terraformに必要なS3とDynamoDBを初期化するためのテンプレートです

方法は二つあります。好きな方を選んでください

1. 以下を踏む

https://ap-northeast-1.console.aws.amazon.com/cloudformation/home?region=ap-northeast-1#/stacks/create/review?templateURL=https://ispec-public.s3.ap-northeast-1.amazonaws.com/cfn-terraform-init-template.yaml&stackName=TerraformInit

2. aws cliで作成
```
aws cloudformation create-stack --template-body https://ispec-public.s3.ap-northeast-1.amazonaws.com/cfn-terraform-init-template.yaml \
 --stack-name TerraformInit \
 --parameters ParameterKey=AppName,ParameterValue=`YourAppName`
```
