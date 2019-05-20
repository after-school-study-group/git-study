# Gitのインストール

### Macでインストールする場合

MacにはGitが標準搭載されているため, 特にインストール作業を行う必要が無いが, もしインストールされていなかったり最新版に更新したい場合は以下の手順に従う.

Macに後からGitをインストールする方法は主に２つある.

１つ目は https://git-scm.com/download/mac からダウンロードし, インストールするという方法である.

２つ目はmacOS用のパッケージマネージャであるHomebrewがインストールされている場合にしかできないが, ターミナル上で

```bash
$ brew install git
```

とコマンドを入力してインストールするという方法である.  
Homebrewのインストール方法に関しては https://brew.sh/index_ja を参照.  
Homebrewは他にも便利なアプリケーションをインストールできるため, 暇な時間にインストールしておくと良い.

### Windowsでインストールする場合

https://git-scm.com/download/win からダウンロードし, インストールする.

### Linux/UNIXでインストールする場合

Debian系ならapt, Red Hat系ならyumでインストールする.  
詳しくは https://git-scm.com/download/linux を参照.

### Gitがインストールされているかを確認

macOSならターミナル, WindowsならGit Bash, Linux/UNIXなら端末を開き, `git --version` と入力する.

```bash
$ git --version
git version 2.15.1 (Apple Git-101)
```

のようにGitのバージョン情報が表示されれば正常にインストールができている.
