```js
//  查出这个条件的 对象

const pets = [
  { type: 'Dog', name: 'Max' },
  { type: 'Cat', name: 'Karl' },
  { type: 'Dog', name: 'Tommy' },
]
function findDog(name) {
  for (let i = 0; i < pets.length; ++i) {
    if (pets[i].type === 'Dog' && pets[i].name === name) {
      return pets[i];
    }
  }
}
console.log( findDog( 'Max' ) ) // {type: "Dog", name: "Max"}
console.log( findDog( 'Karl' ) ) // undefined
console.log( findDog( 'Tommy' ) ) // {type: "Dog", name: "Tommy"}
//简写：
function findDog(name) {
  return pets.find(pet => pet.type === 'Dog' && pet.name === name);
}
console.log( findDog( 'Max' ) ) // {type: "Dog", name: "Max"}
console.log( findDog( 'Karl' ) ) // undefined
console.log( findDog( 'Tommy' ) ) // {type: "Dog", name: "Tommy"}
```
