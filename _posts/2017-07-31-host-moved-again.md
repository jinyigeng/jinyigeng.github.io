---
title: "jinyigeng.com 再度搬家"
layout: post
date: 2017-07-31 20:40
category: blog
author: jinyigeng
description: jinyigeng.com 再度搬家，这是人性的扭曲还是道德的...
---

这下看起来清爽多了。

是的，jinyigeng.com又搬家了，这次我搬到了稳定的GitHub Pages.

今天来点轻松的，比如和电脑玩游戏。

> 是这样的...
>
> 电脑先随机生成一个数字，让你猜，比他大就说比他大，反之亦然，直到猜中为止。

既然开始学C++了，就拿C++来学..不过我发现

**C++的随机数生成居然是假的！WRGETHJ%$H%#W$Q#FEGRHTJE**

转回Java...

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class JavaPlayground {
  //Playground [noun]: A place where people can play (大雾)
    public static void main(String[] args)throws IOException{
        System.out.println("正在生成随机数...");
        int num = (int)(Math.random() * 100);
        System.out.println("随机数生成完毕。");
        System.out.println("正在加载输入组件");
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));
        System.out.println("输入组件加载完毕。");
        int temp = 0;
        int times = 0;
        do {
            System.out.println("请输入您认为的随机数");
            System.out.print('>');
            temp = Integer.parseInt(reader.readLine());
            if (temp > num){
                System.out.println("您认为的数字比随机数大。");
                times++;
            }
            if (temp < num){
                System.out.println("您认为的数组比随机数小。");
                times++;
            }
            if (temp == num){
                System.out.println("太棒了，您猜对了随机数 " + num);
                times++;
                System.out.println("您仅使用了" + times + "次就猜对了这个随机数！");
            }
        } while(temp != num);
    }
}
```

接下来具体解析一下...

首先是控制台输入，控制台输出就很简单，`System.out.println()`即可，不过输入有点麻烦...

你需要导入`java.io.BufferedReader` `java.io.InputStreamReader` `java.io.IOException`

其中`IOException`是拿来报错用的。

生成随机数的方法是`Math.random()`，生成的随机数；类型是Double。

就这样，晚安~