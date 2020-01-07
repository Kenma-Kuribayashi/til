# エラー備忘録

## Composer使用時に「proc_open(): fork failed errors」エラーが出た時の対処法

* 容量不足の可能性

## php artisan serveなどでサーバーが立てられない時は以下でサーバーを立てる。127.0.0.1がなぜか使えないため。

* php -S 192.168.33.10:8000 -t public

## マイグレーションしようとして1071 Specified key was too long;のエラーは、キーが767bytes超えちゃうというエラー。

* 文字の最大値を指定することで解決。$table->string('email', 191)->index();

## マイグレーションしようとして1050 Table 'password_resets' already existsのエラーは、既にこのテーブルがあるというエラー。

* 作ったテーブルを全削除し、再度マイグレーションで解決。
* php artisan migrate:fresh
