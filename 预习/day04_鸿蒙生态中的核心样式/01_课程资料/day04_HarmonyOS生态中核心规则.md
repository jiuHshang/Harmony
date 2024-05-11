# day04_HarmonyOS生态中核心规则

背景 : 在HarmonyOS生态中无论是哪一个设备的开发 , 我们都是对开发的结构进行修饰, 但修饰工程中 , 我们需要通过CSS中的核心样式规则进行修饰 , 但是这种规则有很多, 所以需要我们需要一个一个进行详细的学习 ; 

## 今日学习目标

1. 核心规则的背景
2. 文本规则
3. 背景规则
4. 浮动规则
5. 简单demo

## 1. HarmonyOS中的文本规则

### 1) 文本规则的含义 : 

主要是通过属性和属性值为项目中的文本进行修饰 ; 比如文本的加粗, 文本的倾斜, 文本颜色等等

### 2) 大小规则

```html
<!--
	字体大小属性 : font-size
	取值 : 数值+单位(px单位/em单位)
	默认字体大小 : 16px; 
	最小显示大小 : 12px;
	注意事项 : 如果你的浏览器是最新版本的浏览器, 字体能设置可以设置成小于12px
-->
<style>
    .pTwo{
        font-size:20px;
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了</p>
```

### 3) 字体规则

```html
<!--
	字体属性 : font-family (也称之为字体族科, 因为字体是一个庞大的家族)
	取值 : 字体 ( 宋体,隶书,楷体,黑体,微软雅黑等等 )
	默认字体大小 : 宋体; 
	高版本浏览器 : 微软雅黑;
	注意事项 : 如果你的浏览器是最新版本的浏览器, 字体能设置可以设置成小于12px
-->
<style>
    .pTwo{
        font-family:楷体;
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了</p>
```

### 4) 加粗规则

```html
<!--
	字体加粗属性 : font-weight 
	取值 : 
		1)数值类型
			100-900 (100-细体; 400-正常字体; 700-加粗字体; 900-更粗字体)
		2)关键词类型
			lighter-细体
			normal-正常字体
			bold-加粗字体
			bolder-更粗字体
	
	注意事项 : 900和700 以及bold和bolder 都能实现加粗效果, 但是900和bolder更加具有强调性
	问题1 : 为什么有了加粗b标签反而学习font-weight:bold
		因为使用CSS属性能实现简化页面的结构; 能让所有的标签都实现加粗
		还能实现鼠标的划过效果;
	问题2 : 为什么默认字体没有任何效果还要学习font-weight:normal
		能取消默认的b,strong等自带加粗效果标签的加粗效果
-->
<style>
    .pTwo{
        font-family:bold;
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了</p>
```

### 5) 颜色规则

```html
<!--
	文本颜色属性 : color属性
	取值 : 
		1)颜色单词 : red,green,blue,yellow,purple,plum,aqua,yellowgreen,greenyellow,transparent(透明颜色)
		2)#六位十六进制颜色 : 十六进制颜色取值0-9A-F
			color:#112233
			详解:第12位代表的是红色; 第34位代表的是绿色; 第56位代表的是蓝色
			如果:每个颜色相邻的两位都取值一样,则可以进行简写
				例如:#112233 简写:#123
				例如:#22ccdd 简写:#2cd
				例如:#112212 不能简写, 因为蓝色的取值不同
		3)rgb(red,green,blue) : rgb颜色也是开发中经常使用的一个颜色, 红绿蓝三个颜色取值范围为:0-255;包含0,包含255;
-->
<style>
    .pTwo{
        color:red;
        color:#232323;
        color:rgb(23,34,45)
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了</p>
```

### 6) 大小写转换

```html
<!--
	大小写转换属性 : text-transform
	含义 : 用来控制英文文本的修饰
	取值 : 
		1)none;默认效果
		2)capitalize;英文文本每一个英文单词首字母大写
		3)uppercase;全都变成大写字母
		4)lowercase;全都变成小写字母
-->
<style>
    .pTwo{
        text-transform:uppercase;
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了, My name is Harmony</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了, My name is Harmony</p>
```

### 7) 小型大写字母

