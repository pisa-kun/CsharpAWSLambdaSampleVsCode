# VisualStudio Codeを使った AWS Lambda + .Net6(c#)のデプロイ

## Install Command

AWS Lambdaのグローバルツールをインストール
> $ dotnet tool install -g Amazon.Lambda.Tools

※the best command?
> $ dotnet tool install -g Amazon.Lambda.TestTool-6.0

テンプレートのインストール
> $ dotnet new -i Amazon.Lambda.Templates

サンプルファンクションの作成
> $ dotnet new lambda.EmptyFunction --name AWSLambdaDotnetNewPattern --profile default --region ap-northeast-1

## Deploy Command

> dotnet restore  
> dotnet lambda deploy-function AWSLambdaDotnetNewPattern --function-role lambda_exec_AWSLambdaSimpleSample --profile default

## Local Test Command

> dotnet lambda invoke-function AWSLambdaDotnetNewPattern --payload "morimori rinze"

## Unit Test Command

> cd test\Project.Tests\  
> dotnet test

---
[Reference](https://qiita.com/b-wind/items/4c84be345ba24588153b)
[Reference(準備込み)](https://engr-tie.net/posts/lambda-net6/prepare/)
[Reference(--payload)](https://qiita.com/M_Kagawa/items/1fcd499caf3ccda2495f)