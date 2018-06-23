```
router.afterEach((to, from) => {
  // console.log('PUSH===>>>' + location.pathname + '#' + to.fullPath)
  window._hmt.push(['_setAutoPageview', false])
  window._hmt.push(['_trackPageview', location.pathname + '#' + to.fullPath])
})
```
