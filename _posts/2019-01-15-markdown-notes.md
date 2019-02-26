---
layout: default
---

浓缩的是精华
原链接：[点击这里](https://www.appinn.com/markdown)

Markdown其实支持HTML，可以直接在.md文件中写HTML标签

Markdown自动帮你转换`<`或者`&`这种特殊字符

段落之间需要用空行分割。
段落内想要换行的话，先输入两个以上的空格然后回车。   
就像这样

标题支持两种语法：Setext / atx。
Setext是用`===`和`---`  

这是用`===`的效果
==================

这是用`---`的效果
-----------------

Atx是在行首插入1到6个`#`。
注意：符号后面要加一个空格才会生效？

# 一个`#`
## 两个`#`

区块引用：在每行前面加上`>`
> 引用第一行
> 引用第二行   
> 引用第三行
>> 二级引用  
> ### 引用内的标题
引用后面的内容

无序列表使用`*`或者`+`或者`-`
* 第一行
+ 第二行
- 第三行

有序列表使用英文数字加一个英文句点
2. 第一行
   第一行结束

   新的段落
1. 第二行  
   第二行结束

代码区块也有两种显示方法  
行首缩进4个空格/1个制表符(**前后需要留空行**)

    if (true) {
        printf("hello all");
    }

或者使用```` ``` ````
```c++
if (true) {
    printf("hello again");
}
```

接下来是分割线，你可以使用  
`***`

***

`---`

---

`___`

___

链接分行内式与参考式  
行内式的链接类似于这样（别忘了http）：  
`[baidu](http://www.baidu.com)`  
[baidu](http://www.baidu.com)

参考式的链接类似于（别忘了http）：

    [baidu][b]
    [b]: http://www.baidu.com

[baidu][b]

[b]: http://www.baidu.com


使用*\**或者_\__进行强调  
使用**\*\***或者__\_\___进行强调

使用`` ` ``来包围代码：`printf()`  
也可以用两个``` `` ```来包围，这样能在中间显示反引号``` `` ` `` ```: `` ` ``

图片也分行内式和参考式  
行内式：`![example img](https://thumbs.dreamstime.com/b/%E7%A4%BA%E4%BE%8B%E5%8D%B0%E8%8A%B1%E7%A8%8E-28420393.jpg)`  
![example img](https://thumbs.dreamstime.com/b/%E7%A4%BA%E4%BE%8B%E5%8D%B0%E8%8A%B1%E7%A8%8E-28420393.jpg)  
参考式：

    ![example img][emp]

    [emp]: https://thumbs.dreamstime.com/b/%E7%A4%BA%E4%BE%8B%E5%8D%B0%E8%8A%B1%E7%A8%8E-28420393.jpg

![example img][emp]

[emp]: https://thumbs.dreamstime.com/b/%E7%A4%BA%E4%BE%8B%E5%8D%B0%E8%8A%B1%E7%A8%8E-28420393.jpg

很遗憾，目前还无法指定图片的宽高

最后两个：  
自动链接: `<http://www.baidu.com>` <http://www.baidu.com>  
反斜杠用来插入语法符号: `` \` `` look: \`
