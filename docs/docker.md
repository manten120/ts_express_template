# docker についてメモ

## 参考にしたページ

### docker ドキュメント
- [英語](https://docs.docker.com/)
- [日本語](docs.docker.j)

### [いい加減docker-composeでlinksを使うのをやめてnetworkでコンテナ間名前解決をする](https://qiita.com/dyoshikawa/items/05d627b962da35f7d5b6)

docker-composeの`links`は不要。


> リンク機能（links）とは、他のサービスから到達可能なエイリアス（別名）を定義するものです。サービス間で通信するために必要ではありません。すなわち、 デフォルトでは、あらゆるサービスはサービス名を通して到達できます


```yml
service:
  app:
    links: # 不要
      - db # 不要
  db:
```

### [docker-compose up したコンテナを起動させ続ける方法](https://qiita.com/sekitaka_1214/items/2af73d5dc56c6af8a167)


`tty: true` で `docker-compose up -d` の `-d` が不要になる? → 不要にはならなかった。

`tty: true` が無いとコンテナの起動が継続しなかった。(expressサーバーを起動すれば継続するかも)

とりあえず、コンテナの起動を継続させるために `tty: true` が必要

## 起動方法

### docker-compose でコンテナをビルド・起動する
`docker-compose up -d`

### コンテナのなかに入る
`docker-compose exec app bash`

または `docker exec -it node16 bash`

## 停止方法

### コンテナ、イメージ、ネットワークを削除

`docker-compose down --rmi all`



