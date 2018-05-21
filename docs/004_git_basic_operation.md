# Gitの初期設定
Gitにユーザネームとメールアドレスを設定する(初回のみ).

```
$ git config --global user.name "Taro Tanaka"
$ git config --global user.email "taro@example.com"
```

ついでにデフォルトのエディタをVimに設定する(Vimは最高なので).

```
$ git config --global core.editor 'vim - c "set fenc=utf-8"'
```

# Gitリポジトリの作成

```
$ mkdir hello-git
$ cd hello-git
$ git init
```

`mkdir`や`cd`はLinuxコマンドなどと呼ばれるもので, Linuxコマンドはコマンドラインでファイルやディレクトリの操作を行うために用意されている.

|コマンド名|説明|
|:--|:--|
|mkdir|Make Directoryの略. 引数で指定した名前のディレクトリを作成する.|
|cd|Change Directoryの略. 引数で指定しパスのディレクトリに移動する.|

`git init`コマンドを叩くと, カレントディレクトリ以下に`.git`という隠しディレクトリを生成する.  
これにより, カレントディレクトリ以下にあるファイルはGitに管理され, Gitリポジトリという１つのまとまりとして扱われる.  
また, 「Gitに管理される」というのは, Gitの各種コマンドが使える状態であるということでもある.

# 大まかな流れ
