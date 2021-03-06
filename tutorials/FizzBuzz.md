# Tutorial: 412. Fizz Buzz

## 题目
原题链接[FizzBuzz](https://leetcode.com/problems/fizz-buzz/)，大家点进去就能看到LeetCode上的原题，注册个账号就能做题了。下面给出题目的大概翻译：
>给定一个正整数N，要求返回一个有N个元素的List<String>，对应从1到N的N个数。当对应的数为15的倍数时，在list中的对应位置添加FizzBuzz；当对应的数为5的倍数时，添加Buzz；当对应的数为3的倍数时，添加Fizz。
举例如下：<br>
n = 15,<br>
Return:<br>
[<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"1",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"2",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Fizz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"4",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Buzz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Fizz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"7",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"8",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Fizz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Buzz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"11",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"Fizz",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"13",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"14",<br>
    &nbsp;&nbsp;&nbsp;&nbsp;"FizzBuzz"<br>
]

## 算法
解这道题不需要链表之类的高级数据结构，用内置的List类型来解决就可以了。算法在题目中已经讲解的非常明白，这里就不在赘述了。

## 代码
```Java
public class FizzBuzz {

    public void Show(int n){
        List<String> list=new ArrayList<>();
        list=fizzBuzz(n);
        for (int i=0;i<n;i++){
            System.out.println(list.get(i));
        }
    }

    public List<String> fizzBuzz(int n) {
        List<String> list=new ArrayList<>();
        for(int i=1;i<=n;i++){
            if (i%3==0&&i%5==0){
                list.add("FizzBuzz");
            }else if(i%3==0){
                list.add("Fizz");
            }else if(i%5==0) {
                list.add("Buzz");
            }else{
                list.add(String.valueOf(i));
            }
        }
        return list;
    }

}
```

# Copy Right
Copyright © 2015 - 2016 [stormlin](http://www.stormlin.com/). All Rights Reserved.
Go to my [CSDN blog](http://blog.csdn.net/atmiao) for more interesting things.
For more detail, follow my WeChat Subscription by scanning the QR code below.

![QR Code](http://img.blog.csdn.net/20161209103948618?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvYXRtaWFv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)