# Go lang session - draft

## Installation
### Ubuntu 
```sh
sudo apt install golang-go
```
### Other linux
```sh
wget -qO- 'https://go.dev/dl/go1.17.6.linux-amd64.tar.gz' | sudo tar -C /usr/local -xz
echo 'export PATH=$PATH:/usr/local/go/bin' >> "${HOME}/.profile"
```
## Hello world
```go
package main 

// same like #include in c++
import "fmt"

// special function(same as `int main()` in c++), which is called when program is executed
func main(){
	
    // printf("Hello world!")
    fmt.Println("Hello world!")
}
```
```sh
$ go run hello.go
# else to get executable
$ go build hello.go

```
## Variable
```go
var mystr string
mystr = "Hello world!"
// or in short form
// mystr := "Hello world!

// Multiline string
str1:=`asfj
dfad
adf
`
num1 := 8          // int
num2 := 4.         // float64
num3 := 1 + 7i     // complex128
num4 := byte('c')  // byte (alias for uint8)
var a rune = 'ก'  // int32 and represent Unicode code.

// short declaration
// num1, num2,num3,num4,a := 8,3., 1+7i,byte('c'),rune('ก')

var u uint = 24      // uint (unsigned)
var p float32 = 3.14  // 32-bit float


// Array are initialized with 0 by default
var arr [5] int
fmt.Println(arr)

// Initializing 
// arr := [5] int{1,3,2,5,7}
//fmt.Println(arr)

// Initializing 
// arr := [...] int{1,3,2,5,7}
//fmt.Println(arr)

import ( 
   "fmt"
   "reflect"
)

fmt.Println(reflect.TypeOf(arr),len(arr),cap(arr)

```

## Formatting
`fmt.Printf` - Print formatter eg: `fmt.Printf("%d + %d = %d\n", num1, num2, num3)`   
`fmt.Print` - Print, just prints given vars eg: `fmt.Print(num1,num2,num3,"\n")`   
`fmt.Println` - Print line, ends with `\n` eg: `fmt.Println(num1,num2,num3)`

```
fmt.Printf("%v %v\n",a ,b )
```
![imga](https://i.imgur.com/T4PW26H.png)

## Control flow
### If, else, else if
```go
var number int
fmt.Scanln(&number)

if number > 0
	fmt.Printf("%d is positive",number)
else if number <0 
	fmt.Printf("%d is negative",number)
else
    fmt.Print("Given number is 0")
  
 ```



