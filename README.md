# Example

```Go
package main

import "fmt"
import t "time"

func main() {
	fmt.Println("Hello Mukaram!")
	fmt.Println(t.Now())
}
```
# PACKAGE DECLARATION

```Go
package main
```

### WHAT IS PACKAGE MAIN?

- _Package main shows that this is the beginning of an executable program_

* This line is called a package declaration and it tells the Go compiler to which package this `.go` file belongs. If this package declaration is `package main`, then this program will be compiled into an executable.

* Next is a blank line. Go generally ignores these blank lines, they’re considered WHITESPACE (new lines, spaces, and tabs). Our program doesn’t need the line break, but it makes our code easier to read.

# IMPORT STATEMENT

`import "fmt"`

- _The import keyword allows us to use code from other packages_ 

* In this case, we're using the `Println` function from the fmt package. Note how the package name is enclosed with double quotes "". 

## IMPORTING MULTIPLE PACKAGES

_In Go, you will often need more than one package, To import multiple packages, we can add multiple import statements or use a single import with parentheses_

## Example

### Multiple imports

```Go
import "fmt"
import "time"
```

### Single import with parentheses

```go
import (
    "fmt"
    "time"
)
```

In my example, there's something different in my import, i placed a `t` before the `"time"`, i'll explain, i did something called `"Package alias"`

## PACKAGE ALIAS

* It basically means giving an alternative name to something, i imported the package `time` and i gave it an alternative name `t`. We do that by specifying an alias name before the package name.

### Final example

```go
import t "time"
```


# MAIN FUNCTION

Now that we know how to declare & use Go packages, let’s look through the rest of the code:

```go
func main() {
    fmt.Println("Hello Mukaram!") 
}
```

_We use the func keyword to declare the Go function main_

The `func` keyword denotes the start of a function declaration.

`func` is followed by the name of the function `main`, After the name there follows a pair of parentheses `()` and a set of curly braces `{}`.
The function code is written inside the set of curly braces.

### Function Code

The code inside a function is indented(It means that the lines of code inside a function are moved slightly to the right).

The code here invokes the `Println` function in the fmt package (that we imported earlier) to print the message `"Hello Mukaram!"`.


Normally when we write functions, you need to write code to invoke them, otherwise they are unused. However, the main function is different if it resides in the main package.

When we have a main function in the main package, this is special to Go. When compiled, an executable is produced, and when run, the executable uses the main function as the starting point.

```go
fmt.Println(t.Now())
```

This line prints the current date and time to the screen.

`t.Now()` gets the current date and time from the time package (assuming `t` is an alias for the time package).

`fmt.Println(...)` prints whatever is inside the parentheses to the terminal.

So together, the line gets the current time and displays it in the terminal.


# GO RESOURSES

There are many resources available to help us learn Go.

Go includes a program `go doc` for extracting and viewing documentation from `.go files`. For information about a package, use the command `go doc` followed by the package name.

For information about a package function, use the command `go doc` followed by the package name, a period then the function name.

### Example

```go doc fmt.Println```



# THANK YOU FOR READING!!!
