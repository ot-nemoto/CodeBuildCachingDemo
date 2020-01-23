# CodeBuildCachingDemo

## Overview

- CodeBuildでキャッシュ機能を有効にした場合の検証デモ
- Deployすることで、以下のCodeBuildが作成される
  - \<codebuild-caching-demo>-no-cache : キャッシュをしないCodeBuild
  - \<codebuild-caching-demo>-s3-cache : S3にキャッシュするCodeBuild（キャッシュ対象は `~/.ivy2`、`~/.cache`、`~/.sbt`）

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
