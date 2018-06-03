# リポジトリの作成
GitHubで自分のページに移動し, "New"をクリックする.

<img src="/img/005_github_basic_operation/001.png" width="600">

"Repository name"に任意の名前を入力し(今回の場合は"hello-git"), "Create repository"をクリックする.

<img src="/img/005_github_basic_operation/002.png" width="600">

以下のような画面が出たら成功である.

<img src="/img/005_github_basic_operation/003.png" width="600">

# ローカルリポジトリに追加

// TODO: リモートリポジトリのリンクをコピーする作業

基本的にファイル作成・編集・削除などの作業はローカルリポジトリで行う.  
その変更内容をリモートリポジトリに反映させるには, ローカルリポジトリに対してリモートリポジトリへの参照を追加する必要がある.  
要約すると, ローカルリポジトリに先ほど作成したリモートリポジトリのURLを追加するということである.

ターミナルで下記のコマンドを実行すると, ローカルリポジトリに対してリモートリポジトリが"origin"という名前で登録される.  
ちなみに, "origin"以外の名前を付けても良いが, 慣習的に"origin"と付けられることが多い.

```bash
$ git remote add origin <リモートリポジトリのURL>
```

ローカルリポジトリに登録されているリモートリポジトリの名前やそれに対応するURLを確認する場合は,

```bash
$ git remote -v
```

とコマンドを入力し, 実行する.

// TODO: git remote -v コマンドの実行結果を貼り付けてほしい

# pushする
pushと呼ばれる操作を行うことで, ローカルリポジトリの変更内容をリモートリポジトリに反映させることができる.

まず,pasta.txtを作成する.

```bash
$ touch pasta.txt

$ echo パスタを茹でました. > pasta.txt
```

作成したファイルをステージングする.

```bash
$ git add .

$ git status(確認)
```

コミットする.

```bash
$ git commit -m "Initial commit" -m "close #1"
```

pushする.

```bash
$ git push (origin master)
```

<img src="/img/005_github_basic_operation/008.png" width="600">

<img src="/img/005_github_basic_operation/009.png" width="600">


# pullする
pullすることでリモートリポジトリの内容をローカルリポジトリに反映させることができる.

(基本GitHub上で作業することはありません.)

GitHub上でpasta.txtの内容を変更する.









# issueの作成
issueは日本語で「問題」や「課題」を指す言葉で, プロジェクトで発生したバグや新機能・改善点等の要望をissueとして一元管理することでプロジェクトの見通しを良くするための機能である.

新たにissueを作成する際は"New issue"をクリックする.

<img src="/img/005_github_basic_operation/004.png" width="600">

そして, issueのタイトルとその説明を記述し, "Submit new issue"をクリックすることでissueが作成される.

<img src="/img/005_github_basic_operation/005.png" width="600">

このとき, 右側にある"Assignees"からissueの担当者を割り当てることができたり, 同じく右側にある"Labels"からissueの分類をすることもできる.

<img src="/img/005_github_basic_operation/006.png" width="600">

# cloneする
誰かがGitHub(など, インターネット上)に公開したリポジトリを自分のPCに複製(ダウンロード)することをGitではcloneと呼ぶ.  
cloneするときは"Clone or Download"をクリックし, URLをコピーする.  

<img src="/img/005_github_basic_operation/007.png" width="600">

コピーしたら, ターミナルやGitBashで以下のコマンドを入力する.

```bash
$ git clone https://github.com/takashi0602/hello-github.git
```

これでcloneが完了した.


### forkする
forkとは,既存のpublicリポジトリの複製を自分のGitHub内に作成することである.

今回はhello-githubのリポジトリをforkする.
url：https://github.com/takashi0602/hello-github

右上にForkボタンがあるのでそれを押下する.

<img src="/img/005_github_basic_operation/010.png" width="350">

forkが終わると左上のところに「forked from takashi0602/hello-github」とfork元が記載される.

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
