
# VS Code Go Snippets
-------------------

Autocompletion snippet for golang

## Snippets

Below is a list of all available snippets and the triggers of each one.

### General
| Prefix  | Content |
| :------- | ------- |
| `fp`   | println `fmt.Println()`|
| `hws`   | hello world `"package main func main(){fmt.Println("Hello World!") "}"` |
| `ifs`   | if condition `if $0 {} `|
| `ifels`   | if else condition `"if $0 {} else {}"`|
| `sws`   | switch `switch $0 {case 1:}`|
| `frs`   | for range `for k,v:= range $0 {}"` |
| `fus`   | function `func $0 ($1,error) {return $1,err}` |
| `ss`   | struct `type $0 struct {}` |
| `grs`| go routine `go func() {fmt.Println($0)}() time.Sleep(time.Second)`|
| `grcs`| go channel `messages := make(chan string) go func() { messages <- "ping" }() msg := <-messages fmt.Println(msg)`|
| `grbcs`| go buffer channel `messages := make(chan string, 2) messages <- "buffered" messages <- "channel" fmt.Println(<-messages) fmt.Println(<-messages)`|
| `pp`| go ping pong `pings := make(chan string, 1) pongs := make(chan string, 1) ping(pings, "passed message") pong(pings, pongs) fmt.Println(<-pongs)} func ping(pings chan<- string, msg string) {pings <- msg} func pong(pings <-chan string, pongs chan<- string) { msg := <-pings pongs <- msg }`|
| `grj`| go job channel `jobs := make(chan int, 5) done := make(chan bool) go func() {for { j, more := <-jobs if more { fmt.Println("received job", j) } else { fmt.Println("received all jobs") done <- true return } } }() for j := 1; j <= 3; j++ { jobs <- j fmt.Println("sent job", j) } close(jobs) fmt.Println("sent all jobs") <-done`|
