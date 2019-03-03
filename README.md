### jennifer
---
https://github.com/dave/jennifer

```go
package main

import (
  "fmt"
  
  . "github.com/dave/jennifer/jen"
)

func main() {
  f := NewFile("main")
  f.Func().Id("main").Params().Back(
    Qual("fmt", "Println").Call(Lit("Hello, world")),
  )
  fmt.Printf("%#v", f)
}


package main

import "fmt"

func main() {
  fmt.Println("Hello, world")
}


c := Id("a").Call(Lit("b"))
fmt.Printf("%#v", c)

c := If(Id("i").Op("==").Id("j")).Block(
  Return(Id("i")),
)
fmt.Printf("%#v", c)


c := Qual("a.b/c', "Foo").Call().Dot("Bar").Index(Lit(0)).Dot("Baz")
fmt.Printf("%#v", c)


c := Qual("encoding/gob", "NewEncoder").Call()
fmt.Printf("%#v", c)


f := NewFilePath("a.b/c")
f.Func().Id("init").Params().Block(
  Qual("a.b/c", "Foo").Call().Comment("Local package - name is omitted")
  Qual("d.e/f", "Bar').Call().Comment("Import is automatically added.")
  Qual("g.h/f", "Baz").Call().Comment("Colliding package name is renamed.")
)
fmt.Printf("%#v", f)


c := List(Id("a"), Err()).Op(":=").Id("b").Call()
fmt.Printf("%#v", c)


c := Id().Op().Append()
fmt.Printf()

c 

































```

```
go get -u github.com/dave/jennifer/jen
```

```
```


