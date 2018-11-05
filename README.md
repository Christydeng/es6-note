# es6-note
es6 的点滴


1、es6的变量结构赋值，本质上是一种模式匹配。

   其中对象的解构与数组的解构不同，数组的解构是按次序排序的，而对象的解构是只要变量名与属性名对应相同即可。
 
   let { foo } = { foo: 'woya' }
   等同于
   let { foo: foo } = { foo: 'woya' } 
   let { foo: f } = { foo: 'woya' }

    // f = 'woya'  右边的foo找到左边的同名属性foo， 然后把值赋给变量f. 代码中，foo是匹配模式，而f才是变量，真正被赋值的是f变量，而不是foo模式。
    // f 变量可以任意命名
    
    注意： 指定默认值时，对象的默认值必须严格等于undefined， null都不行， 因为null不严格等于undefined。
    let {x : 3 } = {} // x=3
    let {x : 3} = {x : undefined} // x=3
    let {x : 3} = {x ： null} // x=null

2、let x
    if([1][0] === undefined){
      x = f();
    }else{
      x = [1][0]
    }
    
    // x = 1
    如果数组[1]的第零个[0]元素为undefined，那么 x = f() 否则 x 为数组[1]的第零个[0]元素的值.
    
3、当把大括号{}写在行首，JavaScript会将其解释为代码块，并且执行 {x=2} console.log(x) // x = 2
   所以在解构赋值当中应注意避免把大括号放在行首，正确写法 ({x} = { x: 2 }) // x = 2

4、
