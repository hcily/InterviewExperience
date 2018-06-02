# 炎枭的面经-InterviewExperience 
## 面试准备：
### 自我介绍，系统的说明经历过的项目，为什么离职

自我发展规划：不断突破自我，在技术上以及与人的沟通能力上往更高的层次上发展。

团队的技术氛围很重要，在有很好的业务支撑的环境下，大家为了提出某个实际问题的解决方案，相互之间会进行交流学习。在没有很好的业务支撑的环境下，大家可以一起互相探讨现有技术的优化点，调研新的技术，互相分享学习心得。


#### 知识梳理：
https://juejin.im/post/587dbaf9570c3522010e400e?utm_source=wechat

https://github.com/LRH1993/android_interview

#### 学习资料：
https://blog.csdn.net/mwq384807683/article/details/70795881

#### 技术架构
https://github.com/davideuler/architecture.of.internet-product

***
#### [陌陌](#陌陌架构组)
#### [58](#58-1)
#### [爱奇艺](#爱奇艺-1)
#### [宝宝树](#宝宝树-1)
#### [阿里—大麦网](#阿里巴巴大麦网)
#### [头条-懂车帝](#头条-懂车帝-1)
#### [探探](#探探-1)
#### [美团打车](#美团打车-1)
#### [阿里用人标准](#阿里用人标准聪明皮实乐观自省谦卑)

***

### 陌陌—架构组

##### 数据库：怎样快速插入1万条数据，看过GreenDao的源码吗

> 加快数据库存储
一次插入多条，显示开启事务，关闭读、写同步，执行准备（类似存储过程，Stored Procedure），索引
https://blog.csdn.net/majiakun1/article/details/46607163

> GreenDao
https://blog.csdn.net/zhangjiaofa/article/details/49134341
提供的功能：加密，RxJava1，升级，注解（生成dao），异步封装（操作合并，减少事务的开关），
锁（IdentityScope）?   CursorWindow ?
速度快的原因：Transaction（事务），对SQLiteStatement进行缓存

