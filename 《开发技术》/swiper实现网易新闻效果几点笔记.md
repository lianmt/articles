实现移动端既能 左右滑动导航跟着变又能点击导航切换页面
```
var mySwiper = new Swiper('.swiper-container', {
  onTransitionEnd: function(swiper) {
    $('li').eq(mySwiper.activeIndex).addClass('on').siblings().removeClass('on');
  }
})
$('li').click(function() {
  $(this).addClass('on').siblings().removeClass('on');
  mySwiper.slideTo($(this).index(), 1000)
});
```
[源码地址](https://github.com/lianmt/brand)
