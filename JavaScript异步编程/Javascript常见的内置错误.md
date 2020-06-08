### 1.常见的内置错误

1)ReferenceError:引用的变量不存在

```
console.log(a) 
// Uncaught ReferenceError: a is not defined
```

2)TypeError :数据类型不正确的错误

```
var a
console.log(a.xxx)
// Uncaught TypeError: Cannot read property 'xxx' of undefined
```

3)RangeError :数据值不在其所允许的范围内

```
function fn(){
   fn()
}
fn()
// 递归导致
// Uncaught RangeError: Maximum call stack size exceeded
```
4)SyntaxError:语法错误

```
var a = '
// Uncaught SyntaxError: Invalid or unexpected token
```

### 2.错误处理

1)捕获错误:

```
try {
   var b;
   console.log(b.xxx)
} catch (error) {
    console.log(error.message)
    console.log(error.stack)
}
console.log('捕获错误之后')

// Cannot read property 'xxx' of undefined
// TypeError: Cannot read property 'xxx' of undefined
      at <anonymous>:3:18
// 捕获错误之后
```

2)抛出错误:

```
throw new Error('')
```

### 3.错误对象

message属性:错误相关信息
stack属性:函数调用栈记录信息
