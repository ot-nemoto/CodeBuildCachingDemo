# CodeBuildCachingDemo

## Deploy

```sh
aws cloudformation create-stack \
    --stack-name codebuild-cacheing-demo \
    --capabilities CAPABILITY_IAM \
    --template-body file://template.yaml
```

**Parameters**

|ParameterKey|Type|DefaultParameterValue|Description|
|--|--|--|--|
|Name|String|codebuild-caching-demo|プロジェクト名|
|GitHubRepository|String|https://github.com/nemodija/hello-scala-world-by-playframework.git|ビルド対象リポジトリURL|
