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

```bash
$ git --version
git version 2.15.1 (Apple Git-101)
```

のようにGitのバージョン情報が表示されればOK.

# GitのGUIアプリケーション

<img src="/img/003_install_git/001.png" width="300">

基本的にGitはCUIで操作するが, [Sourcetree](https://ja.atlassian.com/software/sourcetree
)など, GUIで操作するためのアプリケーションも多数用意されている.  
しかし, Gitの真価を発揮させるためにはCUIのGitを使いこなす必要があるため, 今回はCUIで学習していく.

# GitHubのDesktopアプリケーション

<!-- アイコン -->

Webブラウザ上でも不自由なくGitHubを操作できるが, [GitHub Desktop](https://desktop.github.com/)と呼ばれるGitHubのデスクトップアプリケーションも用意されている.

<!-- アイコン -->
