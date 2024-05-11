# day09_HarmonyOS生态中的信息展示

背景 : 随着科技的发展, HarmonyOS生态在国家政策的大力扶持下 , 队伍日渐庞大 , 开发过程中我们除了要了解完成PC端项目的开发 , 还要了解移动项目以及后台管理系统的 ; 后台管理系统在再项目开发的时候仍然占有一席地位 ; 

后台管理系统 : 最主要的是展示数据信息的, 展示数据信息, 我们通常情况显示用表格 ( table ) 完成 ,  

## 今日学习目标

1. 表格的含义和作用
2. 表格的基本语法
3. 表格的标签属性
4. 表格的CSS属性
5. 表格新增的内容

## 1. 表格的含义和作用

<img src="pic1.png" style="zoom:67%;" >

**表格含义 :** 表格就是一个带有边框的矩阵 , 矩阵类似于军训 , 广场舞等 , 各个方阵的队伍

**表格作用 :** 主要是用来将服务器里面的数据整齐划一的展示在浏览器中, 以供用户使用和操作

## 2. 表格的基本语法

表格的基本语法如下 : 

```html
<!-- table 双标签 代表的是一个表格, 一个table就代表出现一个表格 -->
<table>
    <!-- tr 双标签 代表的是一个表格中的行, table-row 的简写-->
    <tr>
       <!-- td 双标签 代表的是一个单元格, 也是tr里面的列  table-data的简写--> 
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
    </tr>
</table>
<!--
	注意事项1:
		1)嵌套结构,table里面必须放置tr,tr里面必须放置td, 如果想要嵌套其他的标签我们需要嵌套在td里面
	注意事项2:
		1)快速创建表格:emet语句
			table>tr*3>td*3
			table>tr*3>td{文本}*3
			等等其他的快捷键
-->
```

## 3. 表格的标签属性

### 0) 回顾

​	标签属性 : 标签属性是将属性属性和属性值放在开始标签名字后面 , 并且属性和属性值需要使用等号链接 , 属性值需要带引号

​	CSS属性 : CSS属性是将属性和属性值,放在CSS的语法中 , 并且属性和属性值使用冒号连接 , 每一组属性和属性值使用分号分隔

### 1) table的标签属性

```html
<!--
	table的标签属性
		1)边框属性
			border="1" 
			注意:取值为数值, 没有单位, 并且会给单元格添加边框, 同时如果设置成大于1的数值, 表格的边框会变大, 单元格的边框边框仍然是1
		2)宽度高度属性
			width="200px"
			height="200px"
			注意:如果不带单位,则代表的是px像素单位; 除了可以给px单位, 还可以给对应的百分比单位
			注意:如果单元格内部文本多少一直的话,则会均分单元格的宽度高度, 如果不一致,并且单元格没有宽度高度,则会自动撑大
		3)背景颜色属性
			bgcolor="red"
		4)边框颜色属性
			bordercolor="blue"
		5)表格水平对其方式
			align="left/right/center"
		6)单元格与单元格之间的间距
			cellspacing="20px"
		7)单元格与内容之间的间距
			cellpadding="20px"
		8)表格外边线
			frame="表格的外边线设置"
				above=上方边框
				below=下方边框
				lhs(left-horizontal-side)=左侧边框
				rhs(right-horizontal-size)=右侧边框
		9)表格内部横纵线
			rules="rows/cols"
				rows=水平线
				cols=垂直线
-->
<table>
    <tr>
    	<td>小张</td>
        <td>小王</td>
        <td>小李</td>
    </tr>
    <tr>
        <td>小孙</td>
        <td>小赵</td>
        <td>小郭</td>
    </tr>
    <tr>
    	<td>小陈</td>
        <td>小谷</td>
        <td>小吴</td>
    </tr>
</table>
```

### 2) tr的标签属性

```html
<!--
	tr的标签属性
		1)高度属性
			height="150px"
		2)背景颜色属性
			bgcolor="red"
		3)文本水平对其
			text-align="left/right/center"
			设置一整行单元格内容的水平对其方式
		4)文本垂直对其
			valign="top/bottom/middle"
			设置一整行单元格内容的垂直对其方式
-->
<table>
    <tr>
    	<td>小张</td>
        <td>小王</td>
        <td>小李</td>
    </tr>
    <tr>
        <td>小孙</td>
        <td>小赵</td>
        <td>小郭</td>
    </tr>
    <tr>
    	<td>小陈</td>
        <td>小谷</td>
        <td>小吴</td>
    </tr>
</table>
```

