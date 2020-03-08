docker-java
====

## Description

DockerでMySQLとApacheを起動します。Apacheからはproxy_ajpを利用してTomcatに転送しています。

### ディレクトリ構造
```
.
├── docker
│   ├── apache （Webサーバー）
│   │   ├── conf.d (apacheの設定ファイル)
│   │   └── logs （apacheのログ）
│   ├── mysql （DBサーバー）
│   │   ├── conf.d (mysqlの設定ファイル)
│   │   ├── data (mysqlのデータファイル)
│   │   ├── init （mysqlの初期DDL）
│   │   ├── logs （mysqlのログ）
│   │   └── script （mysql関連のスクリプト）
│   ├── .env
│   └── docker-compose.yml
├── src (ソースファイル)
├── tools
│   ├── eclipse (IDE)
│   ├── java (JDK)
│   ├── tomcat (APサーバー)
│   ├── maven (Maven)
│   ├── gradle (Gradle)
│   └── workspace (Eclipseのワークスペース)
├── public （公開ディレクトリ）
│   └── thumb (アップロードした写真)
└── dc.sh （Dockerの起動用スクリプト）
```

## Demo

## VS. 

## Requirement

## Usage

### DockerWindows(WSL)を利用している場合は以下の設定が必要です。
$ vi ~/.bashrc
``` 
export DOCKER_HOST=tcp://localhost:2375
```

$ sudo vi /etc/wsl.conf
``` 
[automount]
root = /
options = "metadata"
```

### Eclipseは以下のURLから、「Pleiades All in OneのJava-FullEdition」をダウンロードしてtoolsディレクトリ以下に配置してください。
https://mergedoc.osdn.jp/

### Maven
https://maven.apache.org/

### Gradle
https://gradle.org/

### 使い方
$ dc.sh -h
```
Usage:  dc.sh [command] [<options>]

Options:
  stats|st                 Dockerコンテナの状態を表示します。
  init                     Dockerコンテナ・イメージ・生成ファイルの状態を初期化します。
  start                    すべてのDaemonを起動します。
  stop                     すべてのDaemonを停止します。
  mysql login              MySQLデータベースにログインします。
  mysql export             MySQLデータベースのdumpファイルをエクスポートします。
  --version, -v     バージョンを表示します。
  --help, -h        ヘルプを表示します。
```

## Install

```
./dc.sh start
open https://localhost/
```

## Contribution

## Licence

[MIT](https://github.com/isystk/docker-java/LICENCE)

## Author

[isystk](https://github.com/isystk)


