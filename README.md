# CodeBuildCachingDemo

## Deploy

```sh
aws cloudformation create-stack \
    --stack-name codebuild-cacheing-demo \
    --capabilities CAPABILITY_IAM \
    --template-body file://template.yaml
```
