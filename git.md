## Gitとは
* Git…バージョン管理システム。Gitは基本的にコマンドラインツールだが、分かりづらいためGithubやGUIツールを使った方がいい。
* GitHub…Gitはコマンドラインツールで分かりづらいため、WEB上で分かりやすくしたツール。リーモートリポジトリを作ることができる。他にもGitLabなどがある。
* GitKraken…Gitをより分かりやすくしたGUIツール。ローカルリポジトリの状態が分かる。他にもSourceTreeなどがある。

## コンフリクトとは
* コンフリクトとは、例えばリモートから落としてきたファイルを編集していた場合で、他の人も同じファイルを編集してリモートにプッシュすると起きる。
* コンフリクトが起きたら、他のメンバーの修正箇所は必ず残す、他のメンバーの修正に対して影響がないなら、自分の修正も残す。

## Git:resetとGit:revert
* ローカルでpushする前だったらresetを使い、pushした後だったらrevertを使う。pushした後にresetを使うと、リモートの履歴に残らず、改変することになるので危険。

## Gitkrakenでローカルリポジトリを作った後でGithubで先に作ったリモートリポジトリを登録したいとき。
* Gitkrakenのリポジトリが表示されている画面のREMOTEのところで+ボタンを押す。
* URLタブにしてNameには適当な名前(REMOTEで表示される名前、例githubなど)をPullURLにはGithubのリポジトリのhttpsのクローンURLの貼り付けて、Add Remoteボタンを押す。

## sshでgit cloneする。
* ssh -T git@github.comでyes/no聞かれるからyesでHi○○！とならなかったらgithubとは接続されてない。macのターミナルやvagrantでは接続済み。dockerを使うときはまたやらなくちゃいけないかも。
## 鍵を入れるフォルダに移動
* cd ~/.ssh
## 以降以下の記事を参考にした。
* https://qiita.com/shizuma/items/2b2f873a0034839e47ce#%E8%BF%BD%E8%A8%98-2015531
* vagrantではクリップボードにコピーできなかったので、以下のコマンドで表示してそのままコピーした。
## githubへの登録終わったら、もう一度接続を確認してみる。
## クローン作りたいディレクトリに移動してgit clone ○○

## ブランチを指定してpushしたい時
* git push origin test(ローカルブランチ):test(リモートブランチ)

## git pushしたときに「The requested URL returned error: 403」
* 以下のコマンドで解決
* git remote set-url origin git@github.com:Kenma-Kuribayashi/Laravel-Sample.git

## その他
* ファイルを編集をしたときはWorking状態、この状態でaddするとステージング状態となり、commit対象となる。commitされるのはステージングエリアにあるファイルのみ。
