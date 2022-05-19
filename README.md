# 概要

Linuxの練習

## Docker使用をする場合のコンテナ起動方法

### コンテナ作成

```
$ cd docker
$ docker build . -t linux_practice
```

### コンテナ起動

```
$ docker run -it -d -p 53:53 -p 53:53/udp --name=linux_practice_con linux_practice /bin/bash
```

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