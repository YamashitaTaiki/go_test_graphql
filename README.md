# go graphqlの学習を行うレポジトリ
goのテストを行うレポジトリ

# go環境構築
go言語構築、grapqhql
- Goインストール
https://qiita.com/suke_masa/items/2d6805b09105b00656e0
- graphql構築
https://gqlgen.com/getting-started/

- Create a directory for your project, and initialise it as a Go Module:
```
mkdir gqlgen-todos
cd gqlgen-todos
go mod init github.com/[username]/gqlgen-todos
```

- To automatically add the dependency to your go.mod run
```
go mod tidy
```
- grapqhql用ソース取得
```
go get -d github.com/99designs/gqlgen
go run github.com/99designs/gqlgen init
```
- graphqlサーバ起動
```
$ go mod tidy
$ go run ./server.go
```

- スキーマ更新後自動生成
```
go run github.com/99designs/gqlgen
```

# redis環境構築
- goでredisライブラリget
```
go get -d github.com/go-redis/redis/v8
```
- dockerでredis起動
```
docker run --name redis -d -p 6379:6379 redis
```
- コンテナに入りredisに接続
```
docker ps -a
b7a1b3f612c9
docker exec -it b7a1b3f612c9 bash
redis-cli
keyをセット
127.0.0.1:6379> SET key1 value1
OK
```
- 実装から出力
```
A-20011671:test_graphql s15715$ go run ./redis/test_redis.go 
key1 value1
```
