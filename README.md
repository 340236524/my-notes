# my-library
李亚军学习笔记

https://github.com/linkeddb-v2-dev/webpack-template   开发框架


var isCanClick = ture;
$('#button').on('click',function(){
    if(!isCanClick) return;
    isCanClick = false;
}) 

//阻止冒泡事件
function stopDefault( e ) { 
    //阻止默认浏览器动作(W3C) 
    if ( e && e.preventDefault ) 
        e.preventDefault(); 
    //IE中阻止函数器默认动作的方式 
    else 
        window.event.returnValue = false; 
    return false; 
}

//停止冒泡事件
function stopBubble(e) { 
//如果提供了事件对象，则这是一个非IE浏览器 
if ( e && e.stopPropagation ) 
    //因此它支持W3C的stopPropagation()方法 
    e.stopPropagation(); 
else 
    //否则，我们需要使用IE的方式来取消事件冒泡 
    window.event.cancelBubble = true; 
}

1.&&        // 和 and

1.1两边条件都为true时，结果才为true；           
1.2如果有一个为false，结果就为false；
1.3当第一个条件为false时，就不再判断后面的条件

注意：当数值参与逻辑与运算时，结果为true，那么会返回的会是第二个为真的值；如果结果为false，返回的会是第一个为假的值。  

2.||        // 或者

2.1只要有一个条件为true时，结果就为true；       
2.2当两个条件都为false时，结果才为false；
2.3当一个条件为true时，后面的条件不再判断

注意：当数值参与逻辑或运算时，结果为true，会返回第一个为真的值；如果结果为false，会返回第二个为假的值；