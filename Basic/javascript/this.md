### this

> `this` 就是一个对象。不同情况下 `this` 指向不同，有以下几种情况

- 对象调用，`this` 指向该对象
    ```javascript
    const obj = {
        name: 'obj',
        fn: function() {
            console.log(this.name)
        }
    }
    obj.fn(); // this指向obj,输出 obj
    ```
- 直接调用的函数, `this` 指向全局 `window` 对象
    ```javascript
    function fn() {
        console.log(this)
    }
    fn(); // this => window
    ```
- 通过 `new` 的方式，`this` 永远指向新创建的对象
    ```javascript
    function Person(name) {
        this.name = name
        console.log(this)
    }
    const p = new Person('P') // this => p
    ```
- 箭头函数中的 `this`
由于箭头函数没有单独的 `this` 值。箭头函数的 `this` 与声明所在的上下文相同。也就是说调用箭头函数的同时，不会隐式调用 `this` 参数，而是从定义时的函数继承上下文。
    ```javascript
    const obj = {
        a: () => {
            console.log(this);
        }
    }
    obj.a() // this => window
    ```