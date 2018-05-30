## GitHubの基本操作

### リポジトリ作成
リポジトリとはファイルやディレクトリの状態を記録する場所だ.
GitHubではpublicリポジトリとprivateリポジトリを作成できる.今回はフリープランでサインアップしたのでpublicリポジトリしか作成できない.privateリポジトリは有料プランにするか、学生プランにすると作成できるようになる.

<img src="/img/005_github_basic_operation/001.png" width="600">

<img src="/img/005_github_basic_operation/002.png" width="600">

<img src="/img/005_github_basic_operation/003.png" width="600">

作成したリポジトリはリモートリポジトリといい,複数人で共有するためのリポジトリである.リモートリポジトリを自分のローカル環境にpullしたものをローカルリポジトリといい,作業する時はローカルリポジトリを触る.

### issue作成
issueとは,日本語で問題や課題という意味である.issueを作成することでプロジェクトの管理がしやすくなる.

<img src="/img/005_github_basic_operation/004.png" width="600">

<img src="/img/005_github_basic_operation/005.png" width="600">

<img src="/img/005_github_basic_operation/006.png" width="600">

issueの担当者（作業者）はAssigneesで決めることができる.

labelsを使用することでissueのジャンル分けがしやすくなる.

### pushの流れ
まず、リモートリポジトリをcloneする.cloneとは,既存のリポジトリを複製するための操作.
urlはCodeタブ内に記載されているのでコピーする.


<img src="/img/005_github_basic_operation/007.png" width="600">

コピーしたらターミナルまたはGitBashを開き,任意のディレクトリ内で以下のコマンドを叩く.

```
$ git clone https://github.com/takashi0602/hello-github.git
```

cdコマンドを使用しcloneしたディレクトリに移動する.

```
$ cd hello-github
```

pasta.txtを作成する.

```
$ touch pasta.txt

$ echo パスタを茹でました. > pasta.txt
```

作成したファイルをステージングする

```
$ git add .

($ git status)
```

コミットする.コミットをする際「close #1」とするとissue #1と紐付けされ.mergeされた時にissueもcloseされる.

```
$ git commit -m "Initial commit" -m "close #1"
```

pushする.pushすることでローカルリポジトリの内容がリモートリポジトリに反映させる.

```
$ git push (origin master)
```

<img src="/img/005_github_basic_operation/008.png" width="600">

<img src="/img/005_github_basic_operation/009.png" width="600">

### forkの仕方
<img src="/img/005_github_basic_operation/010.png" width="600">

<img src="/img/005_github_basic_operation/011.png" width="600">

### プルリク作成
<img src="/img/005_github_basic_operation/012.png" width="600">

<img src="/img/005_github_basic_operation/013.png" width="600">

<img src="/img/005_github_basic_operation/014.png" width="600">

<img src="/img/005_github_basic_operation/015.png" width="600">

### mergeのやり方
<img src="/img/005_github_basic_operation/016.png" width="600">

<img src="/img/005_github_basic_operation/017.png" width="600">

<img src="/img/005_github_basic_operation/018.png" width="600">

<img src="/img/005_github_basic_operation/019.png" width="600">

### コントリビュート
<img src="/img/005_github_basic_operation/020.png" width="600">
