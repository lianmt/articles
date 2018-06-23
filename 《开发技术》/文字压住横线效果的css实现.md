![](http://upload-images.jianshu.io/upload_images/3317226-40e24399af4bd4f6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

```
<div class="third-party-login">
  <span>第三方登录</span>
  <div class="hr"></div>
</div>
.third-party-login {
  position: relative;
  width: 45%;
  height: 20px;
  margin: 0 auto;

  span {
    position: absolute;
    left: 50%;
    z-index: 2;
    display: block;
    width: 62.5%;
    margin-left: -31%;
    color: $black;
    font-size: 14px;
    text-align: center;
    background-color: #f0f0f0;
  }
  .hr {
    position: absolute;
    top: 50%;
    z-index: 0;
    width: 100%;
    height: 1px;
    background-color: #d1d1d1;
  }
}
```
