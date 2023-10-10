package name
`example.com/negaposi`

```
// 依存ライブラリをgo.modに追加
go mod tidy
```

```
// 実行
go run .
```

```
// localhostへのホスティング
// http://localhost:8080
go run github.com/hajimehoshi/wasmserve@latest ./

```

```
// コンパイル (negaposi.wasm)
example.com/negaposi 
env GOOS=js GOARCH=wasm go build -o negaposi.wasm example.com/negaposi
```

```
// バイナリを実行するためのファイル (wasm_exec.js)
cp $(go env GOROOT)/misc/wasm/wasm_exec.js ./
```
