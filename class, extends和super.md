```js
//es5
class Animal {
  constructor() {
    this.type = 'animal'
  }
  says(say) {
    console.log(this.type + ' says ' + say)
  }
}
let animal = new Animal()
animal.says('hello')

//es6
class Cat extends Animal {
  constructor() {
    super()
    this.type = 'cat'
  }
}
let cat = new Cat()
cat.says('hello')

-----------------------------------------------------------------------
// 定义类时，方法的顺序如下：
//
// constructor
// public get/set 公用访问器，set只能传一个参数
// public methods 公用方法，以函数命名区分，不带下划线
// private get/set 私有访问器，私有相关命名应加上下划线_为前缀
// private methods 私有方法
class SomeClass {
  constructor() {
  // constructor
  }
  get aval() {
    // public getter
  }
  set aval(val) {
    // public setter
  }
  doSth() {
    // 公用方法
  }
  get _aval() {
    // private getter
  }
  set _aval() {
    // private setter
  }
  _doSth() {
    // 私有方法
  }
}
```
