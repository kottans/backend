[![MIT Licensed][icon-mit]][license]
[![Awesome][icon-awesome]][awesome]
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

# Golang Runtime and Ecosystem

1. Read about how to get rid of `$GOPATH` in your projects using [Go modules](https://blog.golang.org/using-go-modules)
1. A brief walk-through a useful features of Go toolchain. [5 Helpful utilities in Go toolchain](https://medium.com/@yashishdua/5-helpful-utilities-present-in-go-toolchain-bc4ad5ed4e78)

---

1. Video. [Keith Randall - Inside the Map Implementation](https://www.youtube.com/watch?v=Tl7mi9QmLns)
1. Video. [Francesc Campoy - Understanding nil](https://www.youtube.com/watch?v=ynoY2xz-F8s)
1. [Go's work-stealing scheduler](https://rakyll.org/scheduler/)

1. In your `kottans-backend` repo `README.md`:

   5.1 add header `## Golang Runtime and Ecosystem`

   5.2 add answers to the following questions:

   - What value types are invalid for use as go `map` keys and why ?
   - Will this code compile ? Why ?

   ```go
   package main

   func nil() {
       print("Oh Yeah!\n")
   }

   func main() {
       if nil == nil {
           print("Its equal\n")
       }
   }
   ```

   - What's the output of following code ?

   ```go
   package main

   type customError struct{
       text string
   }

   func (e *customError) Error() string {
       return e.text
   }

   func getErrorText(err error) (text string) {
        if err != nil {
            text = err.Error()
        }
        return
   }

   func main() {
       var err *customError
       println(getErrorText(err))
   }
   ```

   - Why `nil` check is not working ? How would we fix that ?

## Extra materials

1. [Async IO on Linux: select, poll, and epoll](https://jvns.ca/blog/2017/06/03/async-io-on-linux--select--poll--and-epoll/)
1. [Go: the Good, the Bad and the Ugly](https://bluxte.net/musings/2018/04/10/go-good-bad-ugly/)
1. [Golang Internals Resources](https://github.com/emluque/golang-internals-resources)
1. [Hacking Go's internals by Bouke van der Bijl](https://www.youtube.com/watch?v=mYqhBYdqCyg)

## Done?

➡️ Go forward to [Databases](databases_basic.md)

⤴️ Back to [Contents](../contents.md)

[icon-chat]: https://img.shields.io/badge/chat-on%20telegram-blue.svg
[icon-mit]: https://img.shields.io/badge/license-MIT-blue.svg
[icon-awesome]: https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg
[license]: https://github.com/Kottans/web/blob/master/LICENSE.md
[awesome]: https://github.com/sindresorhus/awesome
