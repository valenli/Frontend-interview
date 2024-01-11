1. 什麼是作用域 (scope)？
變數在程式中可以被存取的範圍


2. var、let、const 的差別？
const與let能夠在塊級作用域被訪問
```javascript
const globalVar = 10; // 在全局作用域聲明 const 變數

if (true) {
  let blockVar = 20; // 在塊級作用域中聲明 let 變數
  console.log(globalVar); // 可以訪問全局變數
  console.log(blockVar); // 可以訪問塊級變數
}

console.log(globalVar); // 仍然可以訪問全局變數
console.log(blockVar); // ReferenceError: blockVar is not defined

```
- var 具有函數作用域(超出函數範圍後就訪問不到該變數)
==var可以修改和重新宣告==
- let與const具有塊級作用域(超出標示{}就訪問不到該變數)
==let可被修改但不能重新宣告==
==const不可被修改也不能重新宣告==

**假設我希望能讓區塊作用域訪問到函數作用域**
```javascript
function example(){
    let y;
    if (true){
        y = 20;
    }
    console.log(y);
}
example();
```
3.什麼是提升(hosting)?
