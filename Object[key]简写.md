```js
//考虑一个验证函数
function validate(values) {
  if (!values.first) return false;
  if (!values.last) return false;
  return true;
}
console.log(validate({ first: 'Bruce', last: 'Wayne' })); // true
//假设当需要不同域和规则来验证，能否编写一个通用函数在运行时确认？
// 对象验证规则
const schema = {
  first: { required: true },
  last: { required: true }
}
// 通用验证函数
const validate = (schema, values) => {
  for (field in schema) {
    if (schema[field].required) {
      if (!values[field]) {
        return false;
      }
    }
  }
  return true;
}
console.log(validate(schema, { first: 'Bruce' })); // false
console.log(validate(schema, { first: 'Bruce', last: 'Wayne' })); // true
```
