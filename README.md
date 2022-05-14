# 概要

Linuxの練習

## 起動方法

1. コンテナ作成
```
$ cd docker
$ docker build -t linux_practice .
```

2. コンテナ起動
```
$ docker run --rm -it -p 13389:3389 -p 10022:22 --name linux_practice_con linux_practice
$ docker exec --rm -it linux_practice_con /bin/bash
```

3. GUIを確認

localhost:13389

* ログイン
（ID：my-ubuntu、PASS：my-Password)

4. SSH

localhost:10022で確認可能
ただし、秘密鍵が必要。

もちろん、SSHのポートも10022で指定する。

## rootについて

Password: super

# 教科書

Linux標準教科書

ITインフラを学習できるハンズオン学習サービス | Envader(エンベーダー) https://envader.plus/?gclid=Cj0KCQjwpv2TBhDoARIsALBnVnl2a4R051pwprJm57nivQ6ksJzqBO-bVHbJAwWP3nDNjRPIAF7F9DQaAt9WEALw_wcB

## CentOsについて

上記の教科書はCentOSを使うが...

8もサポートが終了していた。
Dockerで構築してGUIまで入れて色々試したかったが、最新版を入れてGUIまで入れる方法がよくわからない。
→パッケージを入れようとするも、コマンドが失敗してしまう。

## 学習方法

1. ローカルに偶然いれていたCentOS8を使う。
2. いっそのことUbuntuを使ってみる

## 環境構築(CentOS)

もうDockerでコンテナを作ってGUIを入れるのはあきらめた。
素直にローカルに入れる。

## 環境構築(Ubuntu)

このリポジトリのDockerfileからコンテナを作ればよい。

### 参考

Rosyuku/ubuntu-rdp: リモートデスクトップ接続とSSH接続が可能なUbuntu:18.04のコンテナです。 https://github.com/Rosyuku/ubuntu-rdp