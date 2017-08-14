# User登録をできるようにする

## やること

とりあえずユーザー登録と認証ができるようになればOK。OAuthとかもできたら最高だけど…マストではないくらいの規模感。  
前提として、railsのインストールとか作業環境的なのは終わってることにする。

## 参考サイト

http://qiita.com/Salinger/items/873e3c667462746ae707

## Gemのインストール

これが必要っぽいので`Gemfile`に書いておく。

```Gemfile
gem 'devise'
```

インストールはこれでできる感じかな
```bash
docker-compose run --rm web bundle install --path vendor/bundle
```

vendor以下には外部ライブラリが入ってるらしい。
> ライブラリや他のアプリケーションで共有するような外部ライブラリを格納するディレクトリ

はいったっぽい。
```
Installing devise 4.3.0
Bundle complete! 16 Gemfile dependencies, 68 gems now installed.
Bundled gems are installed into ./vendor/bundle.
```

とおもったら入ってないかも
```
tmk-mac@tmk-mac:docker_rails_training [master]$ docker-compose run --rm web gem list | grep device
Starting dockerrailstraining_db_1 ... done
```
