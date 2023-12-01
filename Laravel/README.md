# Create Laravel development for docker compose

```shell
# 環境ビルド(初回のみ)
docker compose up -d --build

# コンテナの開始
docker compose start

# PHPコンテナにログイン
docker compose exec php bash

# コンテナの終了
docker compose stop
```
