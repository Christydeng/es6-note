# es6-note
es6的点滴


1、es6的变量结构赋值，本质上是一种模式匹配。其中对象的解构与数组的解构不同，数组的解构是按次序排序的，而对象的解构是只要变量名与属性名对应相同即可。

2、let x
    if([1][0] === undefined){
      x = f();
    }else{
      x = [1][0]
    }
    
    // x = 1
    如果数组[1]的第零个[0]元素为undefined，那么 x = f() 否则 x 为数组[1]的第零个[0]元素的值.
