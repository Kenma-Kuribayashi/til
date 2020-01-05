# エラー備忘録

## Composer使用時に「proc_open(): fork failed errors」エラーが出た時の対処法

* 容量不足の可能性

## php artisan serveなどでサーバーが立てられない時は以下でサーバーを立てる。127.0.0.1がなぜか使えないため。

php -S 192.168.33.10:8000 -t public
