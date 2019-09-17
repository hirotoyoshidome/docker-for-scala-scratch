# docker_for_scala_scratch

## 開発環境をDockerで整える
Scalaでスクリプト書く時にJDKから揃えるのが面倒なので
Docker化する

Doker Hubに公式のDockerfileが見つからなかったため、
Javaの公式のイメージからscalaをインストールして作成する

### 使い方

```
docker build -t dev_env_scala .
docker run -it -w /usr/src -v $PWD:/usr/src --rm dev_env_scala:latest /bin/bash
```

カレントディレクトリに配置したファイルを実行できます
例)

```
sbt
run
```
※最初のsbtコマンド実行時はjarファイルをたくさんダウロードするため、時間がかかります

REPLで試すときは
```
sbt console
```
