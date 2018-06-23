### 组件刷新
```
<...>
    <router-link :paht="'/list' + '?_=' + new Date().valueOf()"></router-link>  // 增加当前时间戳_参数
</...>
然后在组件当中watch这个时间参数就可以了：
<...>
    export default {
        ...
        watch: {
            "this.$router._": function() {
                // refresh data here
            }
        }
        ...
    }
</...>
```

### 无法支持服务端渲染异步组件：<div id="app" server-rendered="true”>
### 组件内新增实现属性继承
propb仅仅被渲染普通html属性，如果想让属性能够向下传递，即使prop组件没有被使用，你也需要在组件上注册
$attrs包含所有未被注册的props
