---
title: "Gitgubでよく使うコマンド"
date: 2021-06-13T03:46:01+09:00
draft: false
TableOfContents: true
weight: 1
---
#### ローカルリポジトリを作成
```shell
git init
```

※ローカルリポジトリはPC上にあるフォルダのこと



#### リモートリポジトリからプロジェクトをコピー

```shell
cd [ローカルリポジトリのパス]
```

```shell
git clone [リモートリポジトリパス] (例： https://github.com/neme/neme.git)
```

※リモートリポジトリはgithub上にあるフォルダのこと

git submodule add URL



#### ファイルの追加
```shell
git add 追加したいファイル名
```



##### git addの種類

```shell
git add .
```
すべてのファイル・ディレクトリ

```shell
git add *.拡張子
```
すべての.拡張子

```shell
git add -n
```
追加されるファイルを調べる

```shell
git add -u
```
変更されたファイルを追加する



##### addしたファイルを除外
```shell
git rm --cached
```

##### addの取り消し

```shell
git reset HEAD
```

```shell
git reset HEAD {file_name}
```



#### ファイルをcommit

```shell
git commit -a -m "コメント"
```
※commitは追加or変更したファイルをgitに登録すること

##### git commitの種類

```shell
git commit -a
```
 変更のあったファイルすべて

```shell
git commit --amend
```
直前のコミットを取り消す

```shell
git commit -v
```
 変更点を表示してコミット

#### ユーザー登録

ユーザー登録をしないとcommitできないので、ユーザー登録をしよう。

```shell
git config --global user.name "ユーザー名"
```
```shell
git config --global user.email メールアドレス
```


#### ファイル更新
```shell
git push origin master
```



#### ブランチ操作
※ブランチは分岐したファイルのこと。分岐したブランチは他のブランチの影響を受けない。

masterブランチが親で、masterブランチからどんどん分岐していく。分岐したブランチを他のブランチとマージすることで1つのブランチにまとめ直せる。

```shell
git branch [branch_name]
```

新しいブランチを作る

```shell
git checkout [branch_name]
```

ブランチの移動

```shell
git branch -d [branch_name]
```

ブランチの削除

```shell
git branch -m [branch_name]
```

現在自分がいるブランチ名の変更

```shell
git branch
```
ローカルブランチの一覧を確認
```shell
git branch -r
```
リモートブランチの一覧を確認
```shell
git branch -a
```
リモートとローカルのブランチ一覧を確認

```shell
git checkout -b branch_name origin/branch_name
```

リモートブランチへチェックアウト

#### 編集をマージ

master以外のブランチで編集した箇所をmasterに反映

```shell
git checkout [branch_name]
```

ブランチに移動

```shell
git commit -a -m "コメント"
```

変更ファイルをコミット

```shell
git checkout master
```

masterに移動

```shell
git merge [branch_name]
```

差分をマージ

```shell
git push origin master
```

ファイルの更新

```shell
git merge --abort
```

マージを取り消す

#### 差分を確認する

```shell
git diif
```

```shell
git diff HEAD^
```

最後のコミットからの差分を表示

```shell
git diff --name-only HEAD^
```

差分ファイルを表示

```shell
git diff file1.txt file2.txt
```

 特定フィイルの差分

```shell
git diff commit1 commit2
```

 コミットの差分

#### ログの表示

```shell
git log
```

コミットのログが見られる

```shell
git reflog origin/branch_name
```

 pushのログが見られる

#### ファイルの名前を変更

```shell
git mv [変更前のファイル名] [変更後のファイル名]
```

```shell
git commit -a -m "rename"
```

```shell
git push origin master
```

#### ファイルを削除

```shell
git rm [name]
```

特定のファイルorディレクトリの削除

```shell
git rm *
```

  全ファイルorディレクトリ

```shell
git commit -a -m "remove"
```

  削除をコミット

```shell
chgit push origin master
```

  削除を反映

#### 圧縮ファイルを作る

```shell
git archive --format=zip HEAD -o ./hoge.zip
```

現在のリポジトリのzipファイルを作る

## 参考

[【Git】基本コマンド - Qiita](https://qiita.com/konweb/items/621722f67fdd8f86a017)

[ブランチとは｜サル先生のGit入門【プロジェクト管理ツールBacklog】](https://backlog.com/ja/git-tutorial/stepup/01/)

