# bitbucket監視用シェルスクリプト

## 概要
bitbucketのリポジトリを自動監視・最新コミットの更新があればgit fetch/git mergeします。
利用・改造等は自己責任でお願いします。

## 必要パッケージ

### [stedolan/jq](https://github.com/stedolan/jq)

- /usr/local/bin版インストール方法
```
sudo curl -o /usr/local/bin/jq http://stedolan.github.io/jq/download/linux64/jq
sudo chmod +x /usr/local/bin/jq
```

- /usr/bin版インストール方法
```
sudo curl -o /usr/bin/jq http://stedolan.github.io/jq/download/linux64/jq
sudo chmod +x /usr/bin/jq
```

## 使い方
```
cd /path/to/app
git clone https://github.com/aozora0000/shell_deployment_bitbucket.git ./service
chmod -R 644 ./service/*

vi ./service/deploy #設定は下記を参照
./service/deploy &
```
## 設定 (./service/deploy)
### [bitbucket](https://bitbucket.org/)の設定
```
vi ./service/deploy

################################
# Bitbucket Setting
################################
OWNER=""            #bitbucketのオーナー名
REPOS=""            #bitbucketのリポジトリ名
USER=""             #bitbucketのユーザー名
PASS=""             #bitbucketのパスワード名
```

### [Idobata.io](https://idobata.io/)の設定
```
################################
# Idobata Setting
################################
IDOBATA_ENDPOINT="" #idobataのエンドポイントURL
DEPLOY_MESSAGE='<span class="label label-success">success</span><br>デプロイ完了しました。'
```

### AUTHROR
Kohei Kinoshita

### LICENCE
MIT
