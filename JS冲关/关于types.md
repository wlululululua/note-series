# 关于类型
有关JavaScript的数据类型的笔记
- [关于类型](#关于类型)
  - [简介](#简介)
  - [类型分类](#类型分类)
    - [primitive type](#primitive-type)
    - [Object type](#object-type)
  - [类型判断](#类型判断)
    - [typeof操作符](#typeof操作符)

## 简介
JavaScript是一种动态类型(dynamic typing)的语言。一个变量可以拥有不同类型的值，在执行期间，才能确定该变量所拥有的值的类型。
```javascript
//javascript
var a = 1;
a = "hi";
```

与动态类型相对的是静态类型(static typing)，变量只能拥有指定类型的值。
```typescript
//typescript
var a: number;
a = 1;
a = "hi";//error: 不能将string类型分配给number类型
```

## 类型分类
> "Everything is an Object or a primitive"

ECMAScript定义了8种数据类型：an Object + 7 primitives

### primitive type
primitive type也叫原始类型或简单类型或基本类型，即不可再分的类型，是什么就是什么(a single value)。

ECMAScript定义了7种基本数据类型：
- Number
  - 包含整数和浮点数
- String
  - 字符序列(a sequence of characters)
  - 单引号双引号均可
- Boolean
  - 值为true或者false
- undefined
    - undefined表示不存在(lack of existence) 
    - JS引擎最开始为变量初始化所设置的值即为undefined
    - 不要给一个变量赋值为undefined，理由即上
- null
  - null也表示不存在(lack of existence)
  - 可以给变量赋值为null
  - 相当于对象的占位符
- Symbol
  - ES6
  - 唯一且不可变
- Bigint
  - ES11
  - 具有任意精度的整数



### Object type
ECMAScript定义了1种复杂数据类型即Object类型。

## 类型判断

### typeof操作符
typeof操作符可以判断一个操作数的数据类型，即到底为primitive还是object
语法：typeof operand | typeof(operand)
```javascript
typeof(6) //"number"
typeof("hi") //"string"
typeof(true) //"boolean"
typeof(undefined) //"undefined"
typeof(null) //"object"
typeof(Symbol()) //"symbol"
typeof(1n) //"bigint"
typeof({}) //"object"
typeof(function() {}) //"function"
typeof([]) //"object"
```