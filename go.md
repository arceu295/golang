Golang
=======

```
The "go-outline" command is not available. Run "go get -v github.com/ramya-rao-a/go-outline" to install.
```

gocode
  gopkgs
  go-symbols
  guru
  gorename
  gotests
  gomodifytags
  impl
  fillstruct
  goplay
  godoctor
  dlv
  gocode-gomod
  godef
  goreturns
  golint
  
deferred function will push into stack and run inverse

log.SetFlags(0)



### Deferred Function

When a function call is deferred, it is not executed immediately. \
It will be pushed into a defer-call stack maintained by its caller goroutine.

```go
    import "fmt"

    func main() {
        defer fmt.Println("The second line.")
        fmt.Println("The first line.")
    }
```

```go
    func nestingFunction(n int) (r int) {
        defer func() {
            r += n
        }()

        return n + n // r = n + n
    }

    log.Print(nestingFunction(5)) // 15
```
