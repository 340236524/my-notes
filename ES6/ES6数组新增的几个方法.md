arr.map(item => item*2)   
等于
arr.map((item) => {
    return item*2
}) 


1.forEach()
```
var arr = [1,2,3,4];

arr.forEach((item,index,arr)=>{

    console.log(item);  //结果为1,2,3,4

});
```
//foreach遍历数组，无返回值，不改变原数组，仅仅只是遍历，常用于注册组件、指令等等。

2.map()
```
var arr = [1,2,3,4];

arr.map((item,index,arr)=>{

    return item*10;  //结果为10,20,30,40

});
```
//map遍历数组，返回一个新数组，不改变原数组

3.filter()

var arr = [1,2,3,4];
```
arr.filter((item,index,arr)=>{

   return item >2; //结果为[3,4]

});
```
//filter过滤掉数组中不满足条件的值,返回一个新数组,不改变原数组

4.find()
```
var arr = [
    {id:'1',name:'11'},
    {id:'2',name:'11'},
    {id:'3',name:'11'},
    {id:'4',name:'11'}
]

arr.find((item,index,arr)=>{

   return item.id == 2; // 结果为{id:'2',name:'11'}

});
```
//find过滤掉数组中不满足条件的值,返回一个新对象,不改变原数组

5.every()    全选用的到
```
var arr = [1,2,3,4];

arr.every((item,index,arr)=>{

   return item >1; //返回false

});
```
//遍历数组每一项，每一项返回true,最终结果为true.有一项返回false,停止遍历,结果返回为false。不改变原数组。

6.some()
```
var arr = [1,2,3,4];

arr.some((item,index,arr)=>{

   return item > 2; //返回true

});
```
//遍历数组每一项,有一项返回true,则停止遍历，结果返回true。不改变原数组。

7.reduce()
```
var arr = [1,2,3,4];

arr.reduce((result,item,index,arr)=>{

  console.log(result);

  console.log(item);

  console.log(inddx);

  return result+item; 

});
```
//reduce计算数组综合,然后返回其值，不改变原数组，从数组的第二项开始遍历。