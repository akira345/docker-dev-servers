Dockerで開発に必要なRedmine、Jenkins、GitBucker、MySQLサーバ環境を一気に構築します。  

Jenkinsのホームディレクトリだけは権限の問題で個別に設定する必要があります。

```
# mkdir -p ./jenkins/jenkins
# chown 1000 ./jenkins/jenkins
```

を実行し、最初に作成してください。

docker-compose.ymlを適当に編集後  

docker-compose up -d  

してください。


本環境は以下のサイトなどを参考にしました。ありがとうございます。

Docker-ComposeでGitLabとRedmineとJenkinsを立ち上げる
http://qiita.com/nexkeh/items/02a4d6c33d884bda1b23


Docker で GitBucket 環境をつくる
http://qiita.com/japboy/items/be3f0bf8eb3b315de6ae


