**常用标签**

标签 | 语义化
----|------|----
b | 表示关键字和产品名称
strong | 表示强调一段`重要的`文本
wbr | 表示安全换行
i | 表示外文词汇或科技术语，表示区分周围内容，并不是特别强调或重要性
em | 表示对一段文本的强调
s | 表示不准确的删除
var | 表示程序输出
del | 表示删除相关文字
u | 表示加下划线，不强调文本
ins | 表示加下划线，强调文本
small sub sup | 用于免责声明和澄清声明
code | 表示计算机代码片段的输入和输出，属英文范畴，需设置lang="en"
var | 表示编程语言中的变量，属英文范畴，需设置lang="en"
samp | 表示程序或计算机的输出，属英文范畴，需设置lang="en"
kdb | 表示用户的输入，属英文范畴，需设置lang="en"
abbr | 表示英文缩写
dfn | 表示术语，解释一个词或短语的一段文本
q | 表示引用来自其他地方的内容
cite | 表示引用其他作品的标题
ruby | 用来为非西方语言提供支持。<rp><rt>用来帮助读者掌握表意语言文字正确发音。比如：汉语拼音在文字的上方
mark | 突出显示文本，可用于做标记，文字加上一个黄色的背景
time | 表示时间和日期，推荐使用 jQuery 等前端库来实现日历功能
span | 表示一般性文本
pre | 表示预格式化，保留简单的排版，如换行
dl dt dd | 表示包含一系列术语和定义说明的列表。dt 在 dl 内部表示术语，一般充当标题；dd 在 dl 内部表示定义，一般是内容。
div | 用于布局，分组元素
figure figcaption | 使用插图
hgroup | 将一组标题组织在一起，如`<hgroup><h1></h1><h2></h2></hgroup>`
section | 表示重要概念或主题，定义一个文档的主题内容
article | 添加一个独立成篇的文档，里面可以包含头、尾、主题等一系列内容，在比较大的页面中会使用到，比如一片`博文`的列表，每篇博文，都有自己的头、尾、主题等内容。和此相似的还有`论坛的帖子`、用户的`评论、新闻`等。
address | 表示文档或 article 元素的联系信息
aside | 专门为某一段内容进行注释使用。
details | 生成一个区域，用户将其展开可以获得更多细节
summary | 用在 details 元素中，表示该元素内容的标题或说明
iframe | 表示内嵌一个 HTML 文档。其下的 src 属性表示初始化时显示的页面， width 和 height 表示内嵌文档的长度和高度，name 表示用于 target 的名称。

**video 标签**

标签 | 语义化
----|------|----
src | 视频资源的 URL
width | 视频宽度
height | 视频高度
autoplay | 设置后，表示立刻开始播放视频
preload | 设置后，表示预先载入视频。none 表示播放器什么都不加载；metadata 表示播放之前只能加载元数据（宽高、第一帧画面等信息）；auto 表示请求浏览器尽快下载整个视频。
controls | 设置后，表示显示播放控件
loop | 设置后，表示反复播放视频
muted | 设置后，表示视频处于静音状态
poster | 预览图，指定视频数据载入时显示的图片
source | 引入不同格式的url，兼容多个浏览器

**audio 标签**

标签 | 语义化
----|------|----
src | 视频资源的 URL
autoplay | 设置后，表示立刻开始播放视频
preload | 设置后，表示预先载入视频
controls | 设置后，表示显示播放控件

**form标签**

标签 | 语义化
----|------|----
action | 表示表单提交的页面
method | 表示表单的请求方式：有 POST 和 GET 两种，默认 GET
enctype | 表示浏览器对发送给服务器的数据所采用的编码格式。有三种：application/x-www-form-urlencoded（默认编码，不能将文件上传到服务器）、multipart/form-data（用于上传文件到服务器）、text /plain（未规范的编码，不建议使用，不同浏览器理解不同）
name | 设置表单名称，以便程序调用
target | 设置提交时的目标位置：_blank、_parent、_self、_top
autocomplete | 设置浏览器记住用户输入的数据，实现自动完成表单。默认为 on 自动完成，如果不想自动完成则设置 off（丧失自动提示功能）。
novalidate | 设置是否执行客户端数据有效性检查，后面课程讲解。
`fieldset` | 对表单进行`编组`
`legend` | 添加`分组说明标签`
`reset` | `重置form表单`

**input textarea标签**

