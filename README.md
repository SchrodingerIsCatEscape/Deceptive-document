﻿#Deceptive-document
---
**功能简介**

	    主机中运行Deceptive后，程序会循环检测磁盘驱动器，当发现U盘插入主机时，就开始对U盘内的文件按照预设的优先级进行
		
    选择性的替换，影响文件替换的因素有两个，最重要的是文件名长度，其次是文件修改时间。替换后U盘内被替换的文件会更改为隐
		
    藏属性，然后生成一个图标一样，名称极为相似的病毒程序，从而诱导用户点击。
		
	    当用户点击病毒程序后，病毒程序会打开原本被隐藏的文件迷惑用户，并偷偷的在后台运行，实现各种预设的程序功能，完成对
        
    主机的入侵。

**使用说明**

	    该程序是在windows上，利用vs2013开发完成。
		
	    test是文件替换程序，主要实现U盘检测，文件替换优先级判断，文件替换的功能。
        
        Funny是病毒程序的一个最简单的实现，无论 怎么设计其他的病毒程序，首先有两点要注意，一是病毒程序的图标应该与被替换
        
    文件基本相似，二是病毒程序必须具有打开隐藏的被替换的文件的功能，即创建进程。
		
        图标资源包中有Funny中用到的五种图标的图标资源文件，需要更多的图标资源文件可以利用网上各种图标提取工具获取。

**注意事项**

	    1.test在vs2013上进行编译时后需修改两处项目属性，一个是将UNICODE字符集改为多字节字符集，二是关闭文件安全检查。
        
    才能通过编译。
		
	    2.工具包中的kidding可执行程序，全是由Funny生成后重命名得到，只是替换了生成exe时的资源图标。名称kidding后面接
        
    数字0-4必须同资源图标一一对应，比如word文档对应的是kidding，txt文件对应的是kidding3，不然会导致替换文件与被替换文
    
    件的图标对应出错。具体原因看test源代码应该很容易理解。

	    3.目前只针对五种类型的文档进行替换，文件夹、txt文本、word文档、ppt、可执行程序(.exe)。
	    
**程序流程示例**  
    
![image](https://github.com/scu-igroup/Deceptive-document/blob/master/image/run.gif)


	
