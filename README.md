# 概要

Linuxの練習

## 起動方法(失敗する)

1. コンテナ作成
```
$ cd docker
$ docker build -t linux_practice .
```

2. コンテナ起動
```
$ docker run -d --privileged --cgroupns=host -v /sys/fs/cgroup:/sys/fs/cgroup:rw -p 30000:3389 -p 30001:22 --name linux_practice_con linux_practice /sbin/init
$ docker exec -it linux_practice_con /bin/bash
```


# 教科書

Linux標準教科書

## CentOsについて

上記の教科書はCentOSを使うが...

8もサポートが終了していた。
Dockerで構築してGUIまで入れて色々試したかったが、最新版を入れてGUIまで入れる方法がよくわからない。

## 環境についての対応

1. ローカルに偶然いれていたCentOS8を使う。
2. いっそのことUbuntuを使ってみる

## 環境構築(仮)

1. コンテナを作成
2. コンテナ内で以下を実行
```
$ yum -y groupinstall "GNOME Desktop"
$ passwd
```