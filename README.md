# BaiduFront-endTechnology
This Repository mainly contains the tasks I have finished in Baidu Institut of  Front end Technology

2017.2.26
    
    实现Task2，在Task1的基础上，增加了语义化，使用header,article,footer标签等等；
    同时增添了更多的样式使得页面变得更美观；
    并利用了css中的伪类选择器
    感觉比较繁琐耗费时间的是：表格的处理部分。发现表格不能用margin或者padding来设置tr/td；同时cellpadding和cellspacing在Google浏览器里面不起作用？
    增加border:2却不会显示边框？（未解决）
    去掉表格中单元格之间的空隙用：border-collapse:collapse即可。


    Task3-三栏布局的实现：
    1. 首先定义三个div，左边的设左浮动，右边的设右浮动；
    2. 将左右样式调好之后，为了使包含左右浮动的box不会高度塌陷，所以要给其设置overflow:hidden，将其变成一个BFC；
    3. 接下来设置中间的自适应宽度盒子，首先将其设了float:left，发现它会占满剩余的空间，而将右浮动的盒子挤到下一行去，因此中间的盒子不能设置左浮动；
    4. 所以将中间的盒子放到右浮动元素后面，并设置一定大小的margin值（如果放在右浮动的盒子之前，右浮动的盒子还是会在下一行）


    Task4-定位
    注意：对于绝对定位，它是相对于最近的非static元素的定位。