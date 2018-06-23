React：颠覆式前端UI框架 
先上干货。好文章：
[Web应用的组件化开发？](http://blog.jobbole.com/56161/)
[关于React你需要知道的13件事 - aimforsimplicity.com](http://www.zcfy.cc/article/13-things-you-need-to-know-about-react-aimforsimplicity-com-2283.html)
[一看就懂的ReactJs入门教程-精华版](http://www.cnblogs.com/yunfeifei/p/4486125.html)
[React.js 2016 最佳实践](http://www.alloyteam.com/2016/01/reactjs-best-practices-for-2016/)
[如何学习React](https://github.com/petehunt/react-howto/blob/master/README-zh.md?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[React项目构建三部曲](https://github.com/lianmt/react-lesson)
[前端早读课收集发表系列](https://mp.weixin.qq.com/mp/homepage?__biz=MjM5MTA1MjAxMQ==&hid=27&sn=5ee28d7e18b7a604decf5aee6e23f41c&devicetype=iOS10.3.3&version=12020810&lang=zh_CN&nettype=WIFI&ascene=0&fontScale=100&pass_ticket=ARGrwX74sC%2Fs2Vm9DcjJ3YaXyuLOkKjMHD8mhGW2pytI0%2FLQoU5yzR7CDKZHXtRS&wx_header=1&scene=1)
[分享一个 react + redux 完整的项目，同时写一下个人感悟](http://react-china.org/t/react-redux/9072) ----------[对应的gitlab项目](https://github.com/bailicangdu/react-pxq)
[大腿：基于webpack + react + react-router + redux + less + flex.css + ES6 的React版cnode社区](http://react-china.org/t/webpack-react-react-router-redux-less-flex-css-es6-react-cnode/6332)
[解剖react组件的多种写法与演进](https://zhuanlan.zhihu.com/p/26216173)
[揭秘react生态体系](https://zhuanlan.zhihu.com/p/26270621)

系统步骤学习文章：
[React全家桶--从零到入门](http://www.jianshu.com/p/2f744954e2d2)
[React启蒙（译）](https://zhangwang1990.gitbooks.io/reactenlightenment/content/%E5%88%9D%E6%8E%A2React.html)
[React.js 小书](http://huziketang.com/books/react/)
[阮一峰：React 技术栈系列教程](http://www.ruanyifeng.com/blog/2016/09/react-technology-stack.html)

选择UI框架：（我选择的是支付宝的Ant）
[[译] 快速构建原型最好用的 10 个 ReactJS UI 框架](https://juejin.im/entry/57ea0bc2a3413100624e62ff)

完整项目：
[嘟嘟微生活——我司主项目基于React全家桶的前端架构。](https://github.com/lianmt/dolife)

资源：
[React 专题](https://www.awesomes.cn/subject/react#应用-框架)
[我收集的Github项目](https://github.com/lianmt)
[慕课网：React.js 开发参见问题 Q&A](http://www.imooc.com/article/17442)
[我搭建的react脚手架](https://github.com/lianmt/react-cli)

怎么学习一个新技术？从官网开始
怎么开始一个新项目？搭建环境

react vs vue? （理念思想）
如果做一件事有两个方案，一个简单，一件困难，不用考虑，选择困难的那个。
组件划分得越细，负责的事情越少，维护起来就越简单，逻辑就越清晰。

编写react项目步骤：
目的是为了代码可复用性、可维护性
理解需求、分析需求、划分这个需求由哪些组件构成（拆分组件，保持你的组件无状态化）

前端组件化原则：
① 标准化
多人协作如果不制定一套标准的话，显然是进行不下去的，任何一个组件都应该遵守一套标准，可以使得不同区域的开发人员据此标准开发出一套标准统一的组件。（组建命名规则、就近原则、样式分离独立文件）。组件化要独立（数据、业务逻辑和交互）又要提供接口还要进行封装。
② 组合性
组件必定是需要相互嵌套组合的，这就需要组件间具有相互的独立性以及有良好的接口，这也是一个组件最基本的构成。
③ 重用性
组件内部应该是高聚合的，任何一个组件都应该是一个可以独立的单元，可以扩展到其他不同的应用场景。
④ 可维护性
任何一个组件应该都具有一套自己的完整的稳定的功能，仅包含自身的，与其它组件无关的逻辑，使其更加的容易理解，使其更加的容易理解，同时大大减少发生bug的几率。

哪些需要组件化？
要么可以复用的，要么就是一块比较大的逻辑比较复杂的单元。
复用代表这个组件要到处引用，一是为了抽象概念，二是为了后期更好地维护。
而比如像banner这种内部逻辑比较复杂的模块，为了更好梳理里面的逻辑也应该和父组件解耦，独立成一个单元。

Why要组件化?
应对复杂的不同状态和情况。

为什么不直接从 JSX 直接渲染构造 DOM 结构，而是要经过ReactDOM.render中间这么一层呢？
1. 把这个结构渲染到 canvas 上，或者是手机 App 上
2. 当数据变化，需要更新组件的时候，就可以用比较快的算法操作这个 JavaScript 对象，而不用直接操作页面上的 DOM，这样可以尽量少的减少浏览器重排，极大地优化性能。

react的一些情况：
1. 需要HTML结构写得好，然后拆分成react的开发方式
2. 考虑复用性，脑子里要有类的继承概念。这里要一定的功力
3. 是否能写成函数组件
3. 要动态传参，写出那个接口形式
4. 糅合redux
5. 非双向绑定，需要自己触发状态更新
6. 类似于java等后台的语法

一些重要的概念：
通过[querySelector和querySelectorAll](http://blog.csdn.net/z742182637/article/details/51655690)来选择选择DOM，传 . # element a[target]
 querySelectorAll返回的一个nodeList集合是非实时的结果。
所谓的 JSX 其实就是 JavaScript 对象

一些方法：
用ReactDOM代替react
子—>父，props
子—>父，绑定一个回调函数
子->爷，订阅
事件的传递或数据的交互，Redux对这些组件的状态进行管理。
Redux（全局状态）：
1. 不同身份的用户有不同的使用方式（比如普通用户和管理员）
2. 多个用户之间可以协作
3. 把交互和UI联系起来
每个独立的组件、最后整合成一个组件集合
拆分、组合、嵌套
手动管理数据和 DOM 之间的关系会导致代码可维护性变差、容易出错。写一个同一个的开关来改变状态，切记不可手动的操作DOM
mount，把组件的 DOM 元素插入页面，并且在 setState 的时候更新页面：

ReactJS庞大的生态系统、自定义渲染器JSX使用Virtual Dom降低DOM渲染
前端框架要考虑什么？
1. 函数式编程
2. 模块化
3. 模块加载器 Webpack
4. 包管理器 npm
5. 自动部署/编译/构建流水线，如果一直做重复的事情的话生命是很短暂的。
6. CSS预处理sass
7. 构建框架，处理基本的布局和样式，方法论，
8. 测试工具
9. 代码质量监控工具 eslint
