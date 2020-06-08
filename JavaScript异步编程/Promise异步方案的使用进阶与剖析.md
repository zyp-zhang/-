### 1.Promise是什么？

抽象表达:
        
    Promise是JS中进行异步编程的新的解决方案。

具体表达:

    从语法来说，Promise是一个构造函数。
    从功能来说，Promise对象用来封装一个异步操作并可以获取其结果。
    
### 2.Promise的状态改变

pending--->fulfilled

pending--->rejected

说明:

    只有这俩种，且一个Promise对象只能改变一次
    无论变为成功、失败，都会有一个结果数据
    成功的结果数据一般称为value，失败的结果一般称为reason

