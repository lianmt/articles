Vuejs的核心思想是数据驱动的组件系统
计算属性基于依赖缓存和实现复杂的逻辑，不想有缓存用method方案。
v-if 删除插入，当 v-if 与 v-for 一起使用的时候， v-for 的优先级高于 v-if，v-for提供key
v-show 设置display值，频繁切换使用v-show=""较好
父组件通过props向内传递数据给子组件，子组件通过events给父组件发送消息。props 做验证、筛选，允许外部环境传递数据给组件。

自定义事件，子组件要把数据传递给父组件。
使用 $on(eventName) 监听事件
使用 $emit(eventName) 触发事件

用.sync可以双向绑定，.once 只能改变一次。
父组件访问子组件使用$children或$refs，子组件访问父组件使用$parent，子组件访问根组件：使用$root
events 事件，允许组件触发外部环境的action事件，监听v-$on和触发v-$emit可以组合，实现非父子组件之间的通信
slot 允许外部环境插入内容到组件的视图结构内，除非子组件模板包含至少一个插口，否则父组件的内容将会被丢弃。当子组件模板只有一个没有属性的 slot 时，父组件整个内容片段将插入到 slot 所在的 DOM 位置，并替换掉 slot 标签本身
创建组件构造器 Vue.extend()、注册 Vue.component()、Vue实例内component定义组件、组件应该挂载在某个vue实例下，否则不会生效、Vue实例的局部组件
使用script type=“text/x-template” id=“abd”   Vue.component(‘abd’, template: ‘#abd’);
使用template标签 id=“abc”，但是不加属性

methods 只有纯粹的数据逻辑，而不是去处理 DOM 事件细节
模型层(model)只是普通 JavaScript 对象，修改它则更新视图(view)。
属性必须在 data 对象上存在才能让 Vue 转换它，这样才能让它是响应的。
使用 Vue.set(object, key, value) 方法将响应属性添加到嵌套的对象上

bug
![](http://upload-images.jianshu.io/upload_images/3317226-c30462c48ca36374.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

vue组件笔记：
### 组件
> 创建一个Vue实例
注册一个全局组件
需在创建Vue实例之前注册自定义元素
Vue实例局部注册组件 components: {}
DOM模板解析受原生HMTL限制，可以使用is属性扩展
组件内data必须返回一个对象
父组件——props子组件；子组件——events父组件
子组件通过props声明期待获得的数据，通过属性把值写进子组件
**统一使用kebab-cas命名**
数据绑定用v-bind
动态语法用v-bind代替字面量语法
父组件带动子组件更新，子组件不应该在内部改变prop，用局部数据和计算机属性代替。（特例是对象或数组）
**自定义事件**：子组件把数据传递给父组件
$on(eventName) 监听事件
$emit(eventName)触发事件
子组件内用$emit()触发事件，用v-on来监听子组件传递给父组件的事件
v-on:click.native="doTheThing" 给组件绑定原生事件
父子双向绑定，.sync修饰符改为 v-on:foo="bar" @update:foo="val => var = val"，并显式地出发一个更新事件 this.$emit('update:foo', newValue)
状态管理：非父子组件通信，使用一个空的Vue的实例作为中央事件总线。
使用slot分发内容
父组件模板的内容在父组件作用域内编译；子组件模板的内容在子组件作用域内编译。
父组件模板不应该知道子组件的状态。
单slog标签的内容被视为备用内容
具名slot
作用域插槽，使用scope传入props数据，把slot设置的text等属性都引入到props对象上，用于template 中使用
动态组件，通过data 下currentView属性，传入不同的组件名称来动态显示
keep-alive 切换前的状态或避免重新渲染
**杂项**
为可复用组件定义一个清晰的公开接口
使用ref为子组件置顶一个索引ID
异步组件和vue-router 配套使用
组件命名约定：在component 中形式自定，在HTML模板汇总，请使用kebab-case，未设置slot 的标签，可以使用闭标签
组件有name选项时，可以递归调用自己；全局注册一个组件，全局的ID作为组件的 name 选项，被自动设置。
避免组件间的循环引用：在components中注册时，框架自动处理了；使用webpack打包工具的时候，在beforeCreate声明周期汇总注册组件优先级。
如果子组件有 inline-template 特性，组件将把它的内容当做她的模板，而不是把它当做分发内容
对低开销的静态组件使用v-once
