# Gitの初期設定
Gitにユーザネームとメールアドレスを設定する(初回のみ).

```bash
$ git config --global user.name "Taro Tanaka"
$ git config --global user.email "taro@example.com"
```

ついでにデフォルトのエディタをVimに設定する(Vimは最高なので).

```bash
$ git config --global core.editor 'vim - c "set fenc=utf-8"'
```

# Gitリポジトリの作成

```bash
$ mkdir hello-git
$ cd hello-git
$ git init
```

`mkdir`や`cd`はLinuxコマンドなどと呼ばれるもので, Linuxコマンドはコマンドラインでファイルやディレクトリの操作を行うために用意されている.

|コマンド名|説明|
|:--|:--|
|mkdir|Make Directoryの略. 引数で指定した名前のディレクトリを作成する.|
|cd|Change Directoryの略. 引数で指定した名前のディレクトリに移動する.|

`git init`コマンドを叩くと, カレントディレクトリ以下に`.git`という隠しディレクトリを生成する.  
これにより, カレントディレクトリ以下にあるファイルはGitに管理され, Gitリポジトリという１つのまとまりとして扱われる.  
また, 「Gitに管理される」というのは, Gitの各種コマンドが使える状態であるということでもある.

# 大まかな流れ

<!-- 図 -->

Gitの管理下に置かれた実際に作業をしているディレクトリのことをワークツリーと呼ぶ.  
ここでファイルの作成や編集, 削除を行った後, 必要なファイルをステージングエリア(インデックスとも呼ぶ)にステージングする作業を行う.  
その後ステージングされたファイルをコミットする作業を行い, これで初めてGitリポジトリに変更履歴として残る.

# ステージングする

<!-- 図 -->

ステージングするにはまずなにかしらファイルを作成する必要があるため,

```bash
$ touch hello.txt
```

としてファイルを作成する.  
`touch`コマンドは引数で指定した名前のファイル名を作成するコマンドである.  

次にステージングを行う.  

```bash
$ git add .
```

`git add`コマンドでワークツリーにある変更されたファイルをステージングエリアにステージングすることができる.  
ここで, `.`(ドット)というのは, ワークツリーにあるファイルの変更を全てステージングエリアにステージングするという意味である.  
ここでは`.`(ドット)を使って全てのファイルをステージングしているが, ファイル名を指定して特定のファイルの変更のみステージングさせることもできる.

ちなみに, 作成, 変更, 削除などを行ったファイルの状態を確認するには, `git status`コマンドを使うと良い.

```bash
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	hello.txt

nothing added to commit but untracked files present (use "git add" to track)
```

ステージングされているファイルは'No commits yet'の下に, ステージングされていないファイルは'Untracked files'の下に表示される.

# コミットする

<!-- 図 -->

ステージングしたファイルはコミットと呼ばれる作業を行い, Gitの変更履歴に記録する必要がある.  
コミットにするには, `git commit`コマンドを使う.  
また, このときに`-m`オプションを付けることによってコミットに対するメッセージを残すことができる.

```bash
$ git commit -m "Initial commit"
[master (root-commit) 23bbb67] Initial commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 hello.txt
```

コミットによってGitに記録された変更履歴は, `git log`コマンドで確認できる.

```bash
$ git log
commit 23bbb672088c1eeaeb1a4c48e81256812edf02e7 (HEAD -> master)
Author: Kazuki Tobita <kazukiti201@gmail.com>
Date:   Tue May 22 18:53:08 2018 +0900

    Initial commit
...
```

閉じるときは`:q`と入力する.

# ブランチとは
開発用とリリース用を分けたい場合など, 同じアプリケーションでも状況に応じて切り分けたい場合がある.  
その問題を解決するのがGitにおけるブランチという概念である.  

<!-- 図 -->
