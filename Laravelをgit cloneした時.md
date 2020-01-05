## ターミナルでvagrantにログインする。
## サイバーダックでクローンを置きたいディレクトリを作成する。
## 作成したディレクトリに移動してgit clone https
## 以下のコマンドでPHP7.1系をインストールする。
* sudo yum install -y --enablerepo=remi-php71 php
## クローンしたホームディレクトリ(一番上のディレクトリ)に移動する。
## Composerのダウンロードのやつを貼り付けて実行する。
## 以下のコマンドでvendor(Laravelのライブラリ系)をインストールする。
* php composer.phar install
## 以下のコマンドで.envファイルのAPP_KEYに自動でapp_keyが入力される。
* php artisan key:generate
## サーバーは以下で立てる。127.0.0.1は使えない。
* php -S 192.168.33.10:8000 -t public
