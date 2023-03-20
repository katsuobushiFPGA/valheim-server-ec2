## このリポジトリについて  
下記の素晴らしいDockerイメージを Docker composeで使用したリポジトリである。  
https://hub.docker.com/r/lloesche/valheim-server  

## 使い方
1. .env.exampleをコピーします。
```
cp .env.example .env
```
2. .envの設定
DockerHubに記載されている「Environment Variables」を参考に設定します。  

設定例: 
```
SERVER_NAME=soloserver
SERVER_PASS=secret
SERVER_PUBLIC=false
WORLD_NAME=soloworld
TZ=Asia/Tokyo
BACKUPS_DIRECTORY=/backup
BACKUPS_MAX_COUNT=3

DATA_PATH=$HOME/valheim-server-ec2/data
CONFIG_PATH=$HOME/valheim-server-ec2/config
```
※他にも設定可能な変数があるのでお好みで。  
必要なものだけ設定しています。  

3. イメージをビルドし立ち上げます。
```
docker compose up -d
```