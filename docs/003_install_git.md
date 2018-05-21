# Gitのインストール

### Macでインストールする場合

https://git-scm.com/download/mac からダウンロードし, インストールする.

<!-- TODO: もう少し詳しく -->

macOS用のパッケージ管理システムのHomebrewが入っている場合なら,

```bash
$ brew install git
```

でインストールすることが可能.

### Windowsでインストールする場合

https://git-scm.com/download/win からダウンロードし, インストールする.

<!-- TODO: もう少し詳しく -->

### Linux/UNIXでインストールする場合

Debian系ならapt, Red Hat系ならyumでインストールする.  
詳しくは https://git-scm.com/download/linux を参照.

### Gitがインストールされているかを確認

macOSならターミナル, WindowsならGit Bash, Linux/UNIXなら端末を開き, `git --version` と入力する.

```
$ git version
git version 2.15.1 (Apple Git-101)
```

のようにGitのバージョン情報が表示されればOK.