> 对象关系映射（英语：(Object Relational Mapping，简称ORM，或O/RM，或O/R mapping）


##### 图片框架：Universal ImageLoader（看过源码吗）、glide（为什么用它，好处在哪里）、fresco

> UIL源码解析：下载进度、缓存策略、下载、显示、线程池
> https://blog.csdn.net/maplejaw_/article/details/51684130

> HashMap : https://blog.csdn.net/justloveyou_/article/details/62893086

> LinkedHashMap : https://blog.csdn.net/justloveyou_/article/details/71713781

> LruMemoryCache : 

> Glide源码：
https://blog.csdn.net/yulyu/article/details/60331803


##### 网络框架：volley（为什么不适用于大文件传输）、okhttp3（为什么用它，好在哪里，看过源码吗）

> Volley：默认开启4个网络请求线程，返回的结果存储在内存中（大文件传输会长时间占用线程，并且可能由于内存占用过多导致OOM）

> okhttp3 ：https://yq.aliyun.com/articles/78104?t=t1
        : https://blog.csdn.net/mwq384807683/article/details/71173442?locationNum=8&fps=1

> okio：

> https?  http2?   SPDY? 
https://zh.wikipedia.org/zh-cn/HTTPS
https://zh.wikipedia.org/zh-cn/HTTP/2
https://zh.wikipedia.org/zh-cn/SPDY

> 如何实现请求的优先级（高德）
Volley的请求队列：PriorityBlockingQueue : 

> okhttp的请求队列：SynchronousQueue :  

##### 如何定位一个不能复现的anr

> traces.txt文件  https://www.jianshu.com/p/f406d535a8bc
https://blog.csdn.net/jiangguangchao/article/details/54908477

> BlockCanary源码：
https://blog.csdn.net/bazhongren/article/details/51125113

> LeakCanary 源码：
https://blog.csdn.net/cloud_huan/article/details/53081120

> Reference : https://www.cnblogs.com/jabnih/p/6580665.html
> ReferenceQueue : https://www.cnblogs.com/dreamroute/p/5029899.html

> iTestin工具


##### 同一张图片，放在hdpi、xhdpi中，分别占用的内存是多少

https://blog.csdn.net/guolin_blog/article/details/50727753

##### binder的通信机制？看过源码吗？

##### Lopper源码：https://blog.csdn.net/a34140974/article/details/50638089

##### 哪些情况造成内存泄漏，内存溢出怎么处理？


##### activity的生命周期是如何实现的？Fragment呢？（高德）

> activity的生命周期：
http://weishu.me/2016/03/21/understand-plugin-framework-activity-management/
https://blog.csdn.net/yangxi_pekin/article/details/19977429

> Fragment的生命周期：
https://blog.csdn.net/jxxfzgy/article/details/44773797

##### 如何防止内存抖动（高德）？？？

##### 如何防止MVP的P功能过多，怎么拆分？？？（高德）

##### 如何判断是主线程（高德）
> ：https://blog.csdn.net/clevergump/article/details/50995612

##### Git为什么能实现分布式管理（高德）


##### Rxjava的线程切换是如何实现的（高德）
> https://blog.csdn.net/chenkai19920410/article/details/52515771

##### ThreadLocal的内部机制？

##### App安装、启动流程？
##### Android deeplink内部实现机制？
> http://blog.csdn.net/qq_27540131/article/details/74938234


##### Java线程，并发编程？

> 并发编程的优缺点：https://juejin.im/post/5ae6c3ef6fb9a07ab508ac85

> 线程状态转换：https://juejin.im/post/5ae6cf7a518825670960fcc2

> 锁？  https://blog.csdn.net/zqz_zqz/article/details/70233767
         https://blog.csdn.net/yanyan19880509/article/details/52345422
         https://www.cnblogs.com/-new/p/7256297.html
         
> Semaphore：    https://blog.csdn.net/qq_19431333/article/details/70212663

> 抽象的队列式的同步器 AQS：https://www.cnblogs.com/daydaynobug/p/6752837.html

> Exchanger的工作原理及实例：https://blog.csdn.net/carson0408/article/details/79477280
                         http://ifeve.com/concurrency-exchanger/    
                         
> CountDownLatch解析 ： https://blog.csdn.net/yanyan19880509/article/details/52349056

> CyclicBarrier：https://www.jianshu.com/p/ccf218dfcfa6


> classloader？https://blog.csdn.net/briblue/article/details/54973413

> 深入剖析volatile关键字 : https://www.cnblogs.com/dolphin0520/p/3920373.html
                        http://www.iteye.com/topic/652440

> 彻底理解synchronized：https://juejin.im/post/5ae6dc04f265da0ba351d3ff

> 锁膨胀：https://www.cnblogs.com/dsj2016/p/5714921.html

##### Java内存模型？
> https://blog.csdn.net/u012152619/article/details/46968883




> https://blog.csdn.net/marvel__dead/article/details/69220153

##### 类的加载过程
> https://blog.csdn.net/eff666/article/details/52203406

##### 方法区是线程安全的??

### 58
#### 一面：
+ handler的底层实现原理 ： https://blog.csdn.net/luoshengyang/article/details/6817933
+ MessageQueue的同步障碍机制：https://blog.csdn.net/tear2210/article/details/49815181
+ 不同线程间怎么通过handler发送消息
+ 线程间的通信
+ Android屏幕的刷新机制（16ms，绘制）：https://www.cnblogs.com/tiger-wang-ms/p/6592189.html
+ performTraversals :  https://www.jianshu.com/p/a65861e946cb
+ Vsync垂直信号\Choreographer
+ 循环调用requestLayout或者invalidate，每次调用都会触发onMeasure\onLayout或者onDraw吗？
+ View的三次measure,两次layout和一次draw https://blog.csdn.net/u012422440/article/details/52972825
+ Android的anr的内部原理：https://www.cnblogs.com/android-blogs/p/5718302.html
+ Watchdog：https://blog.csdn.net/kc58236582/article/details/78480640

+ HashMap怎么避免key冲突：    
+ 红黑树：https://blog.csdn.net/v_july_v/article/details/6105630
            
#### 二面：
+ 看过哪些开源库，详细说一下图片加载库的设计模式
            

### 爱奇艺
#### 笔试：
+ 横竖屏切换时activity的生命周期：https://blog.csdn.net/wenzhi20102321/article/details/68941263
+ 手势分发：https://www.cnblogs.com/Jackwen/p/5239035.html
+ 快速排序：
+ provider怎样共享数据：https://blog.csdn.net/luoshengyang/article/details/6946067
                     ：https://blog.csdn.net/u011240877/article/details/72848608

#### 一面：
+ 框架设计，怎么去封装图片库，能用到什么设计模式；
+ 线程池实现原理（核心线程数，线程最大数）：
+ SurfaceView和TextureView的区别：
>（SurfaceView源码浅析）
> https://blog.csdn.net/luoshengyang/article/details/8661317/
>
> https://www.cnblogs.com/wytiger/p/5693569.html
>
> （对比） https://blog.csdn.net/hejjunlin/article/details/58582919
                                                                    

#### 二面：优势是什么，缺点是什么，职业规划是什么，为什么离开现在的公司

>优势：接受新事物的能力强，学习能力强，有责任心，能很快融入团队
           
>缺点：有时候会钻一些牛角尖，比如有时候产品提出一个问题，我就会以技术的角度去思考这个问题到底能不能实现，但其实在很多时候证明，技术上不能实现的都可以归结为产品问题，重要的还是在产品端，前期的规划很重要，写代码，实施，只是产品研发其中的一个步骤。
           
>职业规划：技术的深度和广度上需要提升，在工作之余了解些后台，前段的技术而不单单是移动端，这样在制定方案的时候能够考虑的更加周到，这是硬技能方面。同时还要在软实力方面有所提升，比如和同事的沟通、对产品的理解等方面，在这一方面，我希望自己在不久的将来能够带领一个团队，能更多的站在产品的角度去思考问题，而不单单是从技术角度，从而以一个更大的角度去看待问题。
           
>为什么离开：

>高级开发者和中级开发者的区别，

#### 三面：
+ Android基础
+ activity的启动模式及应用场景：https://www.cnblogs.com/claireyuancy/p/7387696.html
                            ：https://blog.csdn.net/justinnick/article/details/52530279
+ 谈谈对框架的理解

### 宝宝树

#### 笔试：
+ interface和abstract的区别，interface的变量类型
+ activity和fragment的生命周期：https://blog.csdn.net/zjclugger/article/details/10442335
+ onTouchListener，onTouchEvent，onClickListener的执行顺序
+ StringBuilder和StringBuffer的区别，实现原理：
+ String的深入解析：https://www.cnblogs.com/xiaoxi/p/6036701.html
+ Parcelable和Serializable浅析
> ：https://blog.csdn.net/javazejian/article/details/52665164

> :  https://www.cnblogs.com/redcreen/articles/1955307.html

> ：https://blog.csdn.net/caowenbin/article/details/6532217

+ Java transient使用（ 涉及Externalizable）： https://www.cnblogs.com/lanxuezaipiao/p/3369962.html

#### 一面：
+ handler的实现原理
+ 线程池的核心线程数和最大线程数（爱奇艺也面到）过）：https://blog.csdn.net/wuseyukui/article/details/49617187
+ Thread源码解读：https://blog.csdn.net/owenchan1987/article/details/72021687
+ 守护线程（Daemon）：    https://blog.csdn.net/shimiso/article/details/8964414    
+ SparseArray\ArrayMap：https://blog.csdn.net/u010687392/article/details/47809295
+ 事件总线EventBus源码：https://www.jianshu.com/p/f057c460c77e


### 阿里巴巴—大麦网

#### 电话面试：
+ 工厂模式
+ 了解哪些些最新的技术
+ 热修复 : https://www.cnblogs.com/popfisher/p/8543973.html
         : 方法修复（native、java hoke）、类修复（dex替换）
+ Android P
+ 在项目中遇到最印象深刻的事情（技术难点）
                  
+ dalvik和art的区别
  Ahead-of-time(AOT) compilation instead of Just-in-time(JIT)

+ Android 打包流程：https://www.jianshu.com/p/d29c37dda256

+ 插件化：https://www.jianshu.com/p/353514d315a7

+ SVG图片生成原理：

+ 网络数据传输分片：

+ Okhttp使用遇到过哪些问题：

+ Android中killProcess()、System.exit(0)及finish()的区别
https://blog.csdn.net/freelander_j/article/details/50374900


### 头条
+ 头条博客：https://techblog.toutiao.com/tag/android/
+ Android瘦身：https://techblog.toutiao.com/2017/09/20/untitled-11/


### 头条-懂车帝

+ 线程
+ HandlerThread
+ 锁
+ view的事件分发： https://blog.csdn.net/carson_ho/article/details/54136311
                  https://www.jianshu.com/p/e99b5e8bd67b

+ view的绘制，onLayout，onMeasure（MeasureSpect），onDraw
+ MeasureSpect:https://blog.csdn.net/lamp_zy/article/details/51567942
+ viewpager的内部实现：
+ 深入浅出RecyclerVIew： https://kymjs.com/code/2016/07/10/01/
+ Hashmap的数组长度为什么是2的幂次方？：确保通过hashCode和（length-1）求模（使用的是二进制的与运算）
                                                                       快速找到在数组中的位置

+ java四种引用及使用场景：https://yq.aliyun.com/articles/576226

+ 算法：
> 横向打印二叉树
>
> 合并两个有序链表

+ 架构：MVC、MVP、MVVM
+ 设计模式：开发中常用的设计模式


### 探探

+ activity的生命周期，一个activity启动另外一个activity，第一个activity的onStop一定会被调用吗？
：https://blog.csdn.net/baidu_32472003/article/details/79970992

+ 手写两个线程安全的单例模式。https://blog.csdn.net/jason0539/article/details/23297037/

* 数组大小n+1，数组中数的范围是1-n，并且数组中有且仅有2个重复的数。
将这两个重复的数找出来。要求时间是O（n），空间是（1）。
如果在不改变数据本身的情况下呢？


### 美团打车

#### 一面：
+ Java虚拟机内存模型
+ Java的GC机制
+ 手写全排列算法（递归或者迭代）： https://blog.csdn.net/summerxiachen/article/details/60579623
                                         https://blog.csdn.net/jacky_chenjp/article/details/66477538

#### 二面：
+ okhttp的gzip功能
+ Looper在访问空队列时的等待原理（机制是什么）
+ 自旋锁的机制
+ 多线程问题：最多只能有三个线程同时访问一个方法
+ handler的message为什么不用new

#### 三面：
+ 了解OpenGL吗
+ SurfaceView的内部实现原理
+ 使用数组或者链表实现一个栈，写出具体的pop和push方法。要求：支持范型、线程安全。

#### HR： 
+ 自己的优势是什么
+ 为什么离开
+ 今后的规划
          

***

### 阿里用人标准：聪明、皮实、乐观、自省、谦卑

* 聪明：
你的老板有没有不采纳你建议的时候?
他有没有和你交流为什么不采纳？
你接受他的理由吗?
(聪明人，知进退，一定会问老板理由)

* 皮实：
当你的老板当众批评你的时候，你是怎么想的?
是不是觉得他不够给面子，应该先和你私底下商量一下?
(当众被批评，用好奇心面对所受到的批评和指责，这是皮实的最正能量的解释)

* 乐观：
如果你没有被我们看中，会不会不爽?
(如果回答，不会啊，没什么，说明不乐观，如果回答会有点失落，但是我会了解为什么，然后改进再来过）

* 自省：
一年前，你的老板认为你的不足是什么?
当下，你的老板认为你的不足是什么?
你觉得你自己哪些方面不足，阻碍了你的晋升?
(会自省的人，和自己的老板一定有很好的沟通，而且会得到他人的指点，尤其是自己的老板)

* 谦卑：
一个工作年限比你少的人，轻而易举的解决了你的技术难题，你会如何去请教他?
如果你能够解决你的老板无法解决的问题，你会不会希望拿到和你的老板同样高的薪水?
(弱于比自己年轻的人，不耻下问；强于比自己尊贵的人，更要虚怀若谷)





