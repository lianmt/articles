### 01. css编写超出元素宽度的中文显示省略号
```
p { 
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
```
###  02. 只显示一行文字
```
p {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```
### 03. 移动端横向滚动
```
ul {
-webkit-overflow-scrolling: touch; // IOS设备滑动流畅 允许独立的滚动区域和触摸回弹
  white-space: nowrap; // 不换行
  overflow-y: hidden; // 设置横向可滚动
}
ul li {
  display: inline-block;
}
```
### 04. 清除input border fouce阴影
```
input {
  outline: none;
}
```
### 05. css三角形
```
.triangle-up {
  height: 0;
  width: 0;
  border: 12px #e5c3b2 solid;
  border-color: transparent transparent #e5c3b2 transparent;
}
```
### 06.  line-height 比 height 多一，这样就上下居中了
```
ul li {
  height: 30px;
  line-height: 31px;
}
```
### 07.  背景图片固定不动
```
.parent-box {
  height: 100px;
  background: url('') center center no-repeat fixed;
  background-size: cover;
}
```
[demo](https://jsfiddle.net/lianmingtang/oev7w35o/)
### 08. hover动效
```
div {
  transform: translateY(-100%);  
  transition: .2s all ease-in-out;

  &:hover {
    transform: translateY(100%);    
  }
}
```
### 09.  hover 板块向上抬的效果
```
div:hover {
  z-index: 2;
  transform: translate3d(0,-2px,0);
  box-shadow: 0 15px 30px rgba(0,0,0,.1);
}
```

### 10.  缓动，进来效果
```
div:hover {
  transition: 800ms all ease;
   transform: translateY(68px);
   -webkit-transform: translateY(68px);
}
```

### 11. 清空select样式
```
select {
  appearance: none;
  -moz-appearance: none;
 -webkit-appearance: none;
}
```
