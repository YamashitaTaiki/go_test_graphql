# go graphqlの学習を行うレポジトリ
goのテストを行うレポジトリ

# 環境構築
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
