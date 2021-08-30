## 定义复杂的函数参数

🙅‍函数参数模糊不清

```js
const bad = (payload) => {
    // handle payload
}
```

👌参数更清晰的, 变量使用更简单

```js
const good = ({ name, age, addr }) => {
    console.log(name);
    // more action
}
```

## 类型默认值可以作为函数调用

在 vue 的 props 中需要指定某个 prop 类型和默认, 如果 prop 是基本类型, 且默认值为对应类型的默认值, 可以直接简写。

```js
props: {
    defaultExpand: {
        type: Boolean,
        default: false,
    }
}
```

等价于

```js
props: {
    defaultExpand: Boolean
}
```

类似的

```js
String() == ""
Boolean() == false
Array() == []
```