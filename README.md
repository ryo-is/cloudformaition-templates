## stackの作成

パラメータ `AccountID` は、 `eb deploy` する先のアカウントIDです。
`--region` でCloudFormationのStackを作成するリージョンを設定する

```
$ aws cloudformation create-stack --template-body file://codepipeline-template.yml \
    --stack-name cfn-test --region us-east-1 \
    --capabilities CAPABILITY_NAMED_IAM \
    --parameters ParameterKey=AccountID,ParameterValue=1234567890123
```

## stackの削除

`--region` で削除するCloudFormationのStackのリージョンを設定する

```
$ aws cloudformation delete-stack --stack-name cfn-test --region us-east-1
```