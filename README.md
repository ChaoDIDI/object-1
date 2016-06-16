/***
 * 面向过程方式
 * 1.需要定义很多的变量(容易出现变量名重复的问题)
 * 2.代码重用率比较低
 * 3.结构不是很清晰
 * 4.实现简单,代码容易看懂,可以边思考边写代码
 * 5.在实现一些简单的处理逻辑时建议使用
 * 
 * 
 * 面向对象方式
 * 1.对象定以后可以重复使用
 * 2.对象定义之前需要把对象包含哪些属性和方法思考完全
 * 3.代码结构清晰.代码可读性强
 * 4.不需要担心变量或者方法重名问题
 * 5.实现起来比较复杂 ,在实现的时候尽量把对象相关的方法和属性定义完整
 * 6.可扩展性强*****/ 
 * 
 

<!--///获取当前事件 实例化(创建)一个对象-->
var now =new Date()
console.dir(now);
console.log(now.getSecoonds());
<!--延迟五秒钟之后再次输出一个date-->
setTimeout(function(){var newTime = newDate(); console.dir(newTime); console.log(newTime.getSeconds());},5000)


<!--我们创建的now和newTime两个对象 -->
<!--它们包含的属性方法都一样 但是值是不一样的-->
methodName 方法名
(args1,args2....)参数名
function methodName(args1,args2...){//方法体 方法的内容 return xxx}

 * 创建一个鸭子的对象
 * 需要两个参数name color***/  
function Duck(name,color) {
    this.name = name
    this.color = color
    this.walk = function () {
        
        console.log(this.color+'颜色的鸭子'+this.name,"走起来")
    }
    this.eat = function(){
        console.log(this.color+'颜色的鸭子'+this.name,'在吃东西');
    }
}

//创建鸭子jack
// 为创建后的对象进行属性修改操作 不影响其他创建的对象
var jack = new Duck('jack','黄');
jack.walk();
jack.legs = 1;


// 创建鸭子caler
var caler = new Duck('caler','白');
caler.eat();
caler.eyes =1;

/***
 * 使用原来的实现方式 实现以上功能***/ 

function walk(obj) {
    console.log(obj.color+'颜色的鸭子'+obj.name,"走起来")
    
}
function eat(obj) {
     console.log(obj.color+'颜色的鸭子'+obj.name,'在吃东西');
}
var oldDuck = {};
oldDuck.name ='jack';
oldDuck.color ='黄色';
walk (oldDuck);
eat (oldDuck);