### 3) td的标签属性

```html
<!--
	td的标签属性
		1)宽度属性
			width="200px"
			取值可以不带单位
		2)高度属性
			height="200px"
			取值可以不带单位
		3)背景颜色属性
			bgcolor="red"
		4)水平对其方式
			align="left/right/center"
			调整当前单元格的水平对其方式
		5)垂直对其方式
			valign="top/bottom/middle"
			调整当前单元格的垂直对其方式
		6)水平合并单元格
			colspan="数值"
			水平合并单元格, 水平跨列
		7)垂直合并单元格
			rowspan="数值"
			垂直合并单元格, 垂直跨行
-->
<table>
    <tr>
    	<td>小张</td>
        <td>小王</td>
        <td>小李</td>
    </tr>
    <tr>
        <td>小孙</td>
        <td>小赵</td>
        <td>小郭</td>
    </tr>
    <tr>
    	<td>小陈</td>
        <td>小谷</td>
        <td>小吴</td>
    </tr>
</table>
```

## 4. 表格的CSS属性

CSS属性主要是放在CSS样式里面属性 , 实际开发的过程总使用CSS属性较多 , CSS属性主要是对于table标签和td标签进行修饰

### 1) table的CSS属性

```html
<!--
	table的CSS属性
		1)边框属性
			border:1px solid gray;
			只会给table添加边框, 不会影响td
		2)宽度,高度属性(CSS属性需要带单位)
			width:300px;
			height:300px;
		3)单元格与单元格之间的距离
			border-spacing:0px;
		4)边框线合并
			border-collapse:collapse;
		4)表格的布局方法
			table-layout:
				取值:auto/fixed
			auto:代表的是自动, 灵活性比较强,但每次刷新页面的时候需要重新计算大小
			fixed:代表的是固定, 灵活性比较低,但每次刷新页面的时候不会重新计算大小
		5)其他的CSS属性,均为之前学习的CSS属性
-->
<style>
    table{
        width:300px;
        height:300px;
        border:1px solid gray;
        border-collapse:collapse;
        border-spacing:0px;
    }
</style>
<table>
    <tr>
    	<td>小张</td>
        <td>小王</td>
        <td>小李</td>
    </tr>
    <tr>
        <td>小孙</td>
        <td>小赵</td>
        <td>小郭</td>
    </tr>
    <tr>
    	<td>小陈</td>
        <td>小谷</td>
        <td>小吴</td>
    </tr>
</table>
```

### 2) td的CSS属性

```html
<!--
	td的CSS属性
		1)边框属性
			border:1px solid gray;
		2)宽度高度属性
			width,height 可以设置一个单元格的大小
		3)取消单元格和内容之间的距离
			padding:0px
		4)隐藏空的单元格
			empty-cells:hide/show
-->
<style>
    table{
        width:300px;
        height:300px;
        border:1px solid gray;
    }
    td{
        border:1px solid gray;
    }
</style>
<table>
    <tr>
    	<td>小张</td>
        <td>小王</td>
        <td>小李</td>
    </tr>
    <tr>
        <td>小孙</td>
        <td>小赵</td>
        <td>小郭</td>
    </tr>
    <tr>
    	<td>小陈</td>
        <td>小谷</td>
        <td>小吴</td>
    </tr>
</table>
```

## 5. 表格新增的内容

### 1) 表格的标题标签

```html
<!-- 
	标签位于:table内部,tr出现的位置之前 
-->
<caption>文本</caption>
```

### 2) 表格的行分组标签

```html
<!--
	thead代表的是表格的头部分组标签,双标签,一个表格里面只允许有一个头部
	tbody代表的是表格的主体分组标签,双标签,如果没有使用主体,浏览器会将所有的tr标签自主划分到一个tbody中这个tbody是浏览器自行创建的;一个表格中可以使用多个主体
	tfoot代表的是表格的尾部分组标签,双标签,一个表格里面只允许有一个尾部
-->
<thead></thead>
<tbody></tbody>
<tfoot></tfoot>
```

### 3) 表格的列分组标签

```html
<!--标签使用位置:table表格里面,数值的含义代表的是多少列分为一组-->
<colgroup span="数值"></colgroup>
```

### 4) 表格的标题单元格标签

```html
<!--
	用来替换td,与td是同级别的,放在tr里面, 默认自带加粗和居中效果
-->
<th></th>
```

## 6. 综合案例

1. 案例1

2. 案例2

3. 案例3

   