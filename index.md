<!DOCTYPE HTML>
<html>
<head>
    <meta http-equiv="Content-Type" Content="text/html; charset=utf-8" />
    <title>javascript</title>
    <style type="text/css">
        /*body{font-size:12px;}*/
        /*#txt{*/
        /*    height:400px;*/
        /*    width:600px;*/
        /*    border:#333 solid 1px;*/
        /*    padding:5px;}*/
        /*p{*/
        /*    line-height:18px;*/
        /*    text-indent:2em;}*/
    </style>
</head>
<body>

<!--<h2 id="con">JavaScript课程</H2>-->
<!--<div id="txt">-->
<!--    <h5>JavaScript为网页添加动态效果并实现与用户交互的功能。</h5>-->
<!--    <p>1. JavaScript入门篇，让不懂JS的你，快速了解JS。</p>-->
<!--    <p>2. JavaScript进阶篇，让你掌握JS的基础语法、函数、数组、事件、内置对象、BOM浏览器、DOM操作。</p>-->
<!--    <p>3. 学完以上两门基础课后，在深入学习JavaScript的变量作用域、事件、对象、运动、cookie、正则表达式、ajax等课程。</p>-->
<!--</div>-->
<!--<form>-->
    <!--当点击相应按钮，执行相应操作，为按钮添加相应事件-->
<!--    <input type="button" value="改变颜色" onclick="set.changeColor()">-->
<!--    <input type="button" value="改变宽高" onclick="set.changeHeight()">-->
<!--    <input type="button" value="隐藏内容" onclick="set.hide()">-->
<!--    <input type="button" value="显示内容" onclick="set.show()">-->
<!--    <input type="button" value="取消设置" onclick="set.cansel()">-->

<p id="a2">哈喽，小可爱</p><br>
<input type="button" onclick="a()" value="点击"><br>
<p id="b">hahahahah</p><br>
<p id="c2"></p><br>
<input type="button" onclick="c0()" value="点我"><br>
<p id="x1"></p><br>
<input type="button" onclick="newD()" value="点击前往指定网页"><br>
<input type="button" onclick="newD1()" value="点击前往指定网页但不能返回"><br>
<input type="button" onclick="ret()" value="点击返回"><br>
<input type="button" onclick="forw()" value="点击前进"><br>
<input type="button" onclick="one1()" value="变颜色"><br>
<input type="button" onclick="shuax()" value="刷新页面"><br>
<input type="button" onclick="z0()" value="点击我录入姓名"><br>
<p id="z2"></p><br>
<p id="one">我会变色</p><br>
<!--<input type="button" onclick="tim1()" value="点击我每秒弹出警告框">-->
<p>在下方显示一个时钟</p><br>
<p id="ti4"></p><br>
<input type="button" onclick="t6()" value="点击暂停时钟"><br>
<p id="t5"></p><br>
<input type="button" onclick="show()" value="点击显示setTimeout"><br>
</form>
<script type="text/javascript">
    var x=document.getElementById("one").value;
    function one1(){
        x.style.color="red";
    }

    //获取浏览器高度和宽度
    var H=document.innerHeight || document.documentElement.clientHeight;
    var W=document.innerWidth  || document.documentElement.clientWidth;
    x=document.getElementById("x1");
    x.innerHTML="浏览器宽度："+W+",浏览器高度"+H;
    //获取可用宽度
    document.write("可用宽度"+screen.availWidth);
    document.write("可用高度"+screen.availHeight);
    //获取域名
    document.write(location.href);
    //获取路径名
    document.write(location.pathname);
    //加载新文档
    function newD() {
        window.location.assign("https://www.baidu.com/");
    }
    //两者公用一个页面，没有返回键
    function newD1() {
        window.location.replace("https://www.baidu.com/");
    }
    //创造返回按钮
    function ret() {
        window.history.back();
        //或者 history.go(1);
    }
    //点击按钮前进
    function forw() {
        window.history.forward();
        //或者 history.go(-1);
    }
    function shuax() {
        history.go(0);
    }
    //提示框
    // var x=confirm();
    // if(x==true){
    //     alert("输入正确");
    // }else{
    //     alert("输入错误");
    // }
    //输入的对话框
    function z0() {
        var z;
        var z1=prompt("请问你的名字是？","王小明")
        if(z1!=null && z1!==""){
            z="你好，"+z1;
        }document.getElementById("z2").innerHTML=z;
    }
    //每秒弹出警告框
    function tim1() {
        setInterval(function () {
            alert("Hello")
        },3000);
    }
    //显示实时时间
    var ti0=setInterval(function () {ti1()},1000);
    function ti1() {
        var ti2=new Date();
        var ti3=ti2.toLocaleTimeString();
        document.getElementById("ti4").innerHTML=ti3;
    }

    var t1=setInterval(function(){t2()},1000);
    function t2() {
        var t3=new Date();
        var t4=t3.toLocaleTimeString();
        document.getElementById("t5").innerHTML=t4;
    }
    function t6() {
        clearInterval(t1);
    }
    //使用setTimeout实现点击事件
    function show() {
        setTimeout(setInterval(function () {
            alert("你好")
        },1000));
    }
    function f() {

    }




    var str="Hello world";
    document.write(str.match("world")+"<br>");
    document.write(str.match("World")+"<br>");

function a() {
    var a1=document.getElementById("a2").innerHTML;
    var a3=a1.replace("小可爱","小仙女");
    document.getElementById("a2").innerHTML=a3;
}

var b1="Hello world";
var b2="BIGBIGBIG"
document.write(b1.toUpperCase());
document.write(b2.toLowerCase());

function c0() {
    var c="a,b,c,d,e";
    var c1=c.split(",");
    document.getElementById("c2").innerHTML=c1[1];
}

var d="Me is your honey";
var d1=/your/i;
document.write(d.match(d1)+"<br>");

var d2="I have one dollors and one hundred dollors";
var d3=/one/g;
document.write(d2.match(d3)+"<br>");

var e=new RegExp("a");
document.write(e.test("I hava a apple and a orange")+"<br>");












    // var txt=document.getElementById("txt");
    // var set= {
    //     changeColor:function(){
    //         txt.style.color="red";
    //         text.style.backgroundColor="blue";
    //     },
    //     changeHeight:function () {
    //         txt.style.height="30px";
    //         txt.style.width="100px";
    //     },
    //     hide:function () {
    //         txt.style.display="none";
    //     },
    //     show:function () {
    //         txt.style.display="block";
    //     },
    //     cansel:function () {
    //         var mes=confirm("你确定重置所有设置吗");
    //         if(mes==true){
    //             txt.removeAttribute('style');
    //         }
    //     }
    // }



</script>
</body>
</html>
