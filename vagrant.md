## Vagrantとは
* ターミナルから vagrant up とコマンドを打つだけで、1度作った開発環境を構築することが可能。Vagrant は、VirtualBox に対して、仮想マシンの起動や操作、停止や破棄などの指示をしてくれる。

## VitualBoxとは
* 自分のPCに別のOSを実行できるようにする仮想化ソフトウェア。例えば、macでwindows環境を構築してその環境下でphpをインストールしたりできる。

## 学習を再開する時
* cd
* cd MyVagrant
* cd MyCentOS
* vagrant up
* vagrant ssh
* ファイル転送ツールを立ち上げて、ブックマークの「MyCentOS」をダブルクリック
* php -S 192.168.33.10:8000

## 学習やめるとき
* サーバーが立ち上がっている場合、「Ctl + C」
* exit
* vagrant suspend
* exit

## ローカルとの同期化
* ローカルにあるvagrantfilleを以下のように書き換えた。#はコメント表示なので#はとる必要がある。第一引数がローカル、第2がvagrant上。typeにvirtualboxを指定することでリアルタイムで同期化してくれる。
* config.vm.synced_folder "Laravel-Sample", "/home/vagrant/laravel_sample/Laravel-Sample", type: "virtualbox"
* 書き換えた後にvagrant reloadした。
* 参考は以下の通り。
* https://qiita.com/yusk24/items/96a0000716fed7ca62f6
* https://teratail.com/questions/171625