标签 | 语义化
----|------|----
autofocus | 让光标聚焦在某个 input 元素上，让用户直接输入
autocomplete | 单独设置 input 元素的自动完成功能
form | 让表单外的元素和指定的表单挂钩提交，`fieldset textarea `标签同样可以设置
disabled | 禁用 input 元素
type | input 元素的类型，内容较多，将在下节课展开讲解
name | 定义 input 元素的名称，以便接收到相应的值

**button标签在type 属性为 submit 时**

标签 | 语义化
----|------|----
form | 指定按钮关联的表单
formaction | 覆盖 form 元素的 action 属性
formenctype |  覆盖 form 元素的 enctype 属性
formmethod | 覆盖 form 元素的 method 属性
formtarget | 覆盖 form 元素的 target 属性
formnovalidate | 覆盖 form 元素的 novalidate 属性

**type 为 text 值时**

标签 | 语义化
----|------|----
list |  指定为文本框提供建议值的 datalist 元素，其值为datalist 元素的 id 值
maxlength | 设置文本框最大字符长度
pattern | 用于输入验证的正则表达式
placeholder | 输入字符的提示
readonly |  `文本框处于只读状态`
disabled |  文本框处于禁用状态
size |  设置文本框宽度
value | 设置文本框初始值
required |  表明用户必须输入一个值，否则无法通过输入验证


**type 为 password 值时**

标签 | 语义化
----|------|----
maxlength | 设置密码框最大字符长度
pattern | 用于输入验证的正则表达式
placeholder | 输入密码的提示
readonly |  密码框处于只读状态
disabled |  文本框处于禁用状态
size |  设置密码框宽度
value | 设置密码框初始值
required |  `表明用户必须输入同一个值`


**type 为 number、range 时**

标签 | 语义化
----|------|----
list |  指定为文本框提供建议值的 datalist 元素，其值为datalist 元素的 id 值
min | 设置可接受的最小值
max | 设定可接受的最大值
readonly |  设置文本框内容只读
required |  `表明用户必须输入一个值，否则无法通过输入验证`
step |  指定上下调节值的步长
value | 指定初始值


**type 为 checkbox、radio 时**

标签 | 语义化
----|------|----
checked | `设置复选框、单选框是否为勾选状态`
required |  `表示用户必须勾选，否则无法通过验证`
value | `设置复选框、单选框勾选状态时提交的数据。默认为 on`


**type 为 image 时**

标签 | 语义化
----|------|----
src | 指定要显示图像的 URL
alt | 提供图片的文字说明
width | 图像的长度
height |  图像的高度
提交额外属性 |  formaction、formenctype、formmethod、formtarget和 formnovalidate。


**type 为 file 时**

标签 | 语义化
----|------|----
accept |  指定接受的 MIME 类型 accept="image/gif, image/jpeg, image/png"
required |  表明用户必须提供一个值，否则无法通过验证

> type = email 为电子邮件格式、tel 为电话格式、url 为网址格式。额外属性和 text 一致。但对于这几种类型，浏览器支持是不同的。email 支持比较好，现在浏览器都支持格式验证；tel 基本不支持；url 支持一般，部分浏览器只要检测到 http://就能通过。
seelct optgroup分组option，效果类似在下拉菜单中加一个空行

**output 计算结果**
```
<form oninput="res.value = num1.valueAsNumber * num2.valueAsNumber">
    <input type="number" id="num1"> x <input type="number" id="num2">
    <output for="num1 num2" name="res">
</form>
```
**实体代码**
![实体代码](http://upload-images.jianshu.io/upload_images/3317226-80251f303ee35b87.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**meta 元数据 **

标签 | 语义化
----|------|----
generator | 当前页面的编码工具
refresh | 重新载入当前页面，或指定一个 URL。单位秒。

**全局属性**

标签 | 语义化
----|------|----
accesskey | input快捷键操作，windows 下 alt+指定键，前提是浏览器 alt 并不冲突。
contenteditable | 让文本处于可编辑状态，设置 true 则可以编辑，false则不可编辑。或者直接设置属性。
lang | 可以局部设置语言，en（英文）zh-CN（简体中文）。
tabindex | 表单中按下 tab 键，实现获取焦点的顺序。如果是-1，则不会被选中。

引自：[李炎恢 HTML CSS JavaScript PHP ](https://wizardforcel.gitbooks.io/liyanhui-tutorials/content/1.html)
