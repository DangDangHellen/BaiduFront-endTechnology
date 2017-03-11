# BaiduFront-endTechnology
This Repository mainly contains the tasks I have finished in Baidu Institut of  Front end Technology

2017.3.10
     
     JavaScript任务一和二比较基本
     
     任务三在任务二的基础上，不仅要对字符串数据进行分解，利用split函数；另一方面还要对数据进行处理，即排序，本程序利用冒泡排序的算法；
     其中遇到的一个问题，是变量提升的问题，在交换数据时，声明了一个t变量，在第二次交换时，直接利用t作为中间数据进行交换，发现前一次交换的数据都是第二次交换时t的值了，所以就重新声明了另一个值。


     JavaScript任务四：
     重点在于添加时，怎么添加；appendChild()是在最后添加元素；insertBefore(insertNode，Node)是在Node之前插入insertNode节点；
     删除时怎么删，remove()是删除节点，只需改变里面的参数分别为第一个节点和最后一个节点即可。

     JavaScript任务五：
     在任务四的基础上，主要是在于字符串的处理，将其取字串，并转换为数值;
     另外一个用了冒泡排序算法进行排序，并重新设置div的高度达到视觉上的排序效果。

     在原先基础上，修改重叠部分代码，封装在一个函数中，减少代码量；
     另一方面，将由id获取元素的操作也封装起来。
     利用正则表达式判断输入的数据格式，必须都为数字。