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