rails-dokcer-sample
=====

## 起動方法

**Docker version 1.9 以上**

* コンテナのイメージのビルド

```
docker build --build-arg SECRET_KEY_BASE=$(bundle exec rake secret) -t rails-dokcer-sample .
```

* app.1 コンテナの起動

```
docker run -d --name app.1 --hostname app.1 -p 3000:3000 -e DATABASE_URL="Your Database url" rails-dokcer-sample
```

* app.2 コンテナの起動

```
docker run -d --name app.2 --hostname app.2 -p 3001:3000 -e DATABASE_URL="Your Database url" rails-dokcer-sample
```

## Deploy方法

・・・
