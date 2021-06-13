---
title: "Hugoでよく使うコマンド"
date: 2021-06-13T02:30:11+09:00
draft: false
TableOfContents: true
---

## 新しいサイトを作る
```shell
hugo new site サイトの名前
```



## Huhoのローカルサーバー立ち上げ

```shell
hugo server -w -D
```
-wはレンダリング　-Dは下書きも表示

## サーバーを停止
```shell
Ctrl+C
```

## 新しい記事を作る
```shell
hugo new content/記事のジャンル名/記事の名前.md
```



公開したい記事のdraftをfalseに書き換える

## publicフォルダを作る

```shell
hugo
```

Hugoコマンドを入力するとpublicフォルダが作られる



## Hugoのバージョンを確認する

```shell
hugo version
```

現在のHugoのバージョンの値が返ってくる



参考
>https://maku77.github.io/hugo/