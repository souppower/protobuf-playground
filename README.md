### preparation

https://github.com/protocolbuffers/protobuf/releases からリリースをダウンロードして、`/usr/local` に配置。
PATH にも追加しておく。

`protoc --version` が呼べることを確認。

`go get -u google.golang.org/protobuf` も必要かも。

```bash
go install google.golang.org/protobuf/cmd/protoc-gen-go@latest

protoc -I=./ --go_out=./ ./addressbook.proto

# or

protoc *.proto \
  --go_out=. \
  --go_opt=paths=source_relative \
  --proto_path=.
```

https://developers.google.com/protocol-buffers/docs/gotutorial
