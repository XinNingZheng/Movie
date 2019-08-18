# Movie
一个调用豆瓣api显示最新电影信息的微信小程序

第一次开发微信小程序，有以下总结
 1.小程序目录需要是空文件夹
 2.腾讯云只支持node.js和php
 3.项目自动生成的四个文件的作用：指定腾讯云项目的目录、小程序端的代码、项目描述、项目配置
 4.四种基本文件:.json:配置文件，以json格式存储一些配置（全局配置、页面配置、项目配置）
                .wxml:模板文件，描述网页结构，相当于html
                .wxss:样式文件，调整页面样式，相当于css
                .js:脚本逻辑文件，页面和用户的交互逻辑
 5.list:列表个数2-5
   pagePath:配置路径，pages里配置过的
   text:显示的文字
   iconPath:没被选中时显示的图片
   selectediconPath:选中时显示的图片（图片不支持网络图片）
 6.数据绑定:小程序中的数据一般请跨下要从动态的服务端获取，再渲染输出到视图中显示
            WXML中的动态数据均来自对应Page的data
            数据绑定使用Mustache语法（双大括号）将变量包起来
 7.数据、图片、数组、列表
   问题：warning 在使用wx:for的时候要保证有一个wx:key="唯一标识"配套
 8.列表渲染：wx:for循环列表 {{index}}表示循环时候的索引，{{item}}表示索引的值 
   条件渲染：wx:if wx:else和hidden
   使用wx:if 　不显示的内容不会在Wｘｍｌ体现
   但是hidden　不显示的内容只是会在Ｗｘｍｌ体现
   需要频繁切换的话hidden更好
   运行过程中条件不太可能变化的话用wx:if好一点
 9.用于小程序的样式语言（类似于CSS）
   尺寸单位：rpx　可以根据屏幕宽度自适应，适配不同宽度的屏幕
   引入外部wxss：＠import‘./test_0.wxss’
 10.第三方样式库: WeUI：小程序官方ui库
                 iView Weapp有pc端 还有后台管理系统
                  Vant Weapp
 11.事件绑定的两种方式:bind catch
    区别：bind允许事件冒泡，catch不允许
 12.事件对象：代表事件的一个状态，当组建绑定的事件被触发的时候，就会传递一个事件对象到绑定的函数中
 13.微信小程序云开发:腾讯云和微信团队深度合作推出的全新的小程序的解决方案，云开发开发者可以将服务端的部署和运营环节托管给腾讯云，
                    不用在运维和管理投入很多的精力。
