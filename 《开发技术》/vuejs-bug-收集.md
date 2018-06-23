01. 这样设置网页标题，在微信上点击上一页的时候有bug，标题会缓存起来，**没有更改**。
```
Vue.directive('title', {
  inserted: function (el, binding) {
    document.title = el.innerText
    el.remove()
  }
})
<div v-title>标题内容</div>
```
推荐使用
```
router.beforeEach((to, from, next) => {
  document.title = to.meta.title || 'oola'
}
```
02. content="widht=750 user-scalable=no”，在适配的时候会兼容问题，会导致项目重做
