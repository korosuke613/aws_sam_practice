## 圧縮

```powershell
Compress-Archive -Force -Path .\app-spec.yml, .\index.js -DestinationPath ./app.zip
```

## パッケージ化

```powershell
aws cloudformation package --template-file app-spec.yml --outpu
t-template-file app-spec.deploy --s3-bucket sam-practice
```

## デプロイ

```powershell
aws cloudformation deploy --template-file .\app-spec.deploy --s
tack-name db-sam-stack --capabilities CAPABILITY_IAM
```
