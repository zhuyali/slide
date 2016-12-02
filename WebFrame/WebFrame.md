jQuery

- - -

库 or 框架？

jQuery实际是一个JavaScript脚本库，它并不能帮我们解决脚本的引用管理和功能管理，只是帮我们完成编码逻辑，实现业务功能。

- - -

HTML 元素选取及操作,CSS 操作

$(document).ready(function() {
  $(selector).action()
});

selector:
- 元素选择器 $("p#id")
- 属性选择器 $("[href$='.jpg']")
- CSS 选择器 $("p").css("","")

存在命名冲突
var jq = jQuery.noConflict()

JavaScript 特效和动画
- 链式调用

HTML DOM 遍历和修改
- 根据元素层级关系进行遍历查找
- 过滤元素，基于一组元素中的位置来选择一个特定的元素

- - -

jQuery 其实就是一个函数库
- 封装了复杂的 DOM 原生操作
(元素选取，层级关系，元素操作，属性控制)
- 对 DOM 进行操作
(元素插入，元素删除，元素克隆，元素替代)
- 建立了 DOM 与 CSS 的联系
(改变元素样式)
- 封装了网络请求
(AJAX 进行异步网络请求)