```html
<!--
	小型大写字符属性 : font-variant
	含义 : 小型大写指的是,让所有的小写字母都变成大写字母,并且这个转换后的大写字母占四线三个中的中间位置;
	取值 : 
		1)normal;默认效果
		2)small-caps;用来实现小型大写
-->
<style>
    .pTwo{
        font-variant:small-caps;
    }
</style>
<p class="pOne">原始:欢迎来到HarmonyOS, 我们开始学习了, My name is Harmony</p>
<p class="pTwo">修饰:欢迎来到HarmonyOS, 我们开始学习了, My name is Harmony</p>
```

### 8) 间距

```html
<!--
	文本间距分为两种:字符间距和词间距
		字符间距 : 指的是, 汉字与汉字, 字母与字母, 符号符号之间的距离;
			属性:letter-spacing:数值+单位
		词间距 : 指的是, 单词与英文单词之间的距离;
			属性:word-sapcing:数值+单位
-->
<style>
    /*调整的是每一个字符之间的距离;汉字,字母,标点符号之间的距离*/
    .pOne{
        letter-sapacing:20px
    }
    /*调整的是英文单词和英文单词之间的距离*/
    .pTwo{
        word-spacing:20px;
    }
</style>
<p class="pOne">各位小伙伴们大家好, 欢迎来到HarmonyOS课堂进行学习, Hello everyone, welcome to the HarmonyOS classroom for learning </p>
<p class="pTwo">各位小伙伴们大家好, 欢迎来到HarmonyOS课堂进行学习, Hello everyone, welcome to the HarmonyOS classroom for learning</p>
```

## 2. HarmonyOS中的背景规则

HarmonyOS生态中的背景规则, 主要是用来修饰背景颜色等其他效果, 本次我们学习的时候主要以背景颜色为主

### 1) 背景颜色规则

```html
<!--
	背景颜色属性 : background-color
	取值 : 
		1)颜色单词
		2)#六位十六进制
		3)rgb()颜色
		4)rgba()颜色 a代表的是alpha透明度 取值0-1之间的小数, 经常保留1位, 可以取值为0, 可以取值为1; 0代表的是透明; 1代表的是不透明 
-->
<style>
    div{
        width:200px;
        heght:200px;
        background-color:red
    }
</style>
<div>
	普通的div元素
</div>
```

## 3. HarmonyOS中的浮动规则

HarmonyOS生态中的浮动规则 , 主要用于研发PC项目为主 , 主要解决的问题 : 让原本纵向排列的元素横向显示 ; 方便横向布局展示

注意事项 : 再初期接触浮动的时候 , 父元素要给定高度 , 这样能解决一部分问题, 后面会详细讲解这一问题

### 1) 浮动规则

```html
<!--
	浮动属性 : float
	取值 : 
		1)left: 都添加左浮动, 解决元素横向显示问题, 代表的是从左向右依次显示
		2)right: 都添加右浮动, 解决元素横向显示问题, 代表的是从右向左依次显示
-->
<style>
    .bigbox{
        width:600px;
        height:600px;
        border:10px solid gray;
    }
    .red{
        width:100px;
        height:100px;
        background-color:red;
        float:left;
    }
    .green{
        width:200px;
        height:100px;
        background-color:red;
        float:left;
    }
    .blue{
        width:150px;
        height:100px;
        background-color:red;
        float:left;
    }
</style>
<div class="bigbox">
    <div class="red"></div>	
    <div class="green"></div>
    <div class="blue"></div>
</div>
```

### 2) 浮动基础问题

```html
<!--
	下面的宽度高度添加完毕之后, 会出现问题:蓝色的盒子折行显示, 因为剩余空间不够了
	所以设置的视乎,注意距离
-->
<style>
    .bigbox{
        width:600px;
        height:600px;
        border:10px solid gray;
    }
    .red{
        width:100px;
        height:100px;
        background-color:red;
        float:left;
    }
    .green{
        width:200px;
        height:100px;
        background-color:red;
        float:left;
    }
    .blue{
        width:400px;
        height:100px;
        background-color:red;
        float:left;
    }
</style>
<div class="bigbox">
    <div class="red"></div>	
    <div class="green"></div>
    <div class="blue"></div>
</div>
```

