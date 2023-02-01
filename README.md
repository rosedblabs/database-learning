**学习资料 PDF 及数据库相关书籍，可在我公众号领取**，关注后回复关键字“**数据库**”

![Snipaste_2023-02-01_09-58-05.png](https://cdn.nlark.com/yuque/0/2023/png/12925940/1675216713682-a3cab6f7-93ca-4699-999d-223ba77cbc97.png?x-oss-process=image%2Fresize%2Cw_1500%2Climit_0)

***

# 数据库/存储学习路径推荐

我自己就是从业务自学转入数据库内核研发岗位的，根据自己的经历，简单总结了一下入门数据库相关的学习路线、学习资料、项目书籍推荐等，大家可以参考。

## 必看课程

CMU-15445 和 CMU-15721

[https://www.youtube.com/@CMUDatabaseGroup](https://www.youtube.com/@CMUDatabaseGroup)

这两个不用多说，经典的数据库入门教程，由数据库的大佬 Andy Pavlo 亲自授课。可以了解到数据库的基本概念，例如存储、BufferPool 管理、索引、优化器、执行器、事务、MVCC 等。



15445 的实验部分是基于其开源的教学项目 [bustub](https://github.com/cmu-db/bustub)，补全其中几个重要的部分，这个项目是 C++ 写的，如果对 C++ 不熟悉的话，那么我觉得实验部分可以暂时跳过，有多余的精力再来搞，毕竟我们是来学数据库的，而不是学 C++ 的。

## 存储小项目

学习教学课程的同时，顺便可以了解下存储方面的内容，例如 B+ 树，bitcask，LSM Tree，以及 LSM Tree 的优化 Wisckey，不用专门去学，找几篇文章看看，了解下基本概念，或者直接看看论文。



然后自己去实践写一个，例如写一个简单的 bitcask、B+ 树存储引擎，或者 LSM 存储引擎。



之所以推荐写存储类的小项目，主要是因为存储层的 KV 一般比较好实现，同时又能够了解到一些数据库的基本设计理念。



这里推荐下我的两个项目：
> [https://github.com/flower-corp/rosedb](https://github.com/flower-corp/rosedb)
>
> [https://github.com/flower-corp/lotusdb](https://github.com/flower-corp/lotusdb)

## 事务/MVCC

这部分网上的资料比较多，可以看看事务的一些基本概念 ACID，然后看看如何去实现的，可以借鉴其他数据库例如 MySQL、PostgreSQL，关于事务实现原理分析这方面的文章比较多。



概念了解差不多之后，可以自己动手实现，例如可以在自己写的存储项目的基础上，加上事务的功能，保证事务原子性、隔离性，以及并发读写的性能，自己上手撸肯定比只了解理论好很多。



其他的一些部分，例如 parser、执行器、优化器、向量化等等，比较复杂，自己从头搞一个的难度比较大，我觉得可以简单看看资料，了解一下基本概念，工作之中再针对性的查漏补缺。



当然如果你对某个部分特别感兴趣的话，比如优化器之类的，也可以多去了解然后自己实践，我这里推荐存储和事务的实现，是因为相对来说比较容易上手。

## 分布式

这部分内容首推 Mit.6824，分布式系统入门的首选课程。

https://www.youtube.com/@6.824/videos

有精力的话可以跟着把实验部分做完。



然后可以挑战下 PingCAP 的 talent plan 中的 TinyKV，它和 6824 的实验部分比较类似，实现一个基于 raft 的分布式 KV 存储系统，难度比较大，但是代码框架已经搭好了，只需要往里面添加内容即可，测试也比较完备。

https://github.com/talent-plan/tinykv



如果还有时间的话，可以再上一个台阶，挑战下 PingCAP talent plan 的 TinySQL 项目，主要是实现一个简单的分布式数据库项目，有完备的文字教程

https://github.com/talent-plan/tinysql

## 工作或实习

当然，其实最好的办法，还是能够直接参与到工作实践当中，这样学习起来是最快的，可以向 leader 请教，和同事交流等。



如果自身又没有太多经验的话，可以试试那些愿意接纳转数据库内核的公司，这可能会要求你有其他亮眼的东西了，比如基础比较扎实，折腾过自己的项目之类的。



能把上面提到的这些东西认真学习下，完成个 60% 左右，我觉得应对一些面试就应该没有太大的问题了。

---

为了帮助你更高效的学习，我还整理了一份数据库开发的学习资料，数据库的各个方面都涉及到了，例如 SQL、优化器、执行引擎、存储等等，包含一些优质的书籍、论文、视频课程、博客等，还有一些优质的教学类项目。

![image.png](https://cdn.nlark.com/yuque/0/2023/png/12925940/1673770833130-d80eaccc-6fce-4e23-bdc5-5b00d1bb384f.png#averageHue=%23ececec&clientId=ufa50e856-2120-4&from=paste&height=746&id=ua30dabf1&name=image.png&originHeight=1492&originWidth=1700&originalType=binary&ratio=1&rotation=0&showTitle=false&size=296215&status=done&style=none&taskId=u7b00b1aa-bd87-48b7-934f-e9ca536db81&title=&width=850)

总计十几页的 PDF，一次性送给你，方便提升学习效率。![image.png](https://cdn.nlark.com/yuque/0/2023/png/12925940/1673770714528-fc5cd43d-54c6-4c7f-8c8a-b0e8106fdf3e.png#averageHue=%23f7f7f7&clientId=ufa50e856-2120-4&from=paste&height=615&id=uf81c3cca&name=image.png&originHeight=1230&originWidth=1294&originalType=binary&ratio=1&rotation=0&showTitle=false&size=321082&status=done&style=none&taskId=uca8d9770-71df-4791-9af6-a3cdad4d763&title=&width=647)还有一些关于数据库方面的优质 PDF 书籍，可以参考学习：![image.png](https://cdn.nlark.com/yuque/0/2023/png/12925940/1675175402743-f5987338-d67e-4c0d-a574-9c1a7f743ca0.png#averageHue=%23dbd8cf&clientId=u6861054c-f8dc-4&from=paste&height=451&id=u4b53b520&name=image.png&originHeight=902&originWidth=1682&originalType=binary&ratio=1&rotation=0&showTitle=false&size=897755&status=done&style=none&taskId=u6b44cf46-3c87-4c40-be5f-d7d56162dc1&title=&width=841)这份学习资料 PDF 和所有的书籍都可以在我的**公众号领取**，后台回复关键字【**数据库**】。

![Snipaste_2023-02-01_09-58-05.png](https://cdn.nlark.com/yuque/0/2023/png/12925940/1675216713682-a3cab6f7-93ca-4699-999d-223ba77cbc97.png?x-oss-process=image%2Fresize%2Cw_1500%2Climit_0)

