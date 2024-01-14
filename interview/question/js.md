### 1. 什麼是作用域 (scope)？
變數在程式中可以被存取的範圍


###2. var、let、const 的差別？
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
- let與const具有區塊作用域(超出標示{}就訪問不到該變數)
==let可被修改但不能重新宣告==
==const不可被修改也不能重新宣告==

**假設我希望能讓區塊作用域訪問到函數作用域**
```javascript
function example(){
    let y;
    if (true){
        y = 20;
    }
    console.log(y); // 20
}
example();
```
### 3.什麼是提升(hoisting)?
因為var、function在執行的時候會被推到最上面..?待查證
const let不會被提升

### 4.深拷貝&淺拷貝?

### 5.什麼是閉包（closure）？用途是什麼？


什麼是作用域 (scope)？
什麼是 hoisting？
什麼是 event loop？
function declaration vs function expression 差別？
By value vs by reference
<!-- 在不同情況下 this 指向對象會是什麼？
什麼是原型鍊（prototype chain）？ -->

非同步與同步操作混用時的輸出順序
Promise 熟不熟
有用遞迴的方式寫過 async await 嗎？
var、let、const 的差別？
Array.forEach、Array.map、Array.filter、Array.reduce 的差別？
如果要實現myMap()跟map的功能一樣，要怎麼做（[1,2,3].myMap(()=>{...})）
Promise 和 async await 要解決的是什麼問題？
知道event bubbling和capture的事件傳遞流程嗎？
請解釋何謂 callback function？
知道 debounce 和 throttle 的差異嗎？

請說出 JavaScript 所有的基本型別
請解釋 == 和 === 的差異
使用過什麼方法處理 AJAX？