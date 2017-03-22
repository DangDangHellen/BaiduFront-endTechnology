﻿# BaiduFront-endTechnology
This Repository mainly contains the tasks I have finished in Baidu Institut of  Front end Technology

2017.3.15 YaoYao-Institute

     Task1和Task2-表单验证
     Task1实现比较简单，给按钮增加一个点击事件，并实现点击处理函数，即验证表单输入是否合法；

     1. Task2为了实现页面中的样式，利用了flex布局，使得每个表单及其label为一个整体并按column方向排列；而对于表单和其label再单独按row方向排列；
     2. 由于script脚本在body之前，所以浏览器会首先解析script脚本，因此为了避免由于script脚本造成的阻塞，因此将处理代码都写在window.onload = function(){}中，使得页面加载完成时再运行JS程序；
     3. 表单验证涉及到很多类型的验证，比如名称表单以及密码表单等等，其值不能为空；邮箱表单要利用正则表达式来判断输入是否一个邮箱的格式；手机号表单要按照手机号的格式来判断；
     4. 表单的focus和blur事件，其事件处理函数用到了this,对于this的理解更加深刻了一些，处理函数中的this其实就是.onfocus和.onblur之前的那个节点（对象）；
     5. 对于一些重复的函数进行了函数封装，比如取当前节点的下一个相邻兄弟节点。遇到了一个问题，就是一开始取出的都是Text类型的节点，后来发现，这种方式也会把空格作为相邻节点来处理，因此利用nodeType来判断是否为元素节点，从而成功取到相邻兄弟元素节点。
     
     ExtendTask2-对Task2进行了一些扩展。
     1. 当输入不符合验证条件时，点击提交按钮，对应的输入框会抖动一下，引起用户的注意。（但我觉得抖动效果稍微有点生硬，暂时还没有想到利用原生JS去做）；
     2，将错误时添加的样式封装起来，并将正确时添加的样式也封装起来，由于函数内部用到了this，所以外部调用时需用apply函数改变作用域。

     Task3-表单联动
     将第一级select中的option与第二级select中的option通过class名关联起来，并且利用select的onchange事件，实现每个option对应的第二级内容，相对应的内容设display:block属性。


2017.3.22
     Task4 --会跳的小方格
     主要的问题：
     1. 关于小方格的旋转问题（注意复杂情况，即先向左旋转，再向左，又向右等等）
        如果直接旋转用固定角度的话，当先让向左旋转之后，有让向右旋转胡直接变到初始状态向右旋转的状态。
        因此采用角度累加的方式，就简单一些了。避免角度一直累加，让角度模360，避免不必要的页面渲染；
     2. 关于实现GO时，蓝色小方格的朝向问题
        开始想的问题是0，1，2，3分别代表上右下左，因此向相应的方向运动时，这个值应该对应的加朝向方向的数值。
        但后面在判断时，出现一个问题，即直接利用方向值来判断朝向了，应该利用其模4的值。
     3. 还需注意：top,left值为字符串，要先将其取数值所在的长度，然后转为整数类型即可。